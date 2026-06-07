# 💰 AWS Pricing Model

---

## 1. Three Fundamental Drivers of Cost with AWS

AWS charges you based on **3 main things**. Think of it like running a business — you pay for the machines you use, the storage space you rent, and the deliveries you send out.

> 💡 **Simple Analogy:** Imagine running a **food delivery business**:
> - 🖥️ **Compute** = The vehicles/drivers running your deliveries (you pay per hour or per trip)
> - 📦 **Storage** = The warehouse where you store your products (you pay per shelf/GB)
> - 🚚 **Data Transfer** = Sending packages out to customers (outbound costs money; receiving supplies is free)

---

### 🖥️ Compute

The cost of **processing power** — running servers, VMs, or functions.

- Calculated **by the hour** or **by the second** (depending on the service)
- Cost **varies by instance type** (more powerful = more expensive)

```
Small instance  → Less CPU/RAM → Lower cost
Large instance  → More CPU/RAM → Higher cost
```

**Example:** Running an EC2 instance for 10 hours at $0.02/hour = **$0.20**

---

### 📦 Storage

The cost of **storing data** in the cloud.

- Charged **per GB per month**
- Applies to services like Amazon S3, EBS volumes, databases

```
Data stored: 100 GB × $0.023/GB = $2.30/month
```

**Example:** Storing 500 photos totalling 50 GB on Amazon S3

---

### 🚚 Data Transfer

The cost of **moving data** in and out of AWS.

| Direction | Charge | Analogy |
|---|---|---|
| **Inbound** (into AWS) | ✅ Free (mostly) | Receiving supplies at your warehouse — no cost |
| **Outbound** (out of AWS) | 💰 Charged per GB | Shipping packages to customers — you pay per delivery |

- Outbound traffic is **aggregated** then charged
- Price typically decreases as volume increases

> ⚠️ **Note:** Some exceptions exist for inbound charges (e.g., data transfer between AWS regions).

---

### 📊 Three Cost Drivers — Summary

| Driver | How Charged | Free? |
|---|---|---|
| **Compute** | Per hour or per second | ❌ |
| **Storage** | Per GB per month | ❌ |
| **Data Transfer (In)** | Per GB | ✅ Free |
| **Data Transfer (Out)** | Per GB (aggregated) | ❌ |

---

## 2. What is Inbound vs Outbound?

> 💡 **Simple Analogy:** Think of AWS like your **home**:
> - **Inbound** = Someone delivering a package **to your house** — the delivery is free for you
> - **Outbound** = You shipping a package **from your house** to someone else — you pay the postage

### In AWS terms:

```
The Internet / Users
        ↓  (Inbound — FREE)
   [ AWS Cloud ]
        ↓  (Outbound — CHARGED per GB)
The Internet / Users
```

| Term | Meaning | Example | Cost |
|---|---|---|---|
| **Inbound** | Data coming **INTO** AWS | User uploading a file to S3 | ✅ Free |
| **Outbound** | Data going **OUT OF** AWS | User downloading a file from S3 | 💰 Charged |

---

## 3. How Do You Pay for AWS?

AWS offers **3 pricing models** — designed to give you flexibility and reward smart usage.

---

### 💳 1. Pay for What You Use

Only pay for the resources you actually consume — **no upfront cost, no contracts**.

> 💡 **Analogy:** Like paying for a **taxi** — you only pay for the distance you actually travel. No monthly subscription, no commitment.

- Turn resources on → pay
- Turn resources off → stop paying
- Perfect for unpredictable or variable workloads

```
Used 5 hours of EC2?  → Pay for 5 hours only
Used 0 hours?         → Pay nothing
```

---

### 🏷️ 2. Pay Less When You Reserve

**Commit** to using a resource for 1 or 3 years → get a **significant discount** (up to 75% off).

> 💡 **Analogy:** Like signing a **long-term apartment lease**. Monthly rent is much cheaper if you commit to a 1-year contract vs renting day-by-day.

Three reservation options:

| Option | Payment | Discount |
|---|---|---|
| **All Upfront** | Pay full amount now | Highest discount 💰💰💰 |
| **Partial Upfront** | Pay some now, rest monthly | Medium discount 💰💰 |
| **No Upfront** | Pay monthly | Lowest discount 💰 |

**Best for:** Steady, predictable workloads (e.g., a database that runs 24/7)

---

### 📉 3. Pay Less When You Use More (Volume Discounts)

The **more you use, the less you pay per unit** — pricing tiers reward high usage.

> 💡 **Analogy:** Like buying in **bulk at a wholesale store** (Costco). The more you buy, the cheaper each item gets.

- AWS automatically applies tiered pricing as usage grows
- Also, as **AWS grows** and becomes more efficient, they pass savings on to customers (AWS has reduced prices 100+ times historically)

**Example — Amazon S3 Storage Pricing Tiers:**

```
First 50 TB/month   → $0.023 per GB
Next 450 TB/month   → $0.022 per GB   ← cheaper!
Over 500 TB/month   → $0.021 per GB   ← even cheaper!
```

---

### 📊 Three Payment Models — Comparison

| Model | Best For | Key Benefit |
|---|---|---|
| **Pay for what you use** | Variable/unpredictable workloads | Maximum flexibility |
| **Pay less when you reserve** | Steady, long-running workloads | Up to 75% savings |
| **Pay less as you use more** | High-volume usage | Automatic volume discounts |

---

## 4. AWS Services with No Charge

Some AWS services are **completely free to use** — you only pay for the underlying resources they create or manage.

> 💡 **Analogy:** These are like **free tools** in a workshop. The hammer and measuring tape are free — but the wood and nails you use with them still cost money.

| Service | What it does |
|---|---|
| **Amazon VPC** | Create a private, isolated network in the cloud |
| **AWS Elastic Beanstalk** | Deploy and manage applications automatically |
| **AWS CloudFormation** | Provision AWS resources using templates (Infrastructure as Code) |
| **AWS IAM** | Manage users, roles, and permissions |

> ⚠️ **Important:** These services themselves are free, but the **resources they provision** (EC2 instances, storage, etc.) are still charged normally.

---

