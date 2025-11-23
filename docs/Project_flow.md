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

- Login with username + password
- System authenticates and redirects to dashboard

### 3. Student Dashboard

Dashboard shows:

- Upcoming Events

- Past Events

- Events the student has registered for

- Register / Unregister actions

Per event shown:

- Title

- Date / Time

- Location

- Available seats 

- Status

### 4. Register for Event

**Validation checks (on attempt to register):**

- Event date/time must be >= today

- Seats available > 0

- Student not already registered for the event

**On success:**

- Add a row to REGISTRATIONS table

- Redirect student to dashboard 

### 5. Unregister from Event

- Student clicks Unregister → confirmation popup
- On confirm: delete registration row

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

### ADMIN: Delete Event Flow

- Admin clicks Delete → confirmation requested
- If confirmed:
  - Mark event as deleted (soft-delete) REGISTRATIONS for that event

  - Event no longer visible on student dashboard

---

## Homepage Flow (Before Login)

Visitors see:
- Upcoming events
- Past events
- Links: Login / Signup
---

