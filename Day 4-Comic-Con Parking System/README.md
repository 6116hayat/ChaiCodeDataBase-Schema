# 🅿️ Comic-Con Parking Management System — ER Diagram

This README describes the database design for a multi-zone parking management system used during large-scale events like Comic-Con India. It models how vehicles enter, get assigned parking spots, use reserved access, and complete sessions with payments.

---

## 📌 Design Overview

The database handles:

- Vehicle entry and exit tracking
- Multiple vehicle categories (bike, car, SUV, EV, cab)
- Smart parking spot allocation
- Zone and level-based parking structure
- Reserved parking for VIPs, staff, exhibitors, cosplayers
- Parking sessions (entry → exit lifecycle)
- Ticket generation
- Payment and pricing calculation
- Real-time parking availability tracking

---

## 🔄 Diagram Flow

The ER diagram follows the real-world lifecycle of a patient:

### **Vehicle → Entry → Spot Allocation → Session → Exit → Payment**

- **Vehicles** → Identifies incoming vehicles
- **Parking Zones/Spots** → Physical parking structure
- **Access Categories** → Defines special permissions
- **Parking Session** → Tracks entry and exit
- **Parking Ticket** → Issued at entry
- **Payment** → Completed at exit

---

## 🧱 Core Entities

- vehicles
- vehicle_category
- parking_zone
- parking_spot
- parking_spot_category
- access_category
- reserved_spot
- parking_session
- parking_ticket
- payments
- pricing_rule

---

## 🧠 Key Idea

- `vehicles` = actual entities entering the venue
- `vehicle_category` = defines type & compatibility
- `parking_zone` = physical grouping (zones & levels)
- `parking_spot` = actual parking unit
- `parking_spot_category` = defines which vehicle fits
- `access_category` = special permissions (VIP, staff, etc.)
- `reserved_spot` = links spots to access restrictions
- `parking_session` = core lifecycle (entry → exit)
- `parking_ticket` = issued at entry for tracking
- `payments` = handles transaction per session
- `pricing_rule` = defines how charges are calculated

---

## 🔗 Relationships Summary

- One vehicle belongs to one vehicle category

- One vehicle can have multiple parking sessions

- One parking zone contains multiple parking spots

- One parking spot category maps to multiple parking spots

- One parking spot can be used across multiple sessions

- One access category can apply to many sessions

- One access category can reserve multiple parking spots

- One parking session is linked to one parking ticket

- One parking session results in one payment

- Pricing rules are defined based on vehicle type and spot type

---

## 📷 Diagram

The ER diagram image is included in this repository.

![Clinic ER Diagram](./ComicCon%20Parking%20System.png)

---

## ⚠️ Notes / Improvements

Parking availability can be dynamically calculated using active sessions (exit_time IS NULL)

Reserved spots can be extended with time-based rules

Pricing rules can include surge pricing for peak hours

EV charging sessions can be tracked separately for advanced systems

Add entry/exit gates for more realistic modeling

Introduce staff/admin roles for operational control

Ticket system can support QR/barcode scanning

---

## 🚀 Purpose

This design helps manage high-volume parking during large events, replacing manual allocation with a structured, scalable system capable of handling thousands of vehicles efficiently.

---

## 🧠 Learning Outcome

This project demonstrates:

Real-world event-based system design

Handling of time-based entities (sessions)

Separation of infrastructure and activity layers

Proper use of one-to-many relationships

Scalable modeling for dynamic environments

---

## 🏁 Final Note

This is a clean and scalable foundation for an event parking system—simple enough to understand, yet flexible enough to handle real-world complexity like reserved access, multi-zone layouts, and dynamic pricing.
