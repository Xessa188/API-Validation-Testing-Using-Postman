# API-Validation-Testing-Using-Postman

[🔗 Click here to view the Test Case Spreadsheet](https://docs.google.com/spreadsheets/d/1k-OshvCpR_W7DyKaEJ8WNNAvQfrQQ3uSAbAM85zxc-8/edit?gid=0#gid=0)

## What is this project?
This project demonstrates end-to-end API testing and bug tracking workflows. Using Postman, I performed functional integration testing on backend services handling product kits and delivery calculations. When tests failed, I documented the errors and mapped them directly to Atlassian Jira issue logs to simulate a real-world software development lifecycle (SDLC) environment.

## Skills & Tools Used:
* **API Testing Tools:** Sent targeted REST API requests using Postman to verify backend data handling.
* **Multi-Format Payloads:** Drafted and validated both JSON objects and XML input schemas.
* **Edge-Case Isolation:** Targeted structural boundaries—testing empty arrays, negative numbers, bad string types, and character injections.
* **Defect Lifecycle Management:** Linked failing test scripts to specific Jira tickets for streamlined debugging and tracking.

## Test Scenarios Covered:
1. **Kit Management Endpoint (`POST /api/v1/kits/:id/products`):** Tested product quantities and boundary limits (e.g., verifying limits when adding up to 30 items or handling alphanumeric injections on strictly integer parameters).
2. **Delivery Calculator Endpoint (`POST /calculate-delivery.xml`):** Validated conditional parameters—like operational time boundaries, weight allowances, and handling missing payload tags.
3. **Error Catching:** Isolated hidden system bugs where invalid customer actions triggered unhandled `500 Internal Server Errors` (server crashes) instead of clean client errors.
