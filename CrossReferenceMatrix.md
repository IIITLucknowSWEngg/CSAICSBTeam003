# Cross Reference Matrix for LinkedIn Clone Project

This matrix links the test cases with the corresponding features and requirements. It ensures that all features have been properly tested, and that test coverage aligns with the business and functional requirements of the LinkedIn clone.

---

## Purpose

The purpose of this document is to map the test cases to the features and corresponding requirements for the LinkedIn clone. This helps ensure that every requirement is covered by one or more test cases, enabling thorough testing and validation of the system.

---

## Legend

- **Test ID**: Unique identifier for each test case.
- **Feature**: The feature of the system being tested.
- **Test Case ID**: Unique identifier for each test case related to the feature.
- **Reference Requirement**: The requirement that this test case verifies or validates.
- **Test Status**: (To be updated after testing) - `Pass`, `Fail`, `Pending`, or `Not Applicable (N/A)`.

---

## Test Matrix

| **Test ID** | **Feature**              | **Test Case ID** | **Test Description**                                      | **Reference Requirement** | **Test Status** |
|-------------|--------------------------|------------------|-----------------------------------------------------------|---------------------------|-----------------|
| **TC-01**   | User Registration         | TC-1.1           | Test user registration with valid credentials.            | REQ-001: User should be able to register successfully.  | Pending          |
| **TC-02**   | User Registration         | TC-1.2           | Test duplicate username scenario during registration.     | REQ-002: The system should prevent duplicate usernames. | Pending          |
| **TC-03**   | User Login                | TC-2.1           | Test successful user login with correct credentials.      | REQ-003: User should be able to log in with valid credentials. | Pending          |
| **TC-04**   | User Login                | TC-2.2           | Test login with invalid credentials.                      | REQ-004: The system should reject invalid credentials. | Pending          |
| **TC-05**   | Profile Management        | TC-3.1           | Test updating user profile information.                   | REQ-005: Users should be able to update their profile. | Pending          |
| **TC-06**   | Profile Management        | TC-3.2           | Test profile photo upload and change.                     | REQ-006: Users should be able to upload and update their profile picture. | Pending          |
| **TC-07**   | Post Creation             | TC-4.1           | Test creating a post with valid text and image.           | REQ-007: Users should be able to create posts.        | Pending          |
| **TC-08**   | Post Creation             | TC-4.2           | Test creating a post with invalid data (empty text).      | REQ-008: The system should reject empty posts.         | Pending          |
| **TC-09**   | Post Interaction          | TC-5.1           | Test liking a post.                                       | REQ-009: Users should be able to like posts.           | Pending          |
| **TC-10**   | Post Interaction          | TC-5.2           | Test commenting on a post.                                | REQ-010: Users should be able to comment on posts.     | Pending          |
| **TC-11**   | Notifications             | TC-6.1           | Test receiving notifications for new posts.               | REQ-011: The system should send notifications for new posts. | Pending          |
| **TC-12**   | Notifications             | TC-6.2           | Test receiving notifications for new connections.         | REQ-012: The system should notify users of new connections. | Pending          |
| **TC-13**   | Search Functionality      | TC-7.1           | Test searching for users by name.                          | REQ-013: Users should be able to search for other users by name. | Pending          |
| **TC-14**   | Search Functionality      | TC-7.2           | Test searching for posts by keywords.                     | REQ-014: Users should be able to search for posts by keyword. | Pending          |
| **TC-15**   | Security                  | TC-8.1           | Test XSS prevention in user input fields.                  | REQ-015: The system should prevent XSS attacks.        | Pending          |
| **TC-16**   | Security                  | TC-8.2           | Test SQL Injection prevention in backend APIs.            | REQ-016: The system should prevent SQL injection attacks. | Pending          |

---

## Requirements Mapping

Here’s a summary of the requirements and the associated test cases:

| **Requirement ID** | **Requirement Description**                                  | **Test Case(s) Covered**                                       |
|--------------------|---------------------------------------------------------------|---------------------------------------------------------------|
| REQ-001            | Users should be able to register successfully.               | TC-1.1                                                         |
| REQ-002            | The system should prevent duplicate usernames during registration. | TC-1.2                                                         |
| REQ-003            | Users should be able to log in with valid credentials.        | TC-2.1                                                         |
| REQ-004            | The system should reject invalid login attempts.              | TC-2.2                                                         |
| REQ-005            | Users should be able to update their profile.                | TC-3.1                                                         |
| REQ-006            | Users should be able to upload and update their profile picture. | TC-3.2                                                         |
| REQ-007            | Users should be able to create posts.                         | TC-4.1                                                         |
| REQ-008            | The system should reject empty posts.                         | TC-4.2                                                         |
| REQ-009            | Users should be able to like posts.                           | TC-5.1                                                         |
| REQ-010            | Users should be able to comment on posts.                     | TC-5.2                                                         |
| REQ-011            | The system should send notifications for new posts.          | TC-6.1                                                         |
| REQ-012            | The system should notify users of new connections.            | TC-6.2                                                         |
| REQ-013            | Users should be able to search for other users by name.       | TC-7.1                                                         |
| REQ-014            | Users should be able to search for posts by keyword.          | TC-7.2                                                         |
| REQ-015            | The system should prevent XSS attacks.                       | TC-8.1                                                         |
| REQ-016            | The system should prevent SQL injection attacks.             | TC-8.2                                                         |

---

## Notes

- **Test Status Updates**: This matrix should be updated as test cases are executed and their status is determined (e.g., Pass, Fail).
- **Versioning**: Make sure the test cases align with any changes in the features or requirements.
- **Continuous Updates**: As the project progresses, any new test cases or requirements should be added to this matrix.

---

## Conclusion

The Cross Reference Matrix ensures full coverage of the requirements and features in the LinkedIn clone project. By mapping the test cases to their corresponding requirements, we can validate that the application meets both functional and non-functional expectations.

