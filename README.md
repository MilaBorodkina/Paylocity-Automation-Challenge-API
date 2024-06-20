# Paylocity Automation Challenge

This repository contains a Postman collection for testing a Paylocity Benefits Dashboard API. 

This collection includes several test cases to ensure that the API functions as expected, covering scenarios such as retrieving a list of employees, adding a new employee, getting an employee by ID, updating employee details, and deleting an employee.

## Requirements:

To use the Postman collection, you need to have the following installed:

- [Postman](https://www.postman.com/downloads/): A platform for API development.

## Getting Started:

Clone the repository:
   
   ```
   git clone https://github.com/MilaBorodkina/Paylocity-Automation-Challenge-API
   ```

Open Postman: Launch the Postman application on your machine.

Import the Collection:

In Postman, click on the Import button.

Choose the Paylocity API Tests.postman_collection.json file from the cloned repository.

Set Environment Variables:

Ensure you have an environment set up with the following variables:

token: The authentication token required for the API requests.

## Running the Tests:

Execute the requests to test the API endpoints.

### Test Details:

• **Get Employee List**
Check if the status code is 200.
Verify that each employee has necessary fields (id, firstName, lastName, dependants).
Validate the data types of the fields.

• **Add Employee**
Check if the status code is 200.
Verify that the response contains employee data with correct values.

• **Add Employee Dependents Out Of Range**
Verify that the status code is 400.
Check for an error message indicating the dependants must be between 0 and 32.

• **Add Employee Long Name**
Verify that the status code is 400.
Check for an error message indicating the maximum length of the first name.

• **Add Employee Empty Field**
Verify that the status code is 400.
Check for an error message indicating the first name is required.

• **Get Employee**
Check if the status code is 200.
Verify the returned employee ID matches the requested ID.
Validate the presence and type of employee details.

• **Update Employee**
Check if the status code is 200.
Verify the employee data is updated correctly.

• **Update Employee Invalid ID**
Verify that the status code is 405.

• **Delete Employee**
Check if the status code is 200.

• **Delete Employee Invalid ID**
Verify that the status code is 405.
