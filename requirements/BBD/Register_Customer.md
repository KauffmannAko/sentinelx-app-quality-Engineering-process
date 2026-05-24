# SNT-AUTH-001 — Customer User Registration

## Type

Backend + Frontend

## User Story

As a customer,  
I want to register an account,  
So that I can access the platform.

## Acceptance Criteria

- User can register with valid details
- Duplicate email registration is rejected
- Password validation is enforced
- Success response is returned

## BDD Scenarios

```gherkin
Feature: Customer User Registration
  As a customer
  I want to register an account
  So that I can access the platform

  Background:
    Given the customer registration page is available
    And the customer registration API is available

  Scenario: Register customer with valid details
    Given the customer provides valid registration details
      | firstName | lastName | email            | password     | confirmPassword |
      | John      | Doe      | john@example.com | Password@123 | Password@123    |
    When the customer submits the registration form
    Then the customer account should be created successfully
    And the system should return a success response
    And the customer should see a successful registration message

  Scenario: Reject registration with duplicate email
    Given a customer account already exists with email "john@example.com"
    And another customer provides registration details using email "john@example.com"
    When the customer submits the registration form
    Then the registration should be rejected
    And the system should return a duplicate email error response
    And the customer should see a clear message that the email is already registered
    And no duplicate customer account should be created

  Scenario Outline: Enforce password validation during registration
    Given the customer provides registration details with password "<password>"
    When the customer submits the registration form
    Then the registration should be rejected
    And the system should return a password validation error response
    And the customer should see the message "<expectedMessage>"
    And no customer account should be created

    Examples:
      | password | expectedMessage                                      |
      | pass     | Password must meet the minimum security requirements |
      | 12345678 | Password must meet the minimum security requirements |
      | password | Password must meet the minimum security requirements |

  Scenario: Return success response after successful registration
    Given the customer provides valid registration details
    When the customer submits the registration form
    Then the backend should return a success status response
    And the response should include the created customer user details
    And the response should not expose the customer's password
    And the frontend should display a successful registration confirmation
```