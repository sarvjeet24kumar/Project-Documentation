#  CampusConnect – College Event & Club Portal

##  Overview

**CampusConnect** is an innovative **EdTech web platform** designed to simplify the entire process of **college club and event management**.  
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
  - **Super Admins (optional):** Oversee all clubs, manage user roles, and handle authentication.

---

##  Stakeholders

###  Students
- Explore various college clubs and their activities.
- View detailed event descriptions, dates, and registration requirements.
- Register for events directly through the portal.
- Track participation history and receive event updates or reminders.

### Admins
- Create, edit, and manage events hosted by them.
- Handle event registrations and view participant details.
- Communicate updates and announcements to registered students.
- Analyze event participation trends for better engagement in future events.

###  (Optional) Super Admins
- Manage the entire platform’s configuration.
- Approve or suspend clubs and events.
- Monitor analytics for platform usage, event success, and student involvement.

---

##  Scope

### 1. Technology Stack
- **Backend Framework:** Django (for admin panel and backend logic)
- **API Development:** Django REST Framework (DRF)
- **Database:** PostgreSQL (for relational data storage)
- **Frontend:** HTML, CSS, Bootstrap
- **Authentication:** JWT (JSON Web Token) for secure login and access control

### 2. Core Features
- User registration and login system (JWT-based authentication)
- Event creation and management by club admins
- Event registration and tracking for students
- RESTful API endpoints to support web and mobile platforms
- Role based access permissions (Student/Admin)

---

##  Authentication System

CampusConnect uses **JWT-based authentication** to ensure a secure login and access management process:
- **Signup/Login APIs:** Allow users to authenticate using email and password.
- **Access Token:** Grants temporary access for authorized actions.
- **Refresh Token:** Generates new access tokens without re-login.
- **Role-based permissions:** Ensure that only authorized users can perform admin operations.

This mechanism enhances **data security**, prevents unauthorized actions, and makes API integration seamless across web and mobile platforms.

---

##  REST API Integration

The backend provides well-structured RESTful APIs, such as:

| Endpoint | Method | Description |
|-----------|---------|-------------|
| `/api/register/` | POST | Register a new user (student or admin) |
| `/api/login/` | POST | Authenticate user and generate JWT token |
| `/api/events/` | GET | View all available events |
| `/api/events/<id>/` | GET | Retrieve event details |
| `/api/events/create/` | POST | Create a new event (admin only) |
| `/api/events/<id>/register/` | POST | Register a student for a specific event |

These APIs can later be consumed by a **mobile app** or **React frontend** for enhanced interactivity.

---

##  Expected Outcome

By the end of this project, the CampusConnect platform will deliver the following outcomes:

### 1. For Students:
- A single portal to **explore, register, and participate** in events.
- Access to **event history**, participation records, and notifications.
- Improved engagement with college communities and clubs.

### 2. For Club Admins:
- A **streamlined system** to manage events, registrations, and attendance.
- Reduced manual workload and communication chaos.
- Improved analytics on participation trends.

### 3. For the Institution:
- Transparent and digitalized event management.
- Enhanced collaboration and participation culture.
- Possibility of extending the system to include **AI-driven event suggestions** or **mobile app integration**.

---

##  Conclusion

**CampusConnect** bridges the gap between students and college clubs by bringing all event-related activities into one digital ecosystem.  
Its modular design, secure authentication, and API-driven structure make it a **future-ready platform** capable of scaling across web and mobile environments.

