# Travel Request Assistant

Wanda's Travel Request helps users to submit travel requests and send them for approval. Wanda can also provide cost estimates based on available data from the user's previous similar trips and those of his or her colleagues. 

## System requirements

- Expenses Experience pack version 4.6 or later installed
- Task Management Experience pack version 2.3 or later installed
- Travel Requests public API exposed (found unser Expenses in access screen)
- Unit4Me service V201501 configured 

## System setup 

- Assign user/role access rights for the relevant users to the following:
	- Travel requests public API 
	- Objects public API, and access to **Attributes** and **Attribute values** objects
	- Task Management public API
	- Unit4Me service V201501

- Activate the system parameter DEF\_TRAVEL\_REQ_TYPE and assign the travel rule used for travel requests.

