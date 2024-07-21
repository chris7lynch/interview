### Resources
The API I want you to use is available at https://fakestoreapi.com/products
The documentation for this API is hosted at https://fakestoreapi.com/docs

### Use the Acceptance Criteria below to guide your work

Feature: Retrieve and Filter Products from Fake Store API

  Background:
    Given the application is configured to connect to "https://fakestoreapi.com/products"
    And the application can retrieve the products without error

  Scenario: Filter and Format Highly Rated Products
    Given the application requests all products from the API
    When the application receives the list of products
    Then it should filter out products with a rating less than 3.0 or fewer than 100 reviews
    And it should format the price of each filtered product into USD currency format
    And it should write the filtered products to "results.json"