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
