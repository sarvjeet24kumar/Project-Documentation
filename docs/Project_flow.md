# CampusConnect — Project Flow & Specs



## Table of contents

1. [Overview](#overview)

2. [Student Flow](#student-flow)
3. [Admin Flow](#admin-flow)
4. [Homepage Flow (Before Login)](#homepage-flow-before-login)
5. [Database Schema](#database-schema)
6. [Validation Rules & Advanced Logic](#validation-rules--advanced-logic)


---

## Overview

CampusConnect is a college event management system with three roles:

- **Super Admin** — manages admin accounts.
- **Admin** — creates/manages events.
- **Student** — registers/unregisters for events and views events.

This document captures the full system flow including the updated validations you requested (no two events at same date-time & location, seats required, dynamic seat updates, delete flow, etc.).

---


## Student Flow

**Responsibilities**

- Signup, login
- View events (upcoming, past, registered)
- Register / Unregister
- Track registrations

### 1. Student Signup

- Student opens homepage → Signup
- Enter: name, email, password
- System validates email uniqueness
- Account created → redirect to login

### 2. Student Login

- Login with email + password
- System authenticates and redirects to dashboard

### 3. Student Dashboard

Dashboard shows:
- Upcoming Events
- Past Events
- Events the student has registered for
- Available seats (calculated)
- Register / Unregister actions

Per event shown:
- Title
- Date / Time
- Location
- Available seats (capacity - registered_count)
- Status: `Open` / `Full` / `Past`

### 4. Register for Event

**Validation checks (on attempt to register):**
- Event date/time must be >= today
- Seats available > 0
- Student not already registered for the event

**On success:**
- Add a row to `REGISTRATIONS` table
- Update available seats (derived: capacity - registrations)
- Redirect student to dashboard (confirmation displayed)

### 5. Unregister from Event

- Student clicks `Unregister` → confirmation popup
- On confirm: delete registration row
- Seat count adjusts automatically (derived value changes)

---

## Admin Flow

**Responsibilities**

- Create, edit, delete events
- View registered students per event
- See all events they created and system events

### Admin Login

- Admin logs in using credentials sent by Super Admin
- Admin Dashboard loads

### Admin Dashboard Sections

1. View All Events
2. View Events Created by Admin
3. Create New Event
4. Delete Event
5. View Registered Students per Event

### ADMIN: Event Creation Flow (With Validations)

**Event fields**
- Title
- Description
- Date & Time
- Location
- Number of seats (capacity)
- Created by (auto-filled)

**Critical Validations**

- **Validation 1 — No two events at same date-time & same location**
  - Before saving, check existing events where `existing_event.datetime == new_event.datetime && existing_event.location == new_event.location`.
  - If true, reject with: **"Another event is already scheduled at this location and time."**

- **Validation 2 — Number of seats required**
  - `capacity` must be integer > 0. Otherwise: **"Seat count must be positive."**

- **Validation 3 — Event date must be in the future**
  - If `event_date < today` then reject with an appropriate error message.

**On passing validations**
- Save the event record with `capacity`.
- Event appears in student and admin lists.

### ADMIN: Delete Event Flow

- Admin clicks `Delete` → confirmation requested
- If confirmed:
  - Mark event as deleted (soft-delete) or remove fully depending on policy
  - Set `deleted_by = admin.username`
  - Set `deleted_at = timestamp`
  - Remove or invalidate all `REGISTRATIONS` for that event
  - Event no longer visible on student dashboard

---

## Homepage Flow (Before Login)

Visitors see:
- Upcoming events
- Past events
- Links: Login (Student) / Login (Admin) / Signup
---

## Validation Rules 

- **Seat Handling**
  - Register: `available_seats` computed dynamically (capacity - registrations)
  - Unregister: registration removed → available seats increase
  - Event Delete: delete or mark registrations invalid

- **Event Visibility**
  - Past events: visible but cannot register
  - Upcoming events: register allowed
  - Full events: show status `FULL`
---

