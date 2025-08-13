


# 🧠 Relational vs Non-Relational Databases

## 📊 Relational Database (SQL)

- Stores **structured data** in **tables** (rows and columns)
- Uses **SQL** for querying and managing data
- Tables are linked using **relationships** (foreign keys)
- Requires a **fixed schema** (defined columns and types)

### ✅ Examples:
- MySQL
- PostgreSQL
- Oracle
- SQL Server
- Amazon RDS

### 🏢 Use Cases:
- Banking systems
- E-commerce platforms
- Inventory management
- CRM systems

---

## 📦 Non-Relational Database (NoSQL)

- Stores **unstructured or semi-structured data**
- No fixed schema—flexible formats like **JSON**, **key-value**, **documents**, **graphs**
- Designed for **scalability** and **high performance**
- Doesn’t use SQL (though some support SQL-like queries)

### ✅ Types & Examples:

| Type         | Example           | Description                          |
|--------------|-------------------|--------------------------------------|
| Document     | MongoDB           | Stores JSON-like documents           |
| Key-Value    | Redis, DynamoDB   | Fast access via keys                 |
| Column-Based | Cassandra         | Optimized for large-scale analytics  |
| Graph        | Neo4j             | Stores relationships as graphs       |

### 🚀 Use Cases:
- Real-time analytics
- Social media apps
- IoT data ingestion
- Recommendation engines

---

## 🧁 Analogy Time

- 📊 **Relational DB** = Excel spreadsheet with strict columns and formulas  
- 📦 **Non-Relational DB** = A folder of flexible notes, images, and files—organized your way

---

## 🧠 Summary Table

| Feature               | Relational DB (SQL)         | Non-Relational DB (NoSQL)       |
|------------------------|-----------------------------|----------------------------------|
| 📐 Schema              | Fixed                       | Flexible                         |
| 🔗 Relationships       | Strong (foreign keys)       | Weak or none                     |
| 🔍 Query Language      | SQL                         | Varies (MongoQL, APIs, etc.)     |
| 📁 Data Format         | Tables                      | JSON, key-value, documents       |
| 📈 Scalability         | Vertical (scale up)         | Horizontal (scale out)           |
| 🧰 Use Case            | Structured business data     | Unstructured, fast-changing data |



---


# 📚 AWS Concepts: RDS, NoSQL, Web Servers vs Static Websites

---

## ❓ Question 1: Does RDS Offer NoSQL Databases?

> “Run a custom or NoSQL database → EC2 + EBS”  
You're asking: Does RDS not support NoSQL?

### ✅ Answer:
Amazon RDS supports **only relational (SQL) databases**. Here's what RDS offers:

| Database Engine   | Type       |
|-------------------|------------|
| MySQL             | Relational |
| PostgreSQL        | Relational |
| MariaDB           | Relational |
| Oracle            | Relational |
| SQL Server        | Relational |
| Amazon Aurora     | Relational |

### ❌ RDS does **not** support NoSQL databases like:

- MongoDB  
- Cassandra  
- Redis *(use Amazon ElastiCache instead)*  
- DynamoDB *(AWS’s own NoSQL service, separate from RDS)*

### 🔧 Want NoSQL or custom DBs?
Use **EC2 + EBS** to install and manage your own database engine.

---

## ❓ Question 2: Difference Between Web Server and Static Website?

### 🖥️ Web Server (EC2 + EBS)

- Runs **dynamic websites or applications**
- Uses software like **Apache**, **Nginx**, or **Node.js**
- Can process user input, connect to databases, and generate dynamic content
- Example: E-commerce site with login, search, and orders
- Requires **EC2** for compute and **EBS** for storage

### 🌐 Static Website (S3)

- Contains only **HTML, CSS, JS** files
- No server-side logic or database
- Just displays content—no login, no form processing
- Example: Portfolio site or company homepage
- Hosted directly from **S3 buckets**, no EC2 needed

---

## 🧠 Summary Table

| Feature              | Web Server (EC2 + EBS)     | Static Website (S3)             |
|----------------------|-----------------------------|----------------------------------|
| 🔄 Dynamic Content    | Yes                         | No                               |
| 🧠 Server Logic       | Yes (e.g., PHP, Node.js)    | No                               |
| 🗄️ Storage            | EBS                         | S3                               |
| 🖥️ Compute Required   | EC2                         | None                             |
| 🌍 Hosting Method     | Apache/Nginx on EC2         | S3 Static Website Hosting        |
| ⚙️ Use Case           | Apps, e-commerce, dashboards| Portfolios, blogs, landing pages |

---




# 📊 AWS Database Usage: RDS vs DynamoDB vs EC2 + Custom DB

---

## ❓ Which Is Mostly Used?

### ✅ 1. Amazon RDS (Relational)
- Managed SQL databases (MySQL, PostgreSQL, Oracle, etc.)
- Ideal for structured data, ACID transactions, and complex queries
- Common in enterprise systems, e-commerce, and legacy migrations
- Often paired with EC2 for full-stack apps (e.g., LAMP/MEAN stacks)

### ✅ 2. Amazon DynamoDB (NoSQL)
- Fully managed NoSQL database with high scalability and low latency
- Used by companies like Netflix, Lyft, and Airbnb
- Great for real-time apps, IoT, gaming, mobile, and serverless architectures

### ✅ 3. EC2 + Custom DB (MongoDB, Cassandra, etc.)
- Used when full control over the database engine is needed
- Suitable for unsupported DBs in RDS or legacy systems
- Requires manual setup, scaling, and maintenance

---

## 📊 Usage Summary

| Setup               | Use Case Strengths                              | Popularity Trend       |
|---------------------|--------------------------------------------------|------------------------|
| 🗃️ RDS              | Structured data, SQL apps, enterprise systems    | ⭐⭐⭐⭐⭐ (Very High)     |
| 📦 DynamoDB         | NoSQL, serverless, scalable apps                 | ⭐⭐⭐⭐⭐ (Very High)     |
| ⚙️ EC2 + Custom DB  | Full control, unsupported DBs, legacy migration  | ⭐⭐⭐ (Moderate)        |

---

## 🧠 Final Thought

Many modern AWS architectures use **RDS or DynamoDB**, depending on the data model.  
Some even **combine both**—for example:

- RDS for transactional data  
- DynamoDB for caching or fast lookups

Choose based on your app’s scalability, flexibility, and query needs.






Commit Date: 07-Aug-2025

Commit Date: 13-Aug-2025
