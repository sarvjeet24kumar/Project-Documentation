#  CampusConnect – College Event Portal

##  Overview

**CampusConnect** is an innovative **Web Platform** designed to simplify the entire process of **college event management**.  
It serves as a **central hub** for students and  faculty to participate in college activities.

The platform enables:

- **Students** to explore and register for events across multiple events.

- **Admins** to create, update, and manage their  events easily.

---

##  Key Goals

### 1. Centralize All Campus Event Information
- All upcoming, ongoing, and past events are stored in a **single portal**.  
- Students can browse through events by eliminating the need for multiple WhatsApp groups, posters, or manual announcements.
- This helps in **organizing college activities efficiently** and improves visibility across departments.


### 2. Enable Role-Based Functionality
- The system defines clear **roles and permissions**:
  - **Students:** Can view, register, and participate in events.
  - **Admins:** Can create, edit, or delete events.

---

##  Stakeholders

###  Students
- Explore various college events.
- View detailed event descriptions and  dates.
- Register for events directly through the portal.

### Admins
- Create, edit, and manage events hosted by them.
- Handle event registrations and view participant details.
---

##  Scope

### 1. Technology Stack
- **Backend Framework:** Django (for admin panel and backend logic)
- **API Development:** Django REST Framework (DRF)
- **Database:** PostgreSQL (for relational data storage)
- **Frontend:** React
- **Authentication:** JWT (JSON Web Token) for secure login and access control

### 2. Core Features
- User registration and login system (JWT-based authentication)
- Event creation and management by admins
- Event registration and tracking for students
- RESTful API endpoints to support web and mobile platforms
- Role based access permissions (Student/Admin)

---

##  Authentication System

CampusConnect uses **JWT-based authentication** to ensure a secure login and access management process:

- **Signup/Login APIs:** Allow users to authenticate using username and password.

- **Access Token:** Grants temporary access for authorized actions.

- **Refresh Token:** Generates new access tokens without re-login.

- **Role-based permissions:** Ensure that only authorized users can perform admin operations.

This mechanism enhances **data security**, prevents unauthorized actions, and makes API integration seamless across web and mobile platforms.

---

##  Expected Outcome

By the end of this project, the CampusConnect platform will deliver the following outcomes:

### 1. For Students:
- A single portal to **explore, register, and participate** in events.
- Improved engagement with college communities .

### 2. For  Admins:
- A **streamlined system** to manage events, registrations, and attendance.
- Reduced manual workload and communication gap.

### 3. For the Institution:
- Transparent and digitalized event management.
- Enhanced collaboration and participation culture.


---

##  Conclusion

**CampusConnect** bridges the gap between students and college  by bringing all event-related activities into one digital ecosystem.  