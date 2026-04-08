# 🏥 Clinic Management System — ER Diagram

This README describes the database design for a **modern clinic management system**. It models how doctors and patients interact through appointments, consultations, diagnostic tests, reports, and billing.

---

## 📌 Design Overview

The database handles:

- Doctor–patient **appointments**
- Actual **consultations (visits)**
- **Diagnostic tests** prescribed by doctors
- **Reports** generated after tests
- **Invoices and payments**
- Patient medical history tracking

---

## 🔄 Diagram Flow

The ER diagram follows the real-world lifecycle of a patient:

- **Users** → Base entity (doctor or patient)

- **Patients / Doctors** → Role-specific profiles

- **Appointments** → Booking layer (intent to visit)

- **Consultations** → Actual doctor–patient interaction

- **Prescribed Tests** → Diagnostics recommended during consultation

- **Reports** → Results generated after tests

- **Invoices** → Billing for consultation/services

- **Payments** → Transactions linked to invoices

---

## 🧱 Core Entities

- users
- patients
- doctors
- appointments
- consultations
- prescribed_tests
- reports
- invoices
- payments

---

## 🧠 Key Idea

- `users` = base identity (authentication layer)
- `patients` & `doctors` = role-based extensions
- `appointments` = scheduled intent (may not always happen)
- `consultations` = actual visit (core interaction)
- `prescribed_tests` = diagnostics tied to consultation
- `reports` = output of tests
- `invoices` = billing layer
- `payments` = financial transactions

---

## 🔗 Relationships Summary

- One **user** is either a **patient** or a **doctor**
- One **patient** can book multiple **appointments**
- One **doctor** can handle multiple **appointments**
- One **appointment** may result in **one consultation** (or none)
- One **consultation** can have multiple **prescribed tests**
- Each **test** generates a **report**
- One **consultation** generates an **invoice**
- One **invoice** can have multiple **payments**

---

## 📷 Diagram

The ER diagram image is included in this repository.

![Clinic ER Diagram](./Clinic%20Appointment%20&%20Diagnostic%20Platform.png)

---

## ⚠️ Notes / Improvements

- `specialization` in doctors can be separated into its own table for scalability
- `appointments` can include time-slot management for better scheduling
- `prescribed_tests` can be normalized with a `test_types` table
- `reports` can store structured data (PDFs, lab values, etc.)
- Add **doctor availability** for real booking systems
- Introduce **staff/lab technicians** for advanced workflows

---

## 🚀 Purpose

This design helps transition a clinic from **manual record-keeping and phone bookings** to a **structured digital system** capable of managing patients, consultations, diagnostics, and billing efficiently.

---

## 🧠 Learning Outcome

This project demonstrates:

- Clear separation between **booking (appointment)** and **actual visit (consultation)**
- Real-world **data flow design**
- Proper handling of **one-to-many relationships**
- Scalable thinking for **healthcare systems**

---

## 🏁 Final Note

This is a **clean and scalable foundation** for a clinic platform—simple enough to understand, yet structured enough to extend into a full-fledged healthcare system.
