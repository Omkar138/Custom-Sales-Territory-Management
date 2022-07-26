# Custom-Sales-Territory-Management
Salesforce Project 


Firebolt Motors Inc. is experiencing exponential sales growth after releasing their hit model of
solar powered sports car.They employ a Sales team that sells vehicles to auto dealers across the United States.
Each sales representative has a territory of one or more zip codes. Sales reps own the relationship
with all auto dealers in their zip code territories.

Firebolt Motors Inc. currently uses Salesforce to track their sales activities, including:

● Accounts: Each account represents an automobile dealer.

● Opportunities: A sale of vehicles to an automobile dealer.

● Contacts: Automobile dealer employees.

The Sales Operations team uses a combination of Salesforce and spreadsheets to manage
each sales rep’s territory. They are manually setting the Account Owner field to the sales rep’s
User record when the Account’s Zip Code belongs to the sales rep. currently, a list of zip codes
and their sales rep is stored in spreadsheet that looks like this:
Zip Code Sales Representative

91000    Blake

91001    Blake

91002    Blake

91002    Jacqueline

91010    Jacqueline

91020    Jacqueline


Since Firebolt Motors Inc.’s sales team has tripled in size in the past year, the Sales Operations
team is having trouble keeping up with all the sales territory changes. This process must be
automated!


Requirements
Requirement #1: Recreate the Zip Code spreadsheet as a custom Territory object. The custom
object should have the following custom fields:

Field        Field Type         Field Type Description
Name         Text               Zip Code Text The standard name field. Each record will be named after its specific zip code.



Owner Lookup                   The standard owner field. The sales rep assigned to this
User                                territory


Note: All fields should have field history tracking turned on.
Requirement #2: When an Account’s BillingPostalCode (aka Zip Code), is changed,
1. Change the Account Owner to the sales representative assigned to the new zip code
2. Change the Owner field of all the Account’s Contacts to the same sales rep
3. Change the Owner field of all the Account’s Open Opportunities to the same sales rep

Note:
● The logic should run only when the Account’s zip code is changed or populated for the
first time
● If no matching Territories are found, do nothing


Requirement #3: Multiple sales representatives can be assigned to the same zip code territory.
If this is the case, use a random function to select one of the assigned sales representatives.


Requirement #4: Three sales representatives at most can be assigned to a single zip code.
Display an error if a user attempts to associate another sales representative to a zip code
