Nov20-2025.



### 🎯 Best Title Recommendation
The cleanest and most accurate option is:

**“Automating IAM Access Key Rotation with AWS Lambda, EventBridge, and SNS Notifications”**

Why?
- **EventBridge** is the current AWS service name.  
- **SNS Notifications** makes it clear that users will get alerts.  
- It’s concise, professional, and Medium readers will immediately understand the stack.




---

# Question 1: 

Jee haan, aapka **samajhna bilkul theek** hai\! EventBridge (jo pehle CloudWatch Events tha) isi tarah kaam karta hai:

## 1\. `aws_cloudwatch_event_rule` (The Schedule) ⏰

```terraform
resource "aws_cloudwatch_event_rule" "daily_schedule" {
  # ...
  schedule_expression = "cron(0 12 * * ? *)"
}
```

  * **Maqsad:** Yeh resource ek **"Event Rule"** banata hai. Iska bunyadi kaam **Cronjob** ya **Scheduled Task** ki tarah hai.
  * **Kaam:** Yeh define karta hai ke koi kaam **kab** (when) hona chahiye. Humne yahan `cron(0 12 * * ? *)` istemaal kiya hai, jo bilkul Linux ke cronjob ki tarah **har roz 12:00 PM UTC** par trigger hota hai.

-----

## 2\. `aws_cloudwatch_event_target` (The Target/Link) 🎯



```terraform
resource "aws_cloudwatch_event_target" "lambda_target" {
  rule = aws_cloudwatch_event_rule.daily_schedule.name
  arn  = aws_lambda_function.log_exporter.arn
}
```

  * **Maqsad:** Yeh resource **Rule** aur **Action** ke beech mein **link** (ya **target**) banata hai.
  * **Kaam:** Yeh rule se kehta hai, "Jab tumhara time ho jaye (yaani daily 12:00 PM par), toh **is ARN** (Amazon Resource Name) ko chala do."
  * **Ahamiyat:** Hum yahan **Lambda Function** ka **ARN** dete hain, iska matlab hai ke yeh seedha us **Lambda function ko trigger karta hai**.

-----

## Conclusion

Is tarah, dono resources mil kar yeh automation poora karte hain:

$$\text{Event Rule (Schedule)} \rightarrow \text{Event Target (Link)} \rightarrow \text{Lambda Function (Action)}$$

Yeh **loosely coupled** tareeqa hai, jahan schedule aur action alag alag hain, jo Terraform mein ek behtareen design hai.


---

# Question 2: 

بہت اہم سوال ہے\! یہ سمجھنا ضروری ہے کہ CloudWatch Logs mein data aata kahan se hai aur hum kiska log export kar rahe hain. 🧐

-----


```bash
aws_cloudwatch_event_rule:
yani ya cronjob provide krta ha

aws_cloudwatch_event_target:
ya lambda function ko target krta ha 
```

## 1\. CloudWatch Logs Mein Kiska Data Hota Hai? (What Data is in CloudWatch Logs?)

**CloudWatch Logs** ek central service hai jahan aapki saari applications aur AWS services ke **Text Logs** jama (store) hote hain.

CloudWatch mein data (logs) mukhtalif sources se aata hai:

| Source (Kahan Se Aata Hai) | Misaal (Example Log Group) |
| :--- | :--- |
| **AWS Lambda** | Jab bhi aapka koi Lambda function run hota hai, uska `print()` ya `console.log` output `/aws/lambda/function-name` mein jata hai. **(Hum isi tarah ke log group ka data export kar rahe hain).** |
| **Amazon EC2 (Servers)** | Agar aap EC2 instance par CloudWatch Agent install karein, toh woh server ke system logs (`/var/log/messages`) ko CloudWatch mein bhejta hai. |
| **Amazon ECS/EKS (Containers)** | Containerized applications ka output yahan jama hota hai. |
| **VPC Flow Logs** | Aapke Virtual Private Cloud (VPC) mein hone wale network traffic ki tafseelat. |
| **API Gateway** | API calls ki access aur error logs. |

-----

## 2\. Hum Kiska Log Export Kar Rahe Hain? (Whose Logs Are We Exporting?)

Aapke task mein, hum CloudWatch Logs mein maujood **kisi bhi Log Group** ka data export kar sakte hain.

Humara Terraform code ek **`target_log_group_name`** variable istemaal kar raha hai:

```terraform
variable "target_log_group_name" {
  description = "The name of the CloudWatch Log Group you want to export (e.g., /aws/lambda/MyFunction)."
  type        = string
}
```

Iska matlab hai:

1.  Aapki **`terraform.tfvars`** file mein aap jis Log Group ka naam denge (maslan: `/aws/lambda/MyWebAppLogGroup`), us Log Group ke andar jitne bhi logs (application errors, info messages, etc.) hain, hum unko export kar rahe hain.
2.  **Woh data khud-ba-khud aata hai** kyunki AWS services (jaise Lambda) **natively** (qudrati taur par) apne logs CloudWatch mein bhejte hain.

### Flow of Data (Data ka Bahao)

Aapki application se data CloudWatch tak is tarah aata hai:

$$\text{User/Application Request} \xrightarrow{\text{Runs Code}} \text{AWS Service (e.g., Lambda)} \xrightarrow{\text{Writes Logs}} \text{CloudWatch Log Group}$$

Aur humara automation is data ko yahan se uthaata hai:

$$\text{CloudWatch Log Group} \xrightarrow{\text{Lambda Export Task}} \text{S3 Bucket}$$

Commit date: October 18, 2025.
