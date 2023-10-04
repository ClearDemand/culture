## Optional Enhancements

If you've had fun with and been able to breeze through the required user stories for the [coding exercise](software_engineer_coding_exercise.md), and you want to enhance it further, feel free to tackle the stories below.

_**All the user stories below are completely optional to implement for this exercise**_.

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
  * the regular every-day price (in USD)

### User Story #7: Ability to Set the Current Inventory Level

#### Value

As a Store Owner, I want to be able to set the current inventory of my products.

#### Acceptance Criteria

* For a selected product...
  * I should be able to set and update the quanitity.
  * If I enter a quantity of zero, assume that means it's out of stock.
