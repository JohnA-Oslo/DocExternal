
# Unit4 Wanda ordering and registration

## Ordering

The Unit4 Wanda digital assistant is a Unit4 cloud service and must first be ordered by the customer via Unit4 account management/sales for use with Business World. Once ordered, account management/sales will take care of the registration process by submitting the Cloud Order Form. When ordering Wanda, the customer specifies which digital assistant skills are to be made available to end users. Note that a customer can choose to use a subset of the HR assistant skills, for example absence but not payslip and balances.

## Registration with Unit4 Identity Services and Discovery Service

To use Wanda the customer Business World installation must be assigned an IDS authority an IDS tenant ID and an IDS Scope, and registered with the Unit4 Identity Services and Unit4 Discovery Service. This is done by Unit cloud ops.


## Business World cloud setup / registration

The cloud setup / registration performed by Unit4 cloud ops involves the following:

* The customer is assigned a unique identifier (GUID) which is used to identify the customer throughout the Unit4 Cloud offering.
* The customer is registered as a tenant in the appropriate (geopolitical) Unit4 Identity Services instance.
* The digital assistants (skills) specified by the customer are registered centrally in the Unit4 Cloud. 
* The URLs to the customer's Unit4 Business World are registered centrally in the Unit4 Cloud. This includes URLs to the Web application, public web API and SOAP web services.

## Required customer information for on-premise installations
For cloud customers no additional information is required when Wanda is ordered. On-premise customers must provide the following URLs to Unit4 Cloud ops. These URLs must also be accessible on the internet.

- Web API
- Web Services URL
- U4BW Web Application URL


## Digital Assistant skills

Which digital assistant skills are to be made available for the customer organization is specified. The detailed implementation guides describe the required setup for these skills.







