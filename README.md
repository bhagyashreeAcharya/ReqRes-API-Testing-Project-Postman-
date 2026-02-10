# ReqRes API Testing Project (Postman)

This project demonstrates API testing using Postman on the ReqRes public API. It covers CRUD operations, authentication scenarios, negative testing, and automated test scripts using Postman.

This project is designed for QA portfolio purposes to showcase API testing skills.

---

## Project Objective

Validate ReqRes REST APIs using Postman by verifying:

- HTTP status codes
- Response body validation
- CRUD operations (Create, Read, Update, Delete)
- Authentication scenarios (Register, Login, Logout)
- Negative scenarios (User not found, Invalid login)
- Response time validation
- Environment variables usage
- Automated test scripts
- Collection Runner execution

---

## Tools Used

- Postman
- ReqRes API (https://reqres.in)
- GitHub
- JSON
- REST API

---

## Tested Endpoints

### User APIs
- GET List Users
- GET Single User
- GET User Not Found
- POST Create User
- PUT Update User
- PATCH Update User (Partial)
- DELETE Delete User

### Authentication APIs
- POST Register Successful
- POST Register Unsuccessful
- POST Login Successful
- POST Login Unsuccessful
- POST Logout

### Other APIs
- GET Delayed Response
- POST Redirect

---

## Test Validations Performed

- Status code validation (200, 201, 204, 400, 404)
- Response body validation
- Response time validation (< 2000 ms)
- Token validation
- ID validation
- Empty response validation (Delete)
- Error message validation
- Environment variable usage

---

## Environment Variables Used

- Base_URL
- x-api-key
- userId
- token

---

## Project Structure

```
ReqRes-API-Testing-Project/
│
├── Collection/
│   └── ReqRes_API_Testing_Collection.json
│
├── Environment/
│   └── ReqRes_Environment.json
│
├── Screenshots/
│   ├── 01_Collection_Overview.png
│   ├── 02_Environment_Variables.png
│   ├── 03_Create_User_201.png
│   ├── 04_Update_User_200.png
│   ├── 05_Delete_User_&Test_Script_204.png
│   ├── 06_Register_User_Success_200.png
│   ├── 07_Register_User_Failure_400.png
│   ├── 08_Login_Success_200.png
│   ├── 09_Login_Failure_400.png
│   ├── 10_Create_User_Script.png
│   ├── 11_Login_Failur_Script.png
│   ├── 12_Collection_Run_All_Passed.png
│   └── 13_Collection_Run_All_Passed.png
│
└── README.md
```

---

## How to Run This Project

Step 1: Install Postman

Step 2: Import Collection  
Open Postman → Click Import → Select  
ReqRes_API_Testing_Collection.json

Step 3: Import Environment  
Import ReqRes_Environment.json

Step 4: Select Environment  
Choose ReqRes Environment from dropdown

Step 5: Run Collection  
Click Collection → Run → Run Collection

Step 6: View Results  
All test results will appear in Collection Runner

---

## Sample Test Script Used

```javascript
pm.test("Status code is 201 Created", function () {
    pm.response.to.have.status(201);
});

pm.test("Response contains ID", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.id).to.not.be.empty;
});

pm.test("Response time is less than 2000ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(2000);
});
```

---

## Key Skills Demonstrated

- API Testing
- Postman Collections
- Environment Variables
- Automated Test Scripts
- CRUD API Testing
- Authentication Testing
- Negative Testing
- Response Validation
- Test Execution using Collection Runner

---

## Author

Bhagyashree  
QA Engineer | API Testing | Postman | Manual Testing
