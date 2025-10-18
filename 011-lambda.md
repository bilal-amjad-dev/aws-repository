

### Lambda
Prepare Lambda Source Code (ZIP file)
- archive_file


**IAM Roles and Policies**

- aws_iam_role
- aws_iam_policy
- aws_iam_policy_attachment

**Lambda Function**
- aws_lambda_function

### CloudWatch Event & Target


**EventBridge Rule (Daily Schedule)**
- aws_cloudwatch_event_rule



**EventBridge Target and Permission**
- aws_cloudwatch_event_target
- aws_lambda_permission



Lambda function ki default seeting hoti hai ke koi be bahar ki service usay chala (invoke) nahi sakti.

aws_lambda_permission resource Lambda ki Access Policy mein ek Ijazat Nama (Permission Slip) add karta hai.

Agar aap yeh permission nahi denge, to EventBridge ka schedule ban jaye ga, target set ho jaye ga, magar jab woh chalne ki koshish kare ga, to Lambda Access Denied error de kar trigger ko fail kar dega

Commit date: October 18, 2025.
