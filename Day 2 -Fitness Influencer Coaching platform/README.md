# 🏋️‍♂️ Online Fitness Coaching Platform — ER Diagram

This README describes the database design for an **online fitness coaching platform**. It models how trainers/influencers manage clients, sell coaching plans, schedule sessions, track progress, and handle subscriptions & payments.

---

## 📌 Design Overview

The database handles:

- Trainer-led **coaching programs**
- Client **subscriptions** and renewals
- **Consultation sessions** (calls/meetings)
- **Progress tracking** (fitness metrics)
- **Payments** and transaction records
- Optional **diet plans** linked to programs

---

## 🔄 Diagram Flow

The ER diagram follows the lifecycle of a client:

- **Users** → Base entity (trainer or customer)

- **Customers / Trainers** → Role-specific profiles

- **Plans** → Created by trainers

- **Subscriptions** → Clients enroll in plans

- **Payments** → Linked to subscriptions

- **Sessions** → Scheduled interactions between trainer & client

- **Activity** → Type of session (yoga, cardio, etc.)

- **Progress** → Client fitness tracking over time

- **Trainer Notes** → Feedback from trainer

- **Diet Plan** → Optional nutrition plans tied to programs

---

## 🧱 Core Entities

- users
- customers
- trainer
- plan
- subscriptions
- payment
- sessions
- activity
- progress
- trainer_notes
- diet_plan

---

## 🧠 Key Idea

- `users` = base identity (trainer or customer)
- `customers` & `trainer` = role-based extensions
- `plan` = what trainers sell
- `subscriptions` = who bought what & for how long
- `sessions` = interactions (calls/consultations)
- `progress` = fitness tracking (time-based data)
- `trainer_notes` = feedback layer

---

## 🔗 Relationships Summary

- One **user** is either a **customer** or a **trainer**
- One **trainer** can create multiple **plans**
- One **customer** can have multiple **subscriptions**
- One **plan** can be subscribed to by many customers
- One **subscription** can have multiple **payments**
- Trainers and customers connect via **sessions**
- Customers log **progress updates**
- Trainers provide feedback via **trainer notes**
- Plans can include associated **diet plans**

---

## 📷 Diagram

The ER diagram image is included in this repository.

![Online Fitness Coaching ER Diagram](./Ftiness%20Influencer%20Coaching%20platform.png)

---

## ⚠️ Notes / Improvements

- `progress` currently combines check-ins and metrics (can be split into `checkins` + `progress_logs`)
- `trainer_notes` can be linked to sessions or progress for better context
- `diet_plan` can be extended for detailed meal structures
- Workout plans can be added for more depth

---

## 🚀 Purpose

This design helps transition from **manual coaching via DMs and calls** to a **structured, scalable platform** capable of managing multiple clients and programs efficiently.
