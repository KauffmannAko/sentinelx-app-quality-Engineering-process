# SNT-PROD-001 — View Products

## Type

Backend + Frontend

## User Story

As a customer,  
I want to browse products,  
So that I can purchase items.

## Acceptance Criteria

- Products are paginated
- Products support filtering/search
- Product details are viewable

## BDD Scenarios

```gherkin
Feature: View Products
  As a customer
  I want to browse products
  So that I can purchase items

  Background:
    Given the product listing page is available
    And the product listing API is available
    And products exist in the system

  Scenario: View paginated product list
    Given there are more products than the default page size
    When the customer opens the product listing page
    Then the system should display the first page of products
    And pagination controls should be available
    And the backend should return products according to the requested page and limit

  Scenario: Navigate to the next page of products
    Given the customer is viewing the first page of products
    And more products are available on the next page
    When the customer selects the next page
    Then the system should display the next set of products
    And the previously displayed products should not be duplicated
    And the backend should return the correct page of product results

  Scenario: Search products by keyword
    Given products exist with names or descriptions matching "phone"
    When the customer searches for "phone"
    Then the system should display only products matching the search keyword
    And the backend should return filtered product results
    And products that do not match the search keyword should not be displayed

  Scenario: Filter products by category
    Given products exist in different categories
    When the customer filters products by category "Electronics"
    Then the system should display only products in the "Electronics" category
    And the backend should return products matching the selected category

  Scenario: View product details
    Given the customer is viewing the product listing page
    When the customer selects a product
    Then the system should display the product details page
    And the product name, price, description, and availability should be shown
    And the backend should return the correct details for the selected product

  Scenario: Show empty result when no product matches search
    Given no products match the search keyword "unknownitem"
    When the customer searches for "unknownitem"
    Then the system should display an empty search result message
    And no unrelated products should be displayed
```