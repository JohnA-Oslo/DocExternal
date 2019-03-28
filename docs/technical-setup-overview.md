# Technical setup overview

The following technical setup is required for Unit4 Business World to be compatible with Wanda. Note that for Business World installations running in the cloud and managed by Unit4 Cloud services, this setup is done by Unit4 Cloud services. For Business World installations running on-premise and managed by the customer, this setup is done by the customer.

## Unit4 Identity Services

* The Unit4 Business World installation must be configured to operate with Unit4 Identity Services (U4IDS). The required setup must be done in the Unit4 Business World Management console as described in [Unit4 Identity Services setup on Business World to use Wanda](ubw-ids-configuration.md).
* All users in the system must be assigned a **unit4_id** in the _**Security**_ tab in the **(TAG064) User master file** window as described in [User setup](connect-to.md).

## Unit4 Message Hub for notifications

For notifications, Wanda uses Unit4 Message Hub which is configured in the Business World Management Console as described in [Notifications setup](notifications-setup.md).