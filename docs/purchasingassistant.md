
# Purchasing Assistant

Wanda's Purchasing Assistant helps users submit a single-product purchase request for approval. The target audience includes users with a few simple purchasing needs (for example, computer equipment, mobile devices, office supplies etc.), and not professional procurement departments with more complex purchasing requirements.

### System requirements

- Requisitions Experience pack version 1.6 or later installed (latest version is recommended)
- Purchasing public APIs exposed, including Requisitions, Products and Orders
- Product search indexing service running

### System setup

- Assign access rights to the following public APIs:
	* Requisitions (found under _Purchasing_ folder in access screen)
	* Products (found under _Purchasing_ folder in access screen)
	* Orders (found under _Purchasing_ folder in access screen)
	* Objects, in addition have access to **Attributes** and **Attribute values** objects

- If the Product master file contains accurate and descriptive product descriptions, then the Purchasing Assistant's requests will be user-friendly .

- Product images:
	* In the **LG02 Product master files** window in the Unit4 Business World desktop, there is an option to connect images to products (Product image tool item). Wanda only supports URL links. It is recommended to use secure **https** links to images, since some channels block all external links using unsecure http. 

- Product alias:
    * In the Product master file you can configure alias for products. Using the **Alias** field product search works more accurately, though it is not mandatory to configure it. This alias may contain comma-separated lists. For example, "HP elite 2380 product" can have "laptop, computer, pc" as aliases.

- If not done already, a configuration of product search is required:
	* Use the **(TPG050) Product search configuration** window in the Unit4 Business World web client. Product search configuration can be used to adjust the search features to the customer's needs. This means deciding what to search for and the information displayed to the end user.
	* The suggested way to get started with the Purchasing Assistant is to use the default setup in the **(TPG050) Product search configuration** window. First save this setup (using the correct client) and then publish it. The Product search indexing service will pick this configuration and perform its indexing tasks.
	* As a minimum requirement, Wanda requires these fields to configure Product search. These fields are already configured in the default setup:

		* ```apoprice_currency```
		* ```apoprice_apar_id```
		* ```apoprice_unit_price```
		* ```apoprice_art_descr```
		* ```algunit_description```
		* ```description```
		* ```article```
		* ```apoprice_unit_code```
		* ```apoprice_min_qty```
		* ```image```
			
	* For further details on setting up the product search, see [Reference Manual - Experience Pack - Requisitions 1.5](http://abwdocs.agresso.no/Restricted/Docs/CustDocSpring2017/Spring2017/RefMan_Requisitions_1.5.pdf) (password required)

- The purchase request process for the products made available through Wanda must be defined with a default supplier and the minimum default values to satisfy the applicable account rule for the given product (typically cost center as well as project code, work order code etc. defined).
- Implementation of data control for products/groups is strongly recommended. For example, when a user needs a new laptop, the search results should be limited to only those laptops the user is allowed to purchase.


