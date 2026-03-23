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
   * Select the collection file: `collections/Restful-Booker-Tests.postman_collection.json`
     
2. Import Environment
   
   * Click **Environment**
   * Import `environments/Restful-Booker-Env.postman_environment.json`
  
3. Select Environment

   * Choose `Restful-Booker-Env` from the dropdown
  
**Base Url**
  
  Variable - baseUrl
  
  Value - `https://restful-booker.herokuapp.com`

  **HOW TO RUN API TESTS**

1. Open the collection in Postman
2. Click **Run** (Collection Runner)
3. Select **Restful-Booker-Env as the environment**
4. Set Iterations to 2
5. Click **Run Restful-Booker-Tests**

**FOR MOCK SERVER SETUP**

1. Identify required API endpoints
2. Define API Responses
3. Create mock collection
4. Add mock requests
5. Create mock server
7. Add mockUrl environment variable

   Variable - mockUrl
   
   Value - `https://abcd1234.mock.pstmn.io`
9. Switch between mock and live API

   Variable - apiUrl
   
   Value - {{mockUrl}}
10. Run full test collection


**NEWMAN API TESTING**

1. Install Node.js
   * Run in terminal `node -v`
   * Verify npm `npm -v`
  
2. Install Newman
   *`In Command- `npm install -g newman`
   * Run `newman -v`
  
3. Export and save collection from Postman
4. Export and save environment form Postman
5. Create project directory
    * Restful-booker-newman
      * collections
      * environments
      * scripts
      * reports

6. Run API Tests using Newman
   * Navigate to directory
   * Command- `cd folder`
   * Run `notepad scripts\run-tests.bat`, edit and save
   * Run `scripts\run-tests.bat`
   * Run `start reports\test-report.html`
   * Go to document and load the report generated

**EXPECTED RESULTS**

 * All requests return correct status code.
 * Authentication returns a valid token.
 * Booking ID is created and reused across requests.
 * Response time is under 500ms.
 * All tests pass successfully (100%)
 * No hardcorded values, uses environment variables.
 * Newman summary shows 0 failure.
 * HTML report is generated in the reports folder.


**TEST COVERAGE**

1. Authentication.
2. Booking CRUD operations.
3. Netesting.
4. Edge case scenarios.
5. Performance validation.

**NOTES**

1. Dynamic dates are generated using Postman `moment` library.
2. Token is automatically generated if missing.
3. The mock server is used to enssure consistent, repeatable tests results independent of live API availability.
4. Collection is structured for readability and maintainability

