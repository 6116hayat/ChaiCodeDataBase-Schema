# 🛍️ Instagram Store Database ER Diagram

This README describes the database design shown in **IgStoreDBdesign.png**. It models an Instagram-based store selling **thrifted** and **handmade** products, helping transition from manual DM orders to a structured system.

---

## 📌 Design Overview

The database handles:

- Unique **thrifted items** (single piece)
- **Handmade products** (multiple units/batch-based)
- Customer orders, payments, and delivery tracking

---

## 🔄 Diagram Flow

The ER diagram follows the lifecycle of a purchase:

- **Customers** → Stores buyer details
- **Orders** → Created by customers
- **Order Items** → Connects orders with products (items + quantity + price)
- **Products** → Main catalog
  - **Thrifted Products** → One-of-a-kind items
  - **Handmade Products** → Batch-produced items

- **Payments** → Tracks payment status
- **Shipping** → Tracks delivery status

---

## 🧱 Core Entities

- customers
- orders
- order_items
- products
- thrifted_products
- handmade_products
- payments
- shipping

---

## 🧠 Key Idea

- `orders` = one purchase
- `order_items` = items inside an order
- `products` = base entity
- `thrifted` & `handmade` = specialized subtypes

---

## 📷 Diagram

The ER diagram image (**IgStoreDBdesign.png**) is included in the root of this repository.

![Instagram Store Database ER Diagram](./Instagram%20Thrift%20Creator%20Store.png)

---
