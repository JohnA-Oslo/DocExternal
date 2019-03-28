
# Overview of Wanda Digital Assistant skills

This section gives an overview of the currently available skills offered by Wanda. Which digital assistant skills are to be made available for the customer organization is specified at the time of ordering Wanda and these skills are then registered by Unit4 Cloud Operations. 

Note that this current version of Wanda understands English, Norwegian and Swedish only. However, additional languages will be added in future.

Wanda is able to understand utterances which are misspelled or grammatically incorrect.

## Available Digital assistant skills

The current version of Unit4 Wanda Digital Assistant includes the following skills/functionality:

- Absence Assistant
- Balances Assistant
- Expenses Assistant
- Payslip Assistant
- Purchasing Assistant
- Tasks Assistant
- Time Assistant
- Travel Request Assistant

The detailed implementation guides describe the required setup for each skill.

## Absence Assistant

####Functionality offered
- Submit absence requests
- Include attachments such as medical certificates or similar documents to support the absence request
- Enquire on status of submitted absence request

####Example utterances to trigger Absence skill:
- _Enter new absence_
- _Enter vacation_
- _I'll be off next week._
- _I'll be off sick today_
- _I want to take a day off tomorrow_  

## Balances Assistant

####Functionality offered
- Enquire on balances (vacation, flexi-time, overtime and sickness)
 
####Example utterances to trigger Balances skill
- _Show my balances_
- _How many holidays do I have left?_
- _How much overtime have I built up?_

## Expenses Assistant

####Functionality offered
- Add expenses manually and automatically using receipt recognition
- Keep draft expense reports until ready
- Submit the total estimate expenses for approval
- See expenses details for informative purposes
- Ask for the status of submitted expense claims

####Example utterances to trigger Travel Request skill

* _Add receipt_
* _I want to do my expenses_
* _Submit my expenses_
* _Add expense_
* _Add receipts_
* _Complete expense_
* _What's the status of my expense claim?_

## Payslip Assistant

- Enquire on payslips for last month or any other previous period

####Example utterances to trigger Payslip skill

- _Show my payslip_
- _Show my payslip for March_

## Purchasing Assistant

####Functionality offered

- Request products from an internal product catalog (connection to marketplaces is planned for future releases)
- Submit simple purchase requisitions
- Enquire on the status of requisitions
- Ask for the status of a submitted purchase request and get the workflow status (approved, rejected etc.)

####Example utterances to trigger Purchasing skill
-	_Requisition_
-	_I want to buy/order/request [product]_
-	_Buy me a [product]_
-	_What's the status of my [product] order?_

## Tasks Assistant

#### Functionality offered

- Approve tasks (aimed at manager / supervisor roles)
- Get the list of current tasks
- Have Wanda flag important tasks and proactively push towards deadlines / due dates
- Get the status of submitted travel requests, absences, expenses and purchase requests

#### Example utterances to trigger Tasks skill

-	_Tasks_
-	_Show me all requisition tasks._
-	_I want to approve travel requests_
-	_Any invoices to check?_
-	_Are there any purchase orders to approve?_

#### Wanda Task notifications

Wanda's Tasks Assistant notifies the user about: 

| Approval Tasks				| Notification frequency								   |Number of tasks per notification       |Examples						|
| ------------------------------|----------------------------------------------------------|---------------------------------------|--------------------------------|
| Important						| immediate												   | one								   |_You have a requisition task currently awaiting action. It is marked as important._|
| Close due date				| checked every 30 minutes (24 hours before due date)	   | one								   |_You have a requisition task currently awaiting action. Please be aware that its time limit is within the next 24 hours._|
| Escalated						| checked every 30 minutes (automatic); immediate (manual) | one to many (automatic); one (manual) |Automatic: _This is a notification message about an automatic escalation from {origUser}. You have the following requisition task_ |
| Forwarded						| checked every 30 minutes								   | one								   | _This is a notification about a forwarded task to you from *Jane Doe*, with the following comment: *please check the requested amounts*._ |
| New							| checked every 30 minutes								   | one								   |_There is one requisition task for you._ |
| Reminders						| checked every 30 minutes								   | one to many						   |_This is a reminder. You have the following 5 requisition tasks._|
| As substitute of another user | checked every 30 minutes								   | one to many						   |_As the substitute of *Jane Doe*, this is a notification for you. You have the following 5 requisition tasks._|


| Non-Approval Tasks			| Notification type  |Number of tasks per notification  |Examples					    	|
| ------------------------------|--------------------|----------------------------------|-----------------------------------|
| Rejected						| immediate			 | one to many					    | _You have a requisition task regarding office supplies, with the following comment: "please check the provider" from Jane Doe. To correct this task, you can go to Business World._ |

To receive these notifications, alerts must be setup in the _Alert setup_ window of Business World- Important approval tasks can also be configured in the Element type window. On the other hand, due dates can be configured in different ways. For more details on setting up alerts, importance levels and due dates, see [Reference Manual Spring 2017 - Workflow](http://abwdocs.agresso.no/Restricted/Docs/CustDocSpring2017/Spring2017/RefMan_Workflow_Spring2017.pdf) (password required). 

## Time Assistant

####Functionality offered

- Add time transactions to their timesheets manually
- Accept suggestions for planned time from Planner and Project planner
- Add time to projects (recent projects are suggested)
- Enquire on the status of timesheets and be informed on the outcome of the workflow approval process (approved, rejected etc.) 

####Example utterances to trigger Travel Request skill

-	_Add timesheet for [period/day]_
-	_Add timesheet_
-	_Enter timesheet_
-	_Do my timesheet for last Monday_ (if the user needs to reference a day in the past, the input is _last Monday_ and not _Monday_ alone.)
-	_Change timesheet for yesterday_
-	_Do timesheet for 26th June 2018_


## Travel Request Assistant

####Functionality offered

- Enter a travel request to get approval to travel before booking a trip, purchasing tickets or similar activities
- Enquire on the status of travel requests and be informed of the outcome of the workflow process (approved, rejected etc.)
- 
####Example utterances to trigger Travel Request skill

* _Travel request_
* _I want to travel to [destination] [time period]._	
* _Can you book a trip to [destination] [time period]?_
* _I need to travel to [destination] [time period]._

Wanda's Travel Request Assistant is able to extract the relevant information from the initial key utterance, for example, _I need to travel to London from Thursday to Friday for a seminar._



