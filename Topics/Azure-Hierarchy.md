# ☁️ Azure Hierarchy Guide (Management Group → Subscription → Resource Group → Resources)

---

## 🎯 Overview

This guide explains the **Azure account structure (hierarchy)**:

- Management Group  
- Subscription  
- Resource Group  
- Resources  

👉 Understanding this hierarchy is key to working with Azure.

---

## 🧠 Azure Hierarchy (Top → Bottom)

```
Management Group
    ↓
Subscription
    ↓
Resource Group
    ↓
Resources
```

---

## 🔹 1️⃣ Management Group

### 📌 What is it?

Top-level container to manage **multiple subscriptions**

---

### 📌 Why use it?

- Apply policies across subscriptions  
- Centralized governance  
- Access control at scale  

---

### 📌 Example

```
Company
 ├── Dev Subscription
 ├── Prod Subscription
```

---

## 🔹 2️⃣ Subscription

### 📌 What is it?

- A **billing boundary**  
- Logical container for resources  

---

### 📌 Key Points

- Each subscription has its own billing  
- Limits and quotas are applied here  
- Resources live inside subscriptions  

---

### 📌 Example

```
Subscription: Dev
Subscription: Production
```

---

## 🔹 3️⃣ Resource Group

### 📌 What is it?

A container that holds **related resources**

---

### 📌 Why use it?

- Organize resources by project  
- Apply permissions  
- Easy deletion  

---

### 📌 Example

```
Resource Group: Project-A
 ├── VM
 ├── Storage
 ├── Database
```

---

## 🔹 4️⃣ Resources

### 📌 What are they?

Actual Azure services:

- Virtual Machine (VM)  
- Storage Account  
- Database  
- Load Balancer  

---

## 🔄 Full Example

```
Management Group: Company
    ↓
Subscription: Production
    ↓
Resource Group: E-commerce-App
    ↓
Resources:
    - VM
    - Storage
    - Database
```

---

## 🧠 Simple Analogy

| Azure | Real World |
|------|------------|
| Management Group | Company |
| Subscription | Department |
| Resource Group | Project |
| Resources | Tools |

---

## 🔐 Access Control (RBAC)

- Permissions can be applied at any level  
- Inherited downwards  

Example:

```
Management Group → Applies to all subscriptions below
```

---

## ⚡ Key Concepts

- Everything exists inside a **Subscription**  
- Resource Groups help organize resources  
- Management Groups help manage multiple subscriptions  
- Resources are the actual services  

---

## ❌ Common Mistakes

- Creating everything in one Resource Group  
- Not using Management Groups for large setups  
- Confusing Subscription with Resource Group  

---

## 🎯 One-Line Summary

👉 Azure uses a hierarchy to organize, manage, and control access to resources.

---

## 💡 Memory Trick

MG → Sub → RG → Resource

---
