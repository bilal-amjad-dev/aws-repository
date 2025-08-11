## Create VPC with a Public Subnet

### VPC 
- Click create VPC
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/ffb73ad0-5ed5-4266-a7f9-a9a1ece22301" />

- Name your VPC
- Type CIDR `10.0.0.0/16`
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/ee430fd3-0d73-49ef-b40f-11b19e7d612b" />

- and click create
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/31bff9eb-e74a-4817-84a4-5d82b0d69367" />

- vpc created successfully
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/32c8f03f-3072-41a2-a3af-735ae2f9c604" />

---

### Subnet 

- Click create subnet
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/6f913021-abb6-45ef-9745-13e86d319b4e" />

- Select VPC
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/9566af2a-12c1-49db-aaee-154b6e1f0f9c" />

- Name your subnet
- Select Availability Zone

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/7e98d4a0-fa1b-4eec-97e6-0b246fdb2771" />

- Type CIDR `10.0.0.0/24`
- and click create
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5b5cb305-f46b-4074-bdf2-69dfea25c59a" />

- subnet created successfully
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/d574219a-5cdb-4be9-ab11-35307e364f28" />



--- 

### Internet Gateway

- Click create internet gateway
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/461982ae-7273-49b1-aba1-03bb430f72eb" />

- Name your internet gateway
- and click create
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e12b5833-43b8-47cc-8581-21900b0d045d" />

- internet gateway created successfully
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/f3078a04-ac15-45ac-a53d-7ed0bb92a5c2" />

- **Attach to VPC**
  - Select vpc
    
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/14ad1b18-1ec1-4794-abb7-6c61bf4e0f24" />
 
  -  and click attach

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/552204cd-0205-45f6-a169-4d7c0a706e35" />

   - internet gateway attached successfully

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/1baeb8cc-e553-4fb2-9ab1-b1420a2fed2b" />


--- 

### Implied Router 

- Click create route table

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/f2eda6bf-92e8-4085-ae54-5119344a1ba8" />

- Select VPC
- and click create route table
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b4f66410-39f7-4911-98bf-7d30bee2d460" />

- route table created successfully
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5a122bcc-4811-422a-b31b-6243f5250886" />

- **Associate route table to Subnet**
- Select subnet
- and click save association

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4ead28c6-5b24-4a6d-bbd4-90f205eb6dc1" />

- route table associated successfully

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/23511bf4-9ff4-4853-bbab-ab8d8289aa31" />


- **Add route 0.0.0.0/0:Internet Gateway**
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/ada2a097-ec45-4810-baef-5cbf4fc44a8d" />

  - Click add route
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b81e544d-80ad-42aa-af35-d4871ac42a4c" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e5fc64e3-f2cc-4cfd-b104-3a785b8ca254" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b51d20ee-5ab2-4918-a3ec-1a8754e434e0" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/a1f0af53-3feb-470f-8748-d237418259f3" />




--- 
--- 
### Create EC2 in the same vpc and public subnet 

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5e0e42c6-7e65-4e97-8c2f-001e8cc5c243" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/45add824-6dd4-4902-92b0-3eafa22b5470" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/2d368edb-d2ed-47e7-acc5-bdbafebe2e5a" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/21ceacd4-eaa3-4e1e-9314-f13bf1764d08" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e3b50280-42f3-4181-9265-6c9c74b76c3b" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/6e71b2c9-a2d7-4a9c-98f8-878a406f9208" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/42d2ed7c-c96d-4833-870d-51c890e67cc6" />











Commit Date: 11-Aug-2025

