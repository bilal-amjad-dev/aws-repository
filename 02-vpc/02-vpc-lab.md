### Create VPC with a Public and Private subnet


- VPc
- Subnet
	- Public Subnet
	- Private Subnet
- Internet Gateway
- Implied Router
	- Implied Router for Public subnet
	- Implied Router for Private subnet

- attach igw with vpc
- Public Route table association with Public subnet
- Add route 0.0.0.0/0:InternetGW
- Private Route table association with Private subnet
- Add route 0.0.0.0/0:NATGW


### VPC

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/315ea967-050a-4964-b470-0d1955c9d9ad" />


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/042e6a6d-d2bc-4b29-ad05-91df6ae6821c" />


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/151982bf-12bb-4b7c-9fff-4dd40d7d0344" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5c941313-026d-42d5-b93f-89ce238fadf6" />

### Subnet (Public Subnet)

- **Public Subnet**

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/8d3c5243-4216-4a90-8caa-5f9ae80343fc" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e3750f46-0b96-40e3-ad4a-9e607c764a1e" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/248d5c73-4feb-42fe-adfe-6530561a958d" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/39329066-1aac-45c1-9394-cf75d9163cb1" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/a03d977a-d4da-4a61-8e90-f7fb2c000afa" />




- **Private Subnet**

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/97457b6f-b631-4f4b-8aff-5b28ec8b067d" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/80d8fc34-5380-4631-a771-3b59aa002791" />


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/be638cca-7dd6-4863-b420-bb1212908bc7" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/9419d968-2b92-4111-8763-690723d7d192" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/c99a4d28-9f7e-466f-b78b-e03d1721f8bd" />




### Internet Gateway

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/24f92f15-1db1-4358-ae94-14fe80da4b5a" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/187c89f8-45d0-4d74-9637-27a2c82018c1" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b64e31de-a0cf-454b-9932-e68c9e2ac0ce" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/7629f6bb-15d3-487e-a22a-57af5fce386f" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/d72aa9d6-f07e-41a3-9f62-d1630c4763aa" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b0253b42-289b-424c-8c3f-e9382bd076b1" />








### Implied Router



- Router for Public Subnet

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/873e16fd-d938-4cd2-ac0c-3eeea41b0679" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/746910f1-efb9-4eac-beca-8fd3494441b9" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/02a0b9c2-4f4d-4222-be70-25a2536ca593" />




- Router for Private Subnet



<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e6015dc1-52eb-450e-accf-36bb67afddd5" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/f7ad36ca-9d8a-449c-b301-ff4db8d50aae" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/eb877509-289f-46fb-8f6e-b1ac410942da" />



    - Public Route table association with Public subnet


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/2c33aa7f-a521-44a6-a630-5f4b5bf5c345" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/abb5bd5b-c6f3-4b19-96f1-f356678cab8f" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4faf88d5-7f5e-4b17-a2ef-5630cfa3de3b" />



    - add route 0.0.0.0/0:igw in route table
    
    
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/cf15c111-75fe-4bbd-812a-21449db3b932" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/472e2650-2476-4fde-8fe3-9cf5a616eb79" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/46ec3da0-0af2-4b78-98ac-e599c61e616a" />

    
    
    
    - Private Route table association with Private subnet


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/bca80dba-0227-4b12-8eb0-0b052b7b5838" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/fc61856c-9e88-45c6-8cea-a4a1d3ba3ccf" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4914eda5-6328-4591-be85-6526a76d16ef" />



---
---

### Create EC2 in Public Subnet


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/08f55d29-3f22-4036-8a1b-495dc96e1c9f" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/7d0d3cf8-8203-4a94-ac6b-9fe3e03d8a88" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/365b3aaf-5f43-4895-bc84-f06000840c4f" />

- vpc
- public subnet
- auto-assign PublicIp: Disable

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/f2d1a96f-72c9-4ea8-b59f-6e2e678c1cde" />

- Enable

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/9fde3aa1-d6ac-4bc8-8b49-47b73f8340fb" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e0ea2bd0-e14c-4a0b-b0be-4393541e2fc2" />




### Create EC2 in Private Subnet


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/da5c90c4-199b-4ae5-ae2b-33cfaad59fd8" />

- vpc
- private subnet
- auto-assign PublicIp: Disable, and we need it because we are creating PRIVATE EC2
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/bfbce640-ef98-45ef-baa5-d8987448f167" />


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/a99c57ab-86eb-4137-abac-f4255416d26e" />

---



Now i can't access private subnet because i don't have its public ip. 

1- go inside public subnet. 
2- access private subnet keeping living in public subnet 


- because 
vpc ky adr 2 subnets aaps ma bat kr skty hain 

- but  
ma private subnet ko internet ka though directly acces ni kr skta
i can't access directly through intenret .


private subnet ka andr aany ka bad, type 

and type ping 8.8.8.8 

you can see ya Internet pa ni ja pa rha. is gareeb aadmi ka pass rasta hi ni ha Internet pa jany ka 



- you can see request time out 

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4d497d43-0ddd-41d4-9b78-0e0ca53fae1d" />



# NAT Gateway

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/9ce92d72-b231-41a7-9e27-2240235ac886" />

- Always remember: NAT Gateway is always created in Public Subnet

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/3872ac04-7730-44a9-abce-082bc215fdf0" />

- Always remember: NAT Gateway always take ElasticIP, Allocate ElasticIP, 

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/d76e4b7a-1256-422a-973a-ec892b6a742f" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/1cd432b7-73a6-487f-969f-91169425f2d3" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/9677778c-363c-40c8-a247-710af10b788f" />



### Edit Route of Private route table: 0.0.0.0/0: NATGW

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4e1c232b-80b8-4703-9017-9291db4ab2d5" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/2c293612-bb71-45d2-8599-1e65cb68fae2" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e9f4f1a9-c93b-4eda-84ae-d49dbdae1cef" />





- Aap dekh skty hain, respond aana shuru ho gya ha 

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/794a6aa6-6802-4a9a-8590-c82f4d206eca" />


---

Diagram:

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/1027e97e-123b-4377-9905-e7a3703c6e4b" />

---
























Commit Date: 12-Aug-2025





























Commit Date: 11-Aug-2025
