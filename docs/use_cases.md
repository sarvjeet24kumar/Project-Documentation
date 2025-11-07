#  Functional Use Case Documentation

## Use Case 1: User Registration & Login
**Role:** Student / Club Admin  
**Description:** Allows a user to create an account and login to the system.  
**Steps:**
1. User enters name, email, password, and role.
2. System validates data and stores it in the database.
3. User receives JWT token for authentication.  
**Post-condition:** User logged in and authenticated.  
**Exceptions:** Duplicate email or invalid password.

---

<!-- ## Use Case 2: Club Creation
**Role:** Club Admin  
**Description:** Allows admins to create and manage clubs.  
**Steps:**
1. Admin enters club name and description.
2. System stores club details in DB.
3. Club visible to students for joining.  
**Post-condition:** Club created successfully.  
**Exceptions:** Missing details or unauthorized user.

--- -->

## Use Case 2: Event Management
**Role:** Club Admin  
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

## Use Case 4: Event Viewing & Filtering
**Role:** Student  
**Description:** Students view available events and filter by category or club.  
**Steps:**
1. User applies filters on date or club.
2. System displays matching events.  
**Post-condition:** Filtered event list displayed.  
**Exceptions:** No events found.
