






12-Nov-2025.


<img width="978" height="571" alt="image" src="https://github.com/user-attachments/assets/21b48b22-2656-4a85-8bd6-e25b8998e2cd" />


Bilkul sahi 💯

AWS Config mein **do tarah ke rules** hotay hain:

1. **AWS Managed Rules** –
   Yeh wo rules hain jo AWS ne pehle se banaye hue hain.
   Jaise:

   * `s3-bucket-public-read-prohibited`
   * `restricted-ssh`
   * `ec2-instance-no-public-ip`
     Inhe tum **direct enable** kar sakte ho.

2. **Custom Rules** –
   Yeh tum **khud banate ho** Lambda function ke zariye.
   Jaise agar tum chaho ke:
   “Har EC2 instance ka tag ‘Environment’ hona chahiye,”
   to tum ek **custom AWS Config rule** bana sakte ho jo Lambda se check kare.

To haan — kuch rules AWS deta hai (ready-made),
aur kuch tum apni company ke policies ke hisaab se khud likh sakte ho.



---
---


Bahut acha sawaal 👏

**Compliance** aur **Audit** dono security aur governance se related terms hain 👇

🔹 **Compliance** ka matlab:
AWS Config check karta hai ke tumhare resources **company ya industry ke rules** follow kar rahe hain ya nahi.
Jaise:

* Kya S3 bucket private hai?
* Kya EC2 instances encrypted volume use kar rahe hain?
* Kya SSH port (22) public open to world nahi hai?
  Agar koi resource rule break kare, AWS Config usay **non-compliant** mark kar deta hai.

🔹 **Audit** ka matlab:
Har change ka record rakhna — kisne kya change kiya, kab aur kis resource pe.
Jaise agar kisi ne bucket public kar di, AWS Config uska history rakh lega.
Ye information auditors ya security team ko madad karti hai **track aur verify** karne mein.

👉 Simple Roman Urdu main:
Compliance ka matlab hai **rules follow ho rahe hain ya nahi**,
Audit ka matlab hai **kisne kya badla aur kab**, uska pura record.



