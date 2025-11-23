#  Functional Use Case Documentation

## Use Case 1: User Registration & Login
**Role:** Student  
**Description:** Allows a user to create an account and login to the system.  
**Steps:**

1. User enters name, email And  password.

2. System validates data and stores it in the database.

3. User receives JWT token for authentication.  

**Post-condition:** User logged in and authenticated.  

**Exceptions:** Duplicate email or invalid password.

---

## Use Case 2: Event Management
**Role:** Admin  
**Description:** Admins create, edit, and delete events.  
**Steps:**

1. Admin provides event title, date, and location.

2. Event linked to specific club.

3. System stores event details in database.  

**Post-condition:** Event available for student registration.  
**Exceptions:** Invalid data or unauthorized access.

---

## Use Case 3: Event Registration
**Role:** Student  
**Description:** Students register for an event.  
**Steps:**

1. Student selects an event.

2. System checks for duplicates.

3. Registration stored in database. 

**Post-condition:** Registration confirmed.  
**Exceptions:** Already registered or event full.

---
