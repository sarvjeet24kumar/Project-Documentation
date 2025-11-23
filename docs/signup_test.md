# Signup Module - Test Cases

| Test Case No. | Module Name | Test Scenario                               | Test Description                                          | Expected Result                                                     |
| ------------- | ----------- | ------------------------------------------- | --------------------------------------------------------- | ------------------------------------------------------------------- |
| **TC.1**      | Signup      | Signup With Valid Details                   | Provide valid username, email, and password.              | A new user account is created successfully.                         |
| **TC.2**      | Signup      | Signup With All Required Fields             | Submit all required signup fields correctly.              | User record is stored in the system.                                |
| **TC.3**      | Signup      | Signup With Strong Password                 | Use a password that meets all password rules.             | User registration is completed and password is accepted.            |
| **TC.4**      | Signup      | Signup With Unique Email                    | Register with an email that has not been used before.     | System allows user creation.                                        |
| **TC.5**      | Signup      | Signup With Proper Email Format             | Enter a correctly formatted email address.                | System accepts the email and registers user.                        |
| **TC.6**      | Signup      | Signup With Maximum Allowed Username Length | Enter a username at the upper length limit.               | Signup succeeds if within allowed length.                           |
| **TC.7**      | Signup      | Signup With Duplicate Email                 | Attempt to register using an email that already exists.   | System shows an error indicating the email is already used.         |
| **TC.8**      | Signup      | Signup Without Username                     | Try creating an account while leaving the username blank. | System prevents signup and shows required field message.            |
| **TC.9**      | Signup      | Signup With Weak Password                   | Use a password that does not meet security rules.         | System rejects the password and shows password requirement message. |
| **TC.10**     | Signup      | Signup With Invalid Email Format            | Enter an email without proper formatting.                 | System shows invalid email error.                                   |
