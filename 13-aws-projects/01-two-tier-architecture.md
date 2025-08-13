# Two-Tier Architecture in AWS

![](https://miro.medium.com/v2/resize:fit:720/format:webp/1*HLo4DPIkM-fFjK9LfBFIww.png)


https://medium.com/@labossiere01/two-tier-architecture-in-aws-82966e26929f

In this article, we have:
- vpc
- 4 subnets (4 total)
  - 2 public subnets **(One in each AZ)**
  - 2 private subnets **(One in each AZ)**
 
- Internet Gateway
- Implied Router
  - Public router
  - Private router

- NAT Gateway (2 total): One in each public subnet

(here don't forget: 
- attachment of igw and vpc
- association of implied router and subnet
- add route 0.0.0.0/0:InternetGW)

The author of the blog post created only one EC2 instance and placed it in a single public subnet. This is a common approach for a **simple demonstration or a non-critical development environment**, but it's not the best practice for a production website.


In a true multi-AZ setup for the web tier, the author would have done the following:

1. Created an **EC2 Launch Template**.

2. Set up an **Auto Scaling Group** using that launch template.

3. Configured the Auto Scaling Group to launch instances in **both public subnets** (one in each AZ).

4. Created a **Load Balancer** and placed it in both public subnets.

5. Associated the Auto Scaling Group with the Load Balancer.

So, to summarize your observation: the author created a multi-AZ network foundation, but only deployed a single EC2 instance, making the web server a single point of failure. This is fine for a learning exercise but would be considered a significant vulnerability in a real-world, production environment.








Commit Date: 13-Aug-2025
