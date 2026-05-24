# SNT-AUTH-002 — Login User

## Type

Backend + Frontend

## User Story

As a customer,  
I want to login,  
So that I can access protected features.

## Acceptance Criteria

- Valid credentials generate JWT
- Invalid credentials return error
- Protected routes require authentication

## BDD Scenarios

```gherkin
Feature: Customer Login
  As a customer
  I want to login
  So that I can access protected features

  Background:
    Given the customer login page is available
    And the customer login API is available
    And a registered customer exists with email "john@example.com" and password "Password@123"

  Scenario: Login with valid credentials
    Given the customer provides valid login credentials
      | email            | password     |
      | john@example.com | Password@123 |
    When the customer submits the login form
    Then the login should be successful
    And the backend should return a JWT
    And the JWT should be valid
    And the customer should be redirected to the protected area

  Scenario: Reject login with invalid credentials
    Given the customer provides invalid login credentials
      | email            | password      |
      | john@example.com | WrongPass@123 |
    When the customer submits the login form
    Then the login should be rejected
    And the backend should return an authentication error response
    And the customer should see a clear invalid credentials message
    And no JWT should be returned

  Scenario: Prevent access to protected route without authentication
    Given the customer is not authenticated
    When the customer attempts to access a protected route
    Then access should be denied
    And the backend should return an unauthorized error response
    And the customer should be redirected to the login page or shown an authentication required message

  Scenario: Allow access to protected route with valid JWT
    Given the customer has successfully logged in
    And the customer has a valid JWT
    When the customer accesses a protected route
    Then access should be granted
    And the protected feature should be displayed

  Scenario: Reject access to protected route with invalid JWT
    Given the customer has an invalid or malformed JWT
    When the customer attempts to access a protected route
    Then access should be denied
    And the backend should return an unauthorized error response
    And the protected feature should not be displayed
```