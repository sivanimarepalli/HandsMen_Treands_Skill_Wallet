# 🧵 HandsMen Threads: Elevating the Art of Sophistication in Men's Fashion

Welcome to the **HandsMen Threads** Salesforce Project – a modern CRM-based solution designed to streamline order processing, customer loyalty tracking, inventory management, and marketing campaigns in the men’s fashion industry.

---

## 🚀 Overview

HandsMen Threads leverages Salesforce to:

* Manage customer and product data with custom objects
* Track and automate inventory and stock levels
* Trigger email communication flows based on order status
* Monitor and update customer loyalty tiers
* Maintain campaign data for targeted marketing

This is a comprehensive hands-on project demonstrating advanced Salesforce skills, including:

* **Custom Objects & Fields**
* **Relationships (Lookup & Master-Detail)**
* **Validation Rules & Profiles**
* **Record-Triggered / Scheduled Flows**
* **Email Templates & Alerts**
* **Apex Triggers, Classes, Batch Jobs**

---

## 🧱 Key Objects

| Object                  | Description                                               |
| ----------------------- | --------------------------------------------------------- |
| `HandsMen_Customer__c`  | Manages customer data: name, email, phone, loyalty status |
| `HandsMen_Product__c`   | Catalogs items with SKU, price, and stock details         |
| `HandsMen_Order__c`     | Tracks order number, quantity, status, and amount         |
| `Inventory__c`          | Keeps real-time stock levels and warehouse data           |
| `Marketing_Campaign__c` | Organizes campaign-related data and customer mapping      |

---

## 🔁 Relationships

* **Customer → Order** (Lookup)
* **Order → Product** (Lookup)
* **Inventory → Product** (Master-Detail)
* **Campaign → Customer** (Lookup)

---

## 🛡️ Data Validation

* 🔒 **Total\_Amount\_\_c > 0** (Order)
* 🔒 **Stock\_Quantity\_\_c > 0** (Inventory)
* 🔒 **Email must contain '@gmail.com'** (Customer)

---

## ⚙️ Automations

### Record-Triggered Flows

* ✅ **Order Confirmation** – Sends email when order is confirmed
* ⚠️ **Low Stock Alert** – Sends alert when product quantity is < 5

### Scheduled Flow

* 🥇 **Loyalty Status Updater** – Updates loyalty tier daily based on purchase total

---

## 🧑‍💻 Apex Logic

### `OrderTriggerHandler.cls`

* Validates quantity based on order status (Confirmed, Pending, Rejection)

### `OrderTrigger.trigger`

* Triggers validation before insert/update

### `InventoryBatchJob.cls`

* Schedulable batch job to restock low inventory

---

## 📧 Sample Email Template – Order Confirmation

```html
<p>Dear {!Order__c.Customer__c},</p>
<p>Your order #{!Order__c.Name} has been confirmed!</p>
<p>Thank you for shopping with us.</p>
<p>Best Regards,</p>
<p>Sales Team</p>
```

---

## 📦 Project Structure

```
HandsMenThreads/
├── force-app/
│   └── main/default/
│       ├── objects/
│       ├── classes/
│       ├── triggers/
│       ├── flows/
│       └── tabs/
├── config/
├── manifest/
└── README.md
```

---

## 📄 Project Documentation
A detailed project report containing the abstract, technology stack, project phases, real-world implementation, validations, automation logic, and visuals can be found in:

📘 Documentation/HandsMen_Threads_documentation.pdf

---

## 🎓 Learning Highlights

* Real-world Salesforce data modeling
* Automation using declarative tools
* Apex development best practices
* End-to-end app building in Salesforce platform

---

## 👤 Contributor

* **Sivani Marepalli**

📂 GitHub: [HandsMen_Treands_Skill_Wallet](https://github.com/sivanimarepalli/HandsMen_Treands_Skill_Wallet)

If you like this project, give it a ⭐ and fork it to explore more!
