
# Unit4 Business World setup for Wanda Digital Assistant

## About this guide
This implementation guide covers the setup required in Business World to allow the use of the Unit4 Wanda digital assistant, and is aimed at implementation consultants and system administrator level staff who are responsible for configuring and maintaining a Business World installation.

## System requirements

-	Unit4 Business World Milestone 6 Update 3 or later, plus the latest Experience packs installed for the customer
-	Unit4 Identity Services (U4IDS) registered and configured in the cloud for the customer by Unit4 Cloud Operations
-	Customer (tenant) must be configured in the Unit4 Discovery Service
-	Unit4 Message Hub registered and configured for the customer in the cloud for the customer by Unit4 Cloud Operations
-	End users must have a user account on Microsoft Teams, Skype, Slack or Facebook Messenger

## General considerations

- Wanda is a cloud-only service managed by Unit4 and supports a hybrid setup with an on-premise Unit4 Business World installation.
- Wanda is delivered as a cloud service with continuous non-breaking releases, which means that it will get smarter and learn new skills on a regular basis.
- Customers must agree to the overall [Unit4 Wanda Digital Assistant Terms & Conditions](https://get-wanda-help.u4pp.com/wandaprivacystatement/), including the Terms & Conditions for Microsoft Services such as the Microsoft Language Understanding Service and Microsoft Bot Connector.

## Wanda usage scenarios
#### Supported scenarios
The Unit4 Wanda digital assistant cloud service can be used in the following scenarios:

* Managed cloud, where the Unit4 Business World application and required Unit4 People Platform services are hosted and managed in the cloud by Unit4 Cloud Operations
* Hybrid cloud, where the Unit4 Business World application is hosted and managed on-premise by the custoomer, and the Unit4 People Platform services are hosted and managed in the cloud by Unit4 Cloud Operations


#### Required Unit4 People Platform services

The following Unit4 Platform services are required:

* Unit4 Identity Services (U4IDS) to provide authentication and identity mapping. U4IDS is a multi-tenant Federation Gateway using the OpenID protocol
* Unit4 Message Hub to provide message handling / management for notifications

## Wanda implementation steps

The required setup for Unit4 Business World to use Wanda consists of:

* Ordering and registration of the Unit4 Wanda digital assistant with the Unit4 Cloud for the customer's Business World installation. Ordering of Wanda and the selected [digital assistant skills](digitalassistants.md) is done by the customer via their Unit account manager, and Wanda registration and setup in the Unit Cloud is done by Unit4 Cloud ops. See [Unit4 Wanda ordering and registration](order-registration.md) for details.
* Registration / setup of the Unit4 People Platform cloud services required by Wanda, such as Unit4 Identity services (U4IDS).
    * For Business World installations running as a Unit4 cloud service this entire setup including the required Business World setup is done by the Unit4 Cloud Operations team.
    * For Business World installations running on-premise, the required Business World technical setup to operate with U4IDS is done by implementation consultants and the customer using the Business World Management Console. The [Wanda IDS setup](ubw-ids-configuration.md) outlines this procedure.
* Functional setup of the Unit4 Business World installation to support the business functionality required by Wanda for the specified digital assistant skills. This is done by implementation consultants and the customer. See the Functional setup section which describes the necessary setup for each Wanda skill.




