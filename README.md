**DESCRIPTION**

This project contains a comprehensive API test suite for the Restful Booker application with Postman and automated using Newman. 



**OBJECTIVE**

This project validates the core functionality of the Restful Booker API in Postman, covering;

* Authentication Flow
* Booking lifecycle - Create, Retrieve, Update, Delete (CRUD)
* Negative handling (Error handling)
* Edge cases and boundary conditions
* Mock server testing using Postman's mock server feature.



**TOOLS USED**

 * Postman
 * Postman Collection Runner
 * Restful Booker API
 * JavaScript (Postman test scripts)
 * Newman
 * Node.js
 * Notebook



**SETUP INSTRUCTIONS**

1. Import Collection

   * Open Postman
   * Click "**Import"**
   * Select the collection file from `/postman/collection.json`


**EXPECTED RESULTS**

 * All requests return correct status code.
 * Authentication returns a valid token.
 * Booking ID is created and reused across requests.
 * Response time is under 500ms.
 * No hardcorded values, uses environment variables.
 * Newman summary shows 0 failure.


**TEST COVERAGE**


