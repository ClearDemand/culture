# Simplified Coding Exercise for Software Engineering Roles

## Instructions

For this exercise, you will develop a **full stack application** using both the technical and business requirements further down in this document. Please submit the source code for your solution using the instructions below.

1. Share the link to your solution in a **GitHub public repository**.  Please **DO NOT** send a zip file containing your solution.
1. E-mail `devteam@cleardemand.com` with the above link to your solution.

## Preferred Technologies

The following are the preferred technolgies we would like to see used to implement this solution.

* C#
* ASP.NET
* A relational database (i.e. SQL Server, Postgres, sqlite)

For this exercise, you have the option of...
1. Creating a simple backend API
1. _Optionally_, creating a full stack application with a UI (this is not necessary though)

## Backstory

We'll pretend we're building a utility for small convenience store owners.  We will be providing them with an easy way to keep track of the inventory of the products they sell in their stores. 

Below, you will find both technical and business requirements to help you craft the application.

## Technical Requirements

You will build the ability for store owners to maintain their set of products in their store.  By maintain, we mean, perform the simply CRUD (Create, Read, Update, Delete) that one would do.

Again, to repeat, for this exercise, you have the option of...
1. Creating a simple backend API or...
1. _Optionally_, creating a full stack application with a UI (this is not necessary though)

For the purposes of simplifying the scope of this exercise a **Product** will have the following properties.
  * UPC (a unique human readable identifier)
  * a description (text which describes the product)
  * current price (current retail price of the item in USD)
  * quantity (number of units they currently have)

## User Stories

### User Story #1: Ability to view all of the products I am tracking in the system

#### Value

As a Store Owner, I want to retrieve all of the products I have entered into the software.

#### Acceptance Criteria

* I should be able to retrieve all of the properties for each Product (product Id, description, price, quantity).
* I should be able to see the field names and their associated values for each product.

### User Story #2: Add new products to the system

#### Value

As a Store Owner, I want to be add additional products to the software.

#### Acceptance Criteria

* I should be able to submit the information about that product (product Id, description, price, quantity).
* I should be made aware of invalid values that may have been submitted.
* After I successfully create the new product, it should be available in the system.

### User Story #3 Update an existing product in the system

#### Value

As a Store Owner, I want to be able to modify any of the products I've already entered into the software.

#### Acceptance Criteria

* For a given product, I should be able to submit updated information about that product (product Id, description, price, quantity).
* I should be made aware of invalid values have been submitted.
* After I successfully create the new product, it should be available in the system.

### User Story #4 Delete a product from the system

#### Value

As a Store Owner, I want to be able to delete any of the products I've already added into the software.

#### Acceptance Criteria
* I should be able to delete any of the existing products in the system.
* After I successfully delete that product, it should no longer be available in the system.

## Helpful hints

We're not expecting this to take more than a few hours to complete.
* _**Building a UI is not necessary**_.  Don't waste a lot of time making an elegantly beautiful front end thereby sacrificying your ability to also focus on the business rules on the backend.
* Get the basics down and then iterate to make refinements.

Finally, demonstrate the software engineering techniques which you practice and advocate for.

Good Luck!
