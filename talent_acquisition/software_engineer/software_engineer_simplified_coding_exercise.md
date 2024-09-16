# Simplified Coding Exercise for Software Engineering Roles

## Instructions

For this exercise, you will develop a **full stack application** using both the technical and business requirements further down in this document. Please submit the source code for your solution using the instructions below.

1. Share the link to your solution in a **GitHub public repository**.  Please **DO NOT** send a zip file containing your solution.
1. E-mail `devteam@cleardemand.com` with the above link to your solution.

## Technical Requirements

The following are the preferred technolgies we would like to see used to implement this solution.

* Blazor WebAssembly
* ASP.NET
* A Relational Database (i.e. SQL Server, Postgres, sqlite)

## Backstory

We'll be creating a simple application targeted at small convenience store owners.  We will be providing them with an easy way to keep track of the products they sell in their stores. 

The following are a set of user stories to help craft the application

## Technical Ipmlementation

You will build out a simple, full-stack application for the store owner to maintain their set of products in their store.  By maintain, we mean, perform the simply CRUD (Create, Read, Update, Delete) that one would do. 

For the purposes of reducing the scope of this exercise a **Product** will have the following properties.
  * a unique human readable identifier (i.e. ProductId or UPC)
  * a description
  * current price (in USD)
  * quantity (number of units)

## User Stories

### User Story #1: Ability to view all of the products I am tracking in the system

#### Value

As a Store Owner, I want to see a table or grid of all of the products I have entered into the system

#### Acceptance Criteria

* I should be able to see all of the products on the screen.
* I should be able to see all of the properties of each Product (product Id, description, price, quantity)

### User Story #2: Add new products to the system

#### Value

As a Store Owner, I want to be add additional products to the system.

#### Acceptance Criteria

* I should be able to enter the information about that product (product Id, description, price, quantity).
* It should tell me if I've entered invalid values for any of the properties and not let me save that product.
* It should let me save my new product.
* After I successfully save the new product, it should show the new product in the table which shows me all of the products.

### User Story #3 Update an existing product in the system

#### Value

As a Store Owner, I want to be able to modify any of the products I've already entered into the system

#### Acceptance Criteria

* I should be able to enter the information about that product (product Id, description, price, quantity).
* It should tell me if I've entered any invalid values for any of the properties and not let me save that product.
* It should let me save my updates to the existing product.
* After I successfully save the new product, it should show the new product in the table shows me all of the products.
* If I decide to cancel my changes while entering them, the product information should reflect the values they were originally.

### User Story #4 Delete a product from the system

#### Value

As a Store Owner, I want to be able to delete any of the products I've already entered into the system

#### Acceptance Criteria
* I should be able to choose any of the existing products in the system and choose to delete it.
* It should prompt me to double check to make sure I want to delete it.
* It should only delete that product if I confirm the delete from the prompt.
* After I successfully delete that product, it should no longer show up in table shows me all of the products.
* If I decide to cancel my changes while entering them, the product information should reflect the values they were originally.

## Helpful hints

We're not expecting this to take more than a few hours to complete.
* Don't waste a lot of time making an elegantly beautiful front end thereby sacrificying your ability to also focus on the business rules on the backend.
* Get the basics down and then iterate to make refinements.

Finally, demonstrate the software engineering techniques which you practice and advocate for.

Good Luck!
