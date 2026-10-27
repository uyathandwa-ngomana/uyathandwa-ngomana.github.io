
# User Stories and Tasks — Evidence

[← Back to portfolio](../README.md) · [Reflection](reflection.md)

| | |
|---|---|
| **Student** | Uyathandwa Ngomana (231173229) |
| **Module** | Project Presentation 3 (PRP372S) |
| **Projects** | CommunityPulse AI · ProKonecta |

**Source:** Project requirements, application functionality, development activities, and testing and debugging work.

This document identifies user needs, acceptance criteria (AC), and development tasks (T). Each user story describes a feature from the perspective of the person who will use it. Acceptance criteria define the expected system behaviour, while tasks describe the activities needed to implement, review, or test that behaviour.

# Epic A — CommunityPulse AI

CommunityPulse AI is included as a separate project in which my contribution focused on development and testing.

## US-01 — Application functionality

**As a** user, **I want** to access the application's main features, **so that** I can use the system for its intended purpose.

**Acceptance criteria**

- AC1: The application starts and its main interface can be accessed.
- AC2: Available features respond to the relevant user actions.
- AC3: Invalid inputs and unsuccessful operations are handled appropriately.
- AC4: Unexpected behaviour can be identified and reported.
- AC5: The application provides appropriate feedback when an operation succeeds or fails.

**Tasks**

- T1.1 Review the application's purpose and existing functionality.
- T1.2 Identify the features included in the assigned development work.
- T1.3 Contribute to the assigned development activities.
- T1.4 Run the application and test relevant screens.
- T1.5 Record unexpected behaviour and report identified issues.

## US-02 — Application testing

**As a** project team member, **I want** to test the available application features, **so that** I can identify defects and help improve the application's reliability.

**Acceptance criteria**

- AC1: Selected features are tested using relevant inputs and actions.
- AC2: Expected results are compared with actual results.
- AC3: Failed checks are documented.
- AC4: Identified issues are communicated to the relevant team members.
- AC5: Affected features are retested after fixes where possible.

**Tasks**

- T2.1 Identify the functionality to be tested.
- T2.2 Prepare basic test scenarios.
- T2.3 Execute the test scenarios.
- T2.4 Record successful and unsuccessful results.
- T2.5 Report defects and retest relevant fixes.

---

# Epic B — Customer Accounts and Authentication

ProKonecta is a marketplace intended to connect customers with service professionals in Zimbabwe.

## US-03 — Customer registration

**As a** new customer, **I want** to create a ProKonecta account, **so that** I can access marketplace features that require registration.

**Acceptance criteria**

- AC1: The registration form accepts the required information.
- AC2: Required fields are validated before an account is created.
- AC3: Incomplete or invalid information is handled appropriately.
- AC4: Successful registration creates an account in the system.
- AC5: The user receives suitable feedback if registration succeeds or fails.

**Tasks**

- T3.1 Review the registration form and required fields.
- T3.2 Review the registration API endpoint.
- T3.3 Check input validation and account-creation logic.
- T3.4 Test registration with valid information.
- T3.5 Test invalid submissions and investigate errors.

## US-04 — Secure sign-in and logout

**As a** registered user, **I want** to sign in and log out securely, **so that** I can access my account and protect it when I finish using the platform.

**Acceptance criteria**

- AC1: Users can sign in with valid credentials.
- AC2: Invalid credentials do not grant access.
- AC3: Protected features require an appropriate authenticated session.
- AC4: Access to role-specific features follows the user's permissions.
- AC5: Logging out ends the relevant session.
- AC6: Authentication failures are handled without exposing sensitive information.

**Tasks**

- T4.1 Review sign-in and session-management logic.
- T4.2 Test successful and unsuccessful sign-in attempts.
- T4.3 Review access controls for protected endpoints.
- T4.4 Test logout behaviour.
- T4.5 Investigate authentication errors and retest fixes.

## US-05 — Account verification

**As a** user, **I want** to complete the required account-verification process, **so that** the system can confirm the relevant contact information before allowing the associated action.

**Acceptance criteria**

- AC1: The user can initiate the required verification process.
- AC2: Verification codes are handled through the configured delivery method.
- AC3: Valid codes are accepted according to the verification rules.
- AC4: Invalid or expired codes are rejected.
- AC5: Delivery or verification failures are handled appropriately.
- AC6: Verification status changes only when the required checks succeed.

**Tasks**

- T5.1 Review the verification workflow.
- T5.2 Check the code-generation and verification endpoints.
- T5.3 Review the configured email or SMS integration.
- T5.4 Test the workflow where the required configuration is available.
- T5.5 Investigate delivery failures and document remaining issues.

---

# Epic C — Customer Service Requests

## US-06 — Create a service request

**As a** customer, **I want** to describe the service I need and submit a request, **so that** suitable professionals can respond to my requirements.

**Acceptance criteria**

- AC1: The customer can enter the required service-request details.
- AC2: Required fields are validated before submission.
- AC3: A valid request is processed by the backend.
- AC4: The request is saved and associated with the correct customer.
- AC5: The interface confirms success only when the request is successfully created.
- AC6: Failed submissions produce appropriate feedback.

**Tasks**

- T6.1 Review the service-request form and required fields.
- T6.2 Review the request-creation API endpoint.
- T6.3 Check request validation and database-persistence logic.
- T6.4 Test valid and invalid submissions.
- T6.5 Investigate backend errors affecting request creation.
- T6.6 Verify that saved requests can be retrieved where supported.

## US-07 — View service requests

**As a** customer, **I want** to view the service requests associated with my account, **so that** I can keep track of the services I have requested.

**Acceptance criteria**

- AC1: The system retrieves requests associated with the authenticated customer.
- AC2: Request details are displayed using the information returned by the backend.
- AC3: Empty request lists are handled appropriately.
- AC4: Loading and error states provide clear feedback.
- AC5: Customers cannot access private requests belonging to unrelated users.

**Tasks**

- T7.1 Review the request-listing functionality.
- T7.2 Check the API endpoint used to retrieve requests.
- T7.3 Test the display of existing requests.
- T7.4 Check empty-list and error states.
- T7.5 Review access controls and investigate retrieval errors.

## US-08 — Receive request notifications

**As a** customer, **I want** to receive confirmation when I submit a service request, **so that** I know whether the operation was successful.

**Acceptance criteria**

- AC1: The interface provides feedback after submission.
- AC2: Confirmation is based on the actual outcome of the request operation.
- AC3: A notification failure does not incorrectly imply that a successfully saved request was lost.
- AC4: Failed operations are reported without misleading the customer.

**Tasks**

- T8.1 Review request-submission feedback.
- T8.2 Check how request activity triggers notifications.
- T8.3 Test the confirmation shown after submission.
- T8.4 Investigate notification and request-status inconsistencies.
- T8.5 Verify the request outcome separately from notification delivery.

---

# Epic D — Finding and Saving Professionals

## US-09 — Browse the professional directory

**As a** customer, **I want** to browse available service professionals, **so that** I can identify providers who may be suitable for my needs.

**Acceptance criteria**

- AC1: The directory retrieves available professional information.
- AC2: Provider information is displayed clearly.
- AC3: Empty results are handled appropriately.
- AC4: Failed data retrieval does not appear as a successful result.
- AC5: The directory provides suitable feedback when loading fails.

**Tasks**

- T9.1 Review the professional-directory interface.
- T9.2 Check the endpoint used to retrieve professionals.
- T9.3 Test directory loading and display.
- T9.4 Check empty-result and error handling.
- T9.5 Investigate frontend and backend integration issues.

## US-10 — Search for professionals

**As a** customer, **I want** to search for professionals using the available search criteria, **so that** I can narrow the results to providers who may meet my requirements.

**Acceptance criteria**

- AC1: The customer can use the search options provided by the application.
- AC2: Search criteria are processed by the system.
- AC3: Results reflect the criteria supported by the application.
- AC4: The system handles searches that return no results.
- AC5: Search failures are communicated appropriately.

**Tasks**

- T10.1 Identify the search options supported by the application.
- T10.2 Review the provider-search endpoint.
- T10.3 Test searches using available criteria.
- T10.4 Check the handling of empty search results.
- T10.5 Investigate incorrect results or failed searches.

## US-11 — Save preferred professionals

**As a** customer, **I want** to save professionals I may want to contact later, **so that** I can find them again without repeating my search.

**Acceptance criteria**

- AC1: An authenticated customer can save a professional where the feature is available.
- AC2: The saved record is associated with the correct customer and professional.
- AC3: The customer can retrieve their saved-professionals list.
- AC4: Failed save or retrieval operations are handled appropriately.
- AC5: The interface does not display a successful save when the backend operation fails.
- AC6: Customers cannot retrieve another user's private saved list.

**Tasks**

- T11.1 Review the saved-professionals functionality.
- T11.2 Check how save operations are sent to the backend.
- T11.3 Review the data-storage and retrieval logic.
- T11.4 Test saving a professional.
- T11.5 Test loading the saved-professionals list.
- T11.6 Investigate backend errors and retest relevant fixes.

---

# Epic E — Profiles and Professional Verification

## US-12 — Update profile information

**As a** registered user, **I want** to update my profile details, **so that** my account information remains accurate when I use the marketplace.

**Acceptance criteria**

- AC1: The user can access the profile information available for editing.
- AC2: Submitted information is validated.
- AC3: Updates are associated with the authenticated user's account.
- AC4: Valid changes are saved successfully.
- AC5: Updated details are displayed or returned after saving.
- AC6: Failed database operations do not produce false success messages.
- AC7: Users cannot update another person's private profile without permission.

**Tasks**

- T12.1 Review the profile form and editable fields.
- T12.2 Check how profile information is sent to the backend.
- T12.3 Review the profile-update endpoint and database query.
- T12.4 Test saving valid changes.
- T12.5 Investigate errors affecting profile updates.
- T12.6 Retrieve the profile again to verify persistence after an update.

## US-13 — Professional verification

**As a** service professional, **I want** to submit the required verification information, **so that** my application can be reviewed before I am represented as a verified provider.

**Acceptance criteria**

- AC1: The professional can access the verification process available to their account.
- AC2: Required verification information is validated.
- AC3: Submitted information is associated with the correct professional.
- AC4: The system records the appropriate verification status.
- AC5: A pending application is not incorrectly displayed as approved.
- AC6: Verification information is accessible only to authorised users.

**Tasks**

- T13.1 Review the professional-verification workflow.
- T13.2 Identify the information and documents required.
- T13.3 Check the related backend routes and data model.
- T13.4 Review how verification status is stored and displayed.
- T13.5 Test available verification scenarios using authorised test data.
- T13.6 Document any outstanding verification issues.

---

# Epic F — Quotes, Chat and Jobs

## US-14 — Submit and view quotes

**As a** customer, **I want** to receive and compare quotes from professionals, **so that** I can consider available offers before choosing a provider.

**Acceptance criteria**

- AC1: An eligible professional can submit a quote for a relevant service request.
- AC2: Quote information is validated before submission.
- AC3: A quote is associated with the correct request and professional.
- AC4: The customer can retrieve quotes associated with their request.
- AC5: Quote details are displayed clearly.
- AC6: Empty quote lists and failed operations are handled appropriately.

**Tasks**

- T14.1 Review the quote-submission and retrieval workflows.
- T14.2 Check the required quote fields and API endpoints.
- T14.3 Review the relationship between quotes, requests and professionals.
- T14.4 Test quote submission where the functionality is available.
- T14.5 Test quote retrieval and display.
- T14.6 Investigate quote-related backend errors.

## US-15 — Communicate through chat

**As a** customer or professional, **I want** to communicate through the platform, **so that** I can clarify service requirements before proceeding with a job.

**Acceptance criteria**

- AC1: Authorised participants can access the relevant conversation.
- AC2: Messages are associated with the correct sender and conversation.
- AC3: The interface provides feedback when messages are sent or fail.
- AC4: Conversation history is retrieved from the appropriate source.
- AC5: Unauthorised users cannot access private conversations.

**Tasks**

- T15.1 Review the chat interface and related backend routes.
- T15.2 Check how messages are submitted and retrieved.
- T15.3 Test sending and loading messages.
- T15.4 Review conversation access permissions.
- T15.5 Investigate messaging errors and retest relevant fixes.

## US-16 — View jobs and service progress

**As a** customer or professional, **I want** to view the jobs associated with my account, **so that** I can keep track of relevant service arrangements.

**Acceptance criteria**

- AC1: The system retrieves jobs associated with the authorised user.
- AC2: Available job details and statuses are displayed.
- AC3: Job records are linked to the relevant parties and service request.
- AC4: Empty lists and retrieval failures are handled appropriately.
- AC5: Users cannot access job information they are not authorised to view.

**Tasks**

- T16.1 Review the job-management workflow.
- T16.2 Check the relevant job-listing endpoints.
- T16.3 Test the retrieval and display of job information.
- T16.4 Check status display and data consistency.
- T16.5 Investigate job-retrieval errors.

---

# Epic G — Backend Reliability and Testing

## US-17 — Investigate and fix backend errors

**As a** development team member, **I want** to identify and fix backend errors, **so that** application features can process information reliably and provide accurate feedback.

**Acceptance criteria**

- AC1: Errors are investigated using available logs, responses and relevant code.
- AC2: The likely cause is identified using the available evidence.
- AC3: Changes address the cause rather than simply hiding the error.
- AC4: Fixes are tested against the affected functionality.
- AC5: Unresolved problems are documented accurately.
- AC6: Relevant working functionality is checked for regressions.

**Tasks**

- T17.1 Reproduce the reported error.
- T17.2 Review relevant backend logs and responses.
- T17.3 Inspect the endpoint, query and validation logic.
- T17.4 Apply a correction where the cause is understood.
- T17.5 Retest the affected endpoint and user flow.
- T17.6 Record the outcome and any remaining problems.

## US-18 — End-to-end functional testing

**As a** project team member, **I want** to test complete user flows across the interface and backend, **so that** I can identify integration issues and distinguish working features from those requiring further attention.

**Acceptance criteria**

- AC1: Selected user flows are tested from the interface to the backend.
- AC2: Actual results are compared with expected results.
- AC3: Saved information is checked for persistence where applicable.
- AC4: Failed requests and unexpected responses are documented.
- AC5: Features are classified according to observed test results.
- AC6: Affected flows are retested after relevant fixes.

**Tasks**

- T18.1 Select the main user flows to test.
- T18.2 Test sign-in and relevant account operations.
- T18.3 Test service-request submission and retrieval.
- T18.4 Test relevant directory, profile and saved-professional operations.
- T18.5 Inspect logs and API responses when a flow fails.
- T18.6 Retest affected flows after fixes.
- T18.7 Record successful checks, failures and unresolved issues.

---

# Evidence and Completion Notes

These user stories describe the expected functionality and proposed development or testing activities. The acceptance criteria should not be treated as proof that a feature has passed testing.

For the portfolio submission:

- Include screenshots, test results or code references for work actually completed.
- Distinguish my individual contribution from work completed by the wider project team.
- Mark a task as completed only when there is evidence that the work was performed.
- Record unsuccessful tests and unresolved defects separately from successful results.
- Identify features that were not tested as unverified.

---

[← Back to portfolio](../README.md) · [Reflection](reflection.md)
