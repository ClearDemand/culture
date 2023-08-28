# Coding Exercise for Software Engineering Roles

## Instructions

For this exercise, develop a full stack application using both the technical and business requirements further down in this document. Please provide both the source code and a working version of your application.

1. Share the link to your solution in a GitHub public repository
1. Share a link to your working application deployed to the cloud provider of your choice.

**E-mail humanresources@cleardemand.com with the above links to your solution.**

_Note: This exercise may seem rather lengthy, however, we've been purposely verbose to explain the business requirements for the solution.  See the [Helpful Hints](#helpful-hints) section for guidance on using your time wisely._

## Technical Requirements

The following are the preferred technolgies we would like to see used to implement this solution.

* Blazor WebAssembly
* ASP.NET
* Postgres (or alternative relational database)

### Deploying Your Applcation

All of the major cloud providers provide some sort of introductory free and "always free" plan for providing cloud resources for your application.

[free-for.dev](https://free-for.dev/) is a good resource for finding free resources that developers can use to experiment with without incurring any cost.

## Backstory

Retail store owners have limited space on their shelves with which they can use. 
Even for store owners doing E-Commerce, there is a limited set of capacity they have to "warehouse" the products they sell. For store owners who sell seasonal items, demand for those items tapers off sharply as that season comes to a close.

No store owner wants to be left with a bunch of Halloween decor after October 31st if they are trying to prepare to sell products for the Fall and Winter holidays like Thanksgiving and Christmas.

We want to create a simple application that will allow a small business owner to run some what-if scenarios that will allow them to create a plan to put their products on clearance so they can get rid of their excess inventory.

The following are a set of user stories to help craft the application

## Setup

For the purposes of reducing the scope of this exercise, we're going to assume that the system already has products and inventory already set up.

Rather than building out the full-stack CRUD functionality to maintain these entities in the database...

1. Create whatever entities you need in your backend database to represent the concept of Products and Inventory
1. Populate those entities with dummy data.

For the purposes of this exercise, a **Product** should have the following attributes:
  * a unique human readable identifier (i.e. UPC)
  * a description
  * a cost (this is how much the product costs me as a store owner to manufacture or buy)

**Inventory** is defined as the number of units of a product on hand at a specific date.

_**Don't skip this step.**_  You'll need to represent Prodcuts and Inventory to complete the user stories below.

## User Stories

### User Story #1: Ability to Create a Markdown Plan

#### Value

As a Store Owner, I want to create a Markdown Plan for a Product, so that I can run what-if scenarios on projected sales

Note: a markdown is a permanent price decrease on an item at the end of its lifecycle. For this story, we'll establish a date for when we want to start marking down the price of a product and the target date for when we would like the markdown to end.  (_Ideally, we would have no more inventory at the end of the markdown period._)

#### Acceptance Criteria

* I should be be able to maintain (Create, Read, Update, Delete) Markdown Plans.
* I should be able to select which Product I want to create a plan for.
* I should be able to set the beginning date for my markdown plan.
* I should be able to set the target end date for my mardown plan.
* The target end date should be no less than one week after the beginning date.

### User Story #2: Establish 3 price reductions during the course of the markdown

#### Value

As a Store Owner, I want to be able to establish 3 price reduction rules for the Markdown Plan.

Note: during the course of the markdown plan we'll allow for 3 price reductions.  These will be entered as a percentage.  The percentage that is entered will apply to the previous price.

#### Acceptance Criteria

* I should be able to set the initial price reduction on the first day of the markdown.
* I should be able to set a price reduction percent which will take effect halfway through the markdown plan (_so, for example, if my markdown plan lasts 10 days, on day 5, this price reduction percentage will take effect_).
* I should be able to set the final price reduction for the last day of the markdown (_Essentially, if I still have inventory left on the final day, I may want to drop the price even more dramatically to get rid of it even if it means incurring a substantial loss_)
* The final price reduction cannot be less than $0.50.

#### Example

I have a Markdown Plan which goes from September 1st through the 30th. The current price of the product I want to markdown is $10.00.
* At the beginning of the markdown (September 1st), I want to set a markdown of 20%, which would bring the price to $8.00.
* Halfway through (September 15th), I want to markdown the product another 50%, bringing the price to $4.00.
* On the last day, I want to markdown the product 75%, bringing the price to $1.00.


### User Story #3 Enter Sales Data

#### Value

As a Store Owner, I want to be able to enter sales data for the Products I've put on markdown.

Note: We want to enter sales data using the Markdown Plan I created.

#### Acceptance Criteria

* I should be able to select which Markdown Plan I want to execute.
* For each day of the markdown plan I should be able to sequentially enter in the total number of units of that product sold that day.
* I cannot sell more units than I have actually have inventory for.
* The sell price **must** reflect the price reductions set up in the Markdown Plan.


### User Story #4 See Daily Metrics

#### Value

As a Store Owner, for each day, I want to see my profit or loss.

_Note: We want to see the results of the plan in terms of profit and loss._

#### Acceptance Criteria
* I should be able to see the following detailed information about the product:
  * unique identifier
  * description
  * starting inventory

* For each day, I want to see the following:
  * the total number number of units sold.
  * the margin (sell price - cost).
  * the day's profit (or loss) for that product.
  * the remaining inventory.

## Optional

All the user stories below are completely optional to implement for this exercise.

### User Story #5: View a Summary Report

#### Value

As a Store Owner, I want to see a simple report summary of the Markdown plan.

_Note: We want to see the results of the plan in terms of profit and loss._

#### Acceptance Criteria
* I should be able to see the detailed information about the product
  * unique identifier
  * description
  * starting inventory

* I should be able to see the following summary information for the Markdown plan:
  * the total number number of units sold for the entire plan.
  * the profit (or loss) for that product over the entire plan.
  * the final remaining inventory (number of units) after all of the sales.

### User Story #6: Maintain the Products Being Sold

#### Value

As a Store Owner, I want to be able to maintain (Create, Read, Update, Delete) a set of Products that I sell.

#### Acceptance Criteria
* For products I want to be able to set
  * a unique human readable identifier (i.e. UPC)
  * a description
  * a cost (this is how much the product costs me as a store owner to manufacture or buy)

### User Story #7: Ability to Set the Current Inventory Level

#### Value

As a Store Owner, I want to be able to set the current inventory of my products.

#### Acceptance Criteria

* For a selected product...
  * I should be able to set and update the quanitity.
  * If I enter a quantity of zero, assume that means it's out of stock.

## Helpful hints

This exercise may seem rather lengthy to complete, but it boils down to a few basic concepts:
* Designing and creating database entities for Products and Inventory
* Creating plans to put Products on Clearance (Mardown) (more basic CRUD)
* Entering simulated sales for those products
* Doing some basic math to compute inventory and profit metrics based on sales.

We're not expecting this to take more than a few days of spare time.
*  Skip the optional section if you find yourself spending too much time on it.
* Don't waste a lot of time making an elegantly beautiful front end thereby sacrificying you're ability to also focus on the business rules on the backend.
* Get the basics down and then iterate to make refinements.
*  _**The optional stories are indeed optional**_. This is not a trick.

Finally, demonstrate the software engineering techniques which you practice and advocate for.

Good Luck!


