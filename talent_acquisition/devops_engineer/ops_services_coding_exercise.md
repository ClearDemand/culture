# Coding Exercise for Operational Services Roles

## Instructions

For this exercise, you will be developing a schema, data import, and (optionally) reporting capabilities based on both the technical and business requirements further down in this document. Please provide both the source code and a working version of your application.

Share any relevant artifacts for your solution including, but not limited to...
  1. The source code in a GitHub public repository
  1. An Entity-Relationship diagram
  1. A publically accessible working version of your software

**E-mail devteam@cleardemand.com with the above links to your solution.**

_Note: This exercise may seem rather lengthy, however, we've been purposely verbose to explain the business requirements for the solution.  See the [Helpful Hints](#helpful-hints) section for guidance on using your time wisely._

## Technical Requirements

While you are not limited to these, the following are the preferred technolgies we would like to see used to implement this solution.

* Python
* C#
* Postgres
* Google Cloud

### Deploying Your Applcation

All of the major cloud providers provide some sort of introductory free and "always free" plan for providing cloud resources for your application.

[free-for.dev](https://free-for.dev/) is a good resource for finding free resources that developers can use to experiment with without incurring any cost.

## Business Requirements

**Step 1** is to read through and *familiarize yourself* with the **business requirements** for the [software engineering coding exercise](../software_engineer/software_engineer_coding_exercise.md), starting with the "**Backstory**", including the [optional section](../software_engineer/software_engineer_coding_exercise_optional.md).

*Note: You will **NOT** be required to implement a full stack solution but you DO need to understand the requirements.*

## Tasks

### Schema Design

Create both a...

* **database schema** and
* an associated **Entity-Relationship Diagram (ERD)**

 ... that would satisfy the needs of the **Business Requirments** outlined in the [software engineering coding exercise](../software_engineer/software_engineer_coding_exercise.md), including the [optional section](../software_engineer/software_engineer_coding_exercise_optional.md).

## User Stories - Data Imports

For this exercise, we need to provide the ability for data to be imported into our system so that users don't have to key these in 1 at a time by hand. The following user

_Note: The data should eventually end up in the tables you came up with in your design, but you are free to expand your design to account for dealing with the implications of importing potentially imperfect data._

### General Acceptance Criteria
* I should be able to provide a comma delimted file or files of the data I am uploading
* If a record is invalid, it should not be imported
* The invalid records should not prevent the valid records from being imported
* I want to be able to tell which records were invalid

### User Story #1: Import Products and Inventory

#### Value

As a Store Owner, I want to be able to import my products and inventory information so I don't have to key those in by hand

#### Acceptance Criteria

_in addition to the [General Acceptance Criteria for data imports](#general-acceptance-criteria)..._
* I want to be able to supply my own [UPC number](https://en.wikipedia.org/wiki/Universal_Product_Code) for each product

### User Story #2: Import Markdown Plan

#### Value

As a Store Owner, I want to be able to import my Markdown Plans so I don't have to key those in by hand

#### Acceptance Criteria

_in addition to the [General Acceptance Criteria for data imports](#general-acceptance-criteria)..._
* If a product is contained in differnt Markdown Plans whose dates overlap, that's not a valid scenario

### User Story #3 Import Sales Data

#### Value

As a Store Owner, I want to be able to import sales data for the Products I've put on markdown.

#### Acceptance Criteria

_in addition to the [General Acceptance Criteria for data imports](#general-acceptance-criteria)..._
* If a product is sold outside of the period of an associated Markdown plan
  assume it was sold at its regular price.
* If a product is not included within any Markdown plan, assume it was sold at its regular price.

## Optional Enhancements

If you've had fun with and been able to breeze through the required user stories above for this coding exercise, and you want to enhance it further, we have a number of optional user stories to enhance your solution even further.

Go to the **[Optional Enhancements](ops_services_coding_exercise_optional.md)** page to build upon what you've created.

## Helpful Hints

Take some advice from the [Helpful Hints section of the Software Engineer Coding Exercise](../software_engineer/software_engineer_coding_exercise.md#helpful-hints)