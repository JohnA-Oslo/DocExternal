# Services used by the Expenses

This topic describes the different API endpoints used by Expenses.

## U4 PUBLIC API


#### GET - V1/OBJECTS/ATTRIBUTE-VALUES
Used to get attribute values. Limit 20 results, selects attributeId and description.
Query contains filter: attributeId eq '{accountingInformationId}' and status eq 'N' and (contains(description, '{filter}') or contains(attributeValue, '{filter}'))
•	accountingInformationId => attributeId to lookup.
•	filter => free text (whatever user types to identify attribute value). 

#### GET - V1/OBJECTS/ATTRIBUTES
Used to get attribute descriptions to replace description given by attribute-values endpoint.

#### POST - /V1/ME/TRAVEL-EXPENSES
Used to create new travel expense. Can also include optional query parameter importExpenseIds to automatically connect existing external transactions with the new travel expense.

#### POST - /V1/ME/TRAVEL-EXPENSES/{TRAVELEXPENSEID}EXPENSELINES
Used to update travel expenses with external transactions, described with query parameter `importExpenseIds`.

#### GET - /V1/ME/TRAVEL-EXPENSES/{TRAVELEXPENSEID}
Get existing travel expense by ID.

#### PATCH - /V1/ME/TRAVEL-EXPENSES/{TRAVELEXPENSEID}
Patch travel expense by travel expense ID.

#### GET - /V1/OBJECTS/TRAVEL-TYPES
Used to get information about active travel types in Business World. Only COST and SingleTravel travel types are considered by the Expense bot.

#### GET - /V1/ME/TASKS-ENQUIRY/{COMPANYID}
Get workflow status information for travel requests.

##U4 SOAP SERVICES

### UNIT4ME - SERVICE.SVC?UNIT4MESERVICE/UNIT4MEV201501

#### GETCOMPANYINFOASYNC
Used to get information about the default company for the current tenant.

### TRAVEL - SERVICE.SVC?MOBILEAPPTRAVELSERVICE/TRAVELV201212

#### ADDEXTERNALTRANSACTIONASYNC
Used to add new expense lines as external transactions. This is basically potential expense lines that can be added to an expense claim at a later stage.

#### DELETEEXTERNALTRANSACTIONASYNC
Used to delete external transactions. Not used by Expense agent, but exposed on FA.

#### UPDATEEXTERNALTRANSACTIONASYNC
Used to update an external transaction. Used when changing expense type/amount/date/currency code. Also used when attaching a document to the external transaction.

#### GETTRAVELEXPENSETYPESASYNC
Get information about all expense types that can be used to enter expenses.

#### GETMILEAGEEXPENSETYPEASYNC
Not currently in use, but exposed on FA.

#### GETENVIRONMENTASYNC
Used to get information about Receipt Recognition consent. Information about suggestion confidence level (to determine if result from Receipt recognition requires user validation or not). Info from GetEnvironmentAsync is also used as identification when posting/patching to Receipt Recognition.

#### USERECEIPTRECOGNITIONASYNC
When the user is asked to give consent to Receipt Recognition, the response is passed to this endpoint.