# ☁️ Basics of Cloud Computing

---

## 1. What is a Server?

A **server** is a computer that provides data or services to other computers over a network.

> 💡 **Simple Analogy:** Think of a server like a **waiter** in a restaurant. You (the client) place an order (request), and the waiter (server) brings your food (data/service) back to you.

### How it works:
- A **client** sends a **request** → the **server** sends back a **response**

### Server Hardware vs Desktop Hardware

| Feature | Server | Desktop |
|---|---|---|
| Memory | More RAM, multiple CPUs | Standard |
| Power | Redundant power supplies | Single supply |
| Network | Redundant network interfaces | Single NIC |
| Form Factor | Smaller, rack-mounted | Tower/laptop |

### Examples of servers:
- Web servers (e.g., Apache, Nginx)
- Database servers (e.g., MySQL, PostgreSQL)
- File servers
- Mail servers

---

## 2. Where Does a Server Reside?

Servers reside in a **Data Center**.

> 💡 **Simple Analogy:** A data center is like a **huge, secure library** that stores all of an organization's "books" (data). It has librarians (staff), backup lights (UPS), air conditioning (cooling), and strict security — all to make sure the books are always accessible and safe.

### A Data Center hosts:

```
Data Center
├── 🖥️  Servers
├── 💾  Storage Devices
├── 🌐  Network Devices
│       ├── Routers
│       ├── Switches
│       └── Hubs
├── ❄️  Cooling Equipment
└── 🔋  Uninterruptable Power Supplies (UPS)
```

---

## 3. What is a Virtual Machine (VM)?

A **Virtual Machine (VM)** is a **software-based computer** that runs on top of a physical computer.

> 💡 **Simple Analogy:** Imagine a **single apartment building** (physical computer). Each **apartment** (VM) is independent — it has its own furniture, rules, and tenants (OS and apps). The **building manager** (hypervisor) controls access to shared resources like water and electricity (CPU, memory, disk, network).

### Key Components:

```
Physical Computer (Host)
└── Hypervisor (software layer)
    ├── VM 1 → OS + App A
    ├── VM 2 → OS + App B
    └── VM 3 → OS + App C
```

- **Host** — the physical machine running the VMs
- **Hypervisor** — the software that manages and allocates physical resources to each VM
- **VM** — runs its own OS and interacts with the host through the hypervisor

### Why Virtualization?
- Run **multiple VMs** on a single physical machine
- Each VM is **isolated** — crash in one doesn't affect others
- More **efficient** use of hardware

---

## 4. VMs in the Cloud

> VMs are the **fundamental unit of computing** in the cloud.

### Benefits of Cloud VMs:

| Benefit | What it means |
|---|---|
| ✅ Self-service | Spin up or shut down VMs anytime, on demand |
| 💰 Pay-as-you-go | Only pay for what you actually use |
| 📈 Scalability | Instantly scale up or down based on demand |

> 💡 **AWS Example:** In the AWS Cloud, the core service for computing with VMs is **Amazon Elastic Compute Cloud (Amazon EC2)**.

---

## 5. How Software is Developed — SDLC

The **Software Development Life Cycle (SDLC)** is a structured process for building software.

> 💡 **Simple Analogy:** Think of building a **house**. You first plan what you want, design the blueprint, construct it, inspect it, move in, and then do maintenance. SDLC works the same way for software!

### The 7 Phases:

```
Plan → Analyze → Design → Develop → Test → Implement → Maintain
```

| Phase | Key Question | House Analogy 🏠 |
|---|---|---|
| **Plan** | What is the problem? What resources do you need? | Deciding you need a house & budgeting |
| **Analyze** | What do you want from the solution? | Listing your requirements (3 bedrooms, garden, etc.) |
| **Design** | How will you build it? | Creating the architectural blueprint |
| **Develop** | Build what you designed | Actually constructing the house |
| **Test** | Did you get what you wanted? | Inspecting the house before moving in |
| **Implement** | Start using what you built | Moving into the house |
| **Maintain** | Improve what you built | Repainting, repairing, renovating over time |

---

*Notes based on AWS Cloud Foundations curriculum.*
