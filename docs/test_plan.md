# **Test Plan – Signup & Login Module**

## **1. Introduction**
This test plan outlines the validation strategy for the Signup and Login modules to ensure correct user registration, authentication, and error handling.

---

## **2. Scope of Testing**
**In Scope:** Signup and Login functionality, input validation, session creation.  
**Out of Scope:** API testing, admin modules.

---

## **3. Test Objectives**
- Verify successful user signup with valid data.
- Ensure duplicate email and invalid data are rejected.
- Validate login with correct credentials.
- Confirm proper error messages for invalid login attempts.

---

## **4. Testing Approach**
- **Type:** Manual functional testing.  
- **Method:** Execute unit-level test cases for form validation and authentication.

---

## **5. Test Environment**
- Django Local Server: `http://127.0.0.1:8000/`  
- Database: PostgreSQL  
- Browser: Chrome / Firefox

---

## **6. Test Schedule**
- Test Case Design: 13/11  
- Test Execution: 

---

## **7. Resources**
- **Test Engineer:** Sarvjeet – Executes tests, reports defects.
- **Developer:** Backend support for bug fixes.

---

## **8. Risks & Mitigation**
- **Risk:** Incorrect test data. **Mitigation:** Use clean test DB.
- **Risk:** Browser inconsistency. **Mitigation:** Multi-browser checks.

---

## **9. Deliverables**
- Signup Test Cases (TC.1 – TC.12)  
- Login Test Cases (TC.13 – TC.24)  
- Defect Report

---

## **10. Entry & Exit Criteria**
**Entry:** Code ready, environment stable.  
**Exit:** 95% test cases passed, no major defects.

