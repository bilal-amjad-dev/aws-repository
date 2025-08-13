


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b78cbf9e-d77a-4ff4-b14a-bf7a3b18c14d" />


In this diagra, we know about VPC, SIR. Now, we have 3 new concepts:
- **T**arget group (we set target)
- **L**oad balancer (We send load to Target)
- **A**uto scaling group (launch template, it is important because we tell when new ec2 will get created, according to this template, new ec2 instance should get created)


### VPC
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5275ccf1-5849-47be-b704-860919c4e775" />

### Internet Gateway
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/12c4a893-f080-4a49-8d1d-e1a6f3d21724" />

- Attach to VPC
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5e855408-ee4d-42bc-8081-4b9c5c49b30c" />

### Subnet 
Here we learn a new thing, we can create more than 1 subnet while living in the same option 

- Subnet 1
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/ce4b8d13-5abc-4a8e-8c3e-cb4a38624a5e" />

- Subnet 2
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/88b65917-0e04-4253-9e3d-2450d7305cdd" />

Now, our **2 subnets** have created:
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e55e91ce-96e5-4c29-84ba-04ef452b2198" />

### Implied Router
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/02350d35-5ab1-415d-b086-2994bbb8d325" />

- Association of Implied Router and Subnets
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/375fbe10-221e-4266-aeb2-3a841624c911" />

- Add route 0.0.0.0/0:Internet GW in Route table
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/50ebd3fa-9be0-48cd-bd90-1506aad3638f" />

Till now, we already know. Now, 3 new things:

- **T**arget group
- **L**oad balancer
- **A**uto scaling group 

---

### Target group 
- Choose your target
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/882cf79c-e560-4000-96cb-1a52ac20da45" />
- Your target group name
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/dfd46626-0a5b-456f-8d68-ea9e89b394ed" />
- Select your vpc
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4602c975-3ed9-4efc-9a6f-26bb634b63a7" />
- Target group created successfully
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/2d413359-3999-4d48-b2fe-058ab49699cb" />


### Load balancer

- You can see our **Target group** has been created, but it has no load balancer. Let's create:
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/fa1a20ab-790e-4104-80ec-1338042fac2a" />


- Create load balancer
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/c5a740ff-7d81-4a66-8e5c-4e8ad13e5c63" />

- Application Load Balancer
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/3a160097-0e3c-4f6c-8dc6-8b1b14bcab20" />

- your load balancer name
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/88efc714-d1b6-4aee-801e-8af8b79493ba" />

- select your VPC
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/ac09c406-cc03-4f57-b5c5-278ff9a3156d" />

- select Availability zones
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/c2729b27-88aa-41c4-8f64-a33dab055737" />

- sg


<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/a0f9cd63-8359-48a6-b798-1e64cec7fd84" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/d9eab591-dbd2-47d0-98a7-2936da56e950" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/aaebaf18-b9f2-4f1d-85c9-369e6fe9a702" />


- Listeners and routing (request ko sunna and aagy route krna)
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/26ed07d4-97c8-41a6-a325-cbfaf9b1e204" />

- summary (what we have done so far in **Load balancer**)
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/af7695bf-0a29-4a34-bb44-592a9d57c00c" />



---

### Auto scaling group (it has launch template, kis trh ka ec2 mazeed create krny hain)

- create Auto scaling group
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/46c351ca-2f48-44f7-b296-42f89670a6c3" />

- ASG name
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/86df79a7-6c0d-4a88-a7b1-4ab0969906d4" />

- Launch template
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/4b437711-ddd2-42ba-9a85-b50735140974" />

- Launch template name
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/65bde356-9a25-4952-9fee-b79d36544cce" />

- Launch template ami 
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5099b491-e57e-45de-8287-69ccca97a93c" />

- Launch template instancetype
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/be8ad382-1317-4e60-8c95-727557fea8a6" />

- Launch template keypiar
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/01940d86-95ac-4e3b-bf35-68865efa4607" />

- Launch template NO-Subet
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b3fa76ee-2825-4448-bf42-53657517119d" />

- Lauch template sg
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/0f10a40e-af40-4c3d-9c2f-a38dcbf1b615" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/3da8ff53-672c-4ae4-af1e-8f0e81e6b3db" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b163b68f-c57d-45b1-b750-fd912bb648f9" />


- Launch template enable publicip
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/77afcc66-1608-4652-bdd7-94d31c3f382c" />


- Launch template userdata
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/3bd580a8-da8f-4ba2-80cc-f58a2b78b88d" />


- Search Launch template you created
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/70bb2494-39a2-43ab-bcf3-64cb9f6777e0" />


- Select VPC and Availabilty Zones
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/5570b5f3-d8b4-4682-b28d-442576fc605b" />


- attach an existing Load Balancer
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/b2f4b045-095a-4e88-bc9c-7659d960ba6e" />


- health check grace period
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/64908b88-60f3-4227-8713-19685f834c86" />


- configure group size (desire, min, max), and scaling policy

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/dfef26f5-bf8d-487e-9b30-3fd7d9d71246" />


---

### Testimonial

- You can see our ec2 instances were created by AutoScalingGroup

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/998367db-5c62-474e-86e7-368a24d8a620" />


- Copy Loadbalancer's DNS and paste in browser:
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/2ab206ca-357b-4151-958a-d28020dee030" />

<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/9c078aab-e720-4977-a62e-98addfb54442" />

- Refresh
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/f411b48d-c81c-4af4-a30e-abdd7e6b5739" />



### Test (terminate 1 instance and ASG will automatically create it)
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/82a308bc-0d85-4724-bbe8-30d1d51ef4b4" />


### You can see it is automatically created by AutoScalingGroup 
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/102cdfeb-8a99-44e8-9bde-f906d928d09d" />



### AutoScalingGroup (Instance management healthCheck)
<img width="1600" height="900" alt="Image" src="https://github.com/user-attachments/assets/e5fd2b9a-ffc9-4ed1-bb23-a2d8cbecd3e2" />


Source: Rahul Wagh
Commit Date: 13-Aug-2025



