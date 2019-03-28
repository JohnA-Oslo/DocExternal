# Expenses Assistant

Wanda's Expenses Assistant helps users add trip expenses on-the-fly, both manually and automatically using OCR receipt recognition, to submit expense claims for approval. Travel expense claims for single destination trips may include prefilled data (destination and purpose) if it's based on a travel request.

## System requirements

- Expenses Experience pack version 4.6 or later installed
- Unit4 Me Experience pack version 1.3 or later (latest version recommended)
- Expenses public API exposed, including Expenses and Travel Requests
- Unit4Me service V201501 configured 
- Travel expenses service V201212 configured 

## System setup 

Assign user/role access rights as required for the relevant users to:

* Public APIs in the **(XAG005) Public API access** window on the Business World web client:

    - Expenses  
    - Travel requests
    - Objects

* SOAP APIs on the _**Web services**_ tab in the **(AG65) Role/user based access** or the **(AG68) Menu-based access** window on the Business World Desktop client:

    - Unit4Me service V201501
    - Travel expense service V201212

    For details on setting up the Travel web service, see [Mobile expenses reference manual](http://abwdocs.agresso.no/Restricted/Docs/CustDocSpring2017/Spring2017/RefMan_MobileExpenses_Spring2017.pdf) (password required).

* Report objects in the **(XAG002) Object access** window on the Business World web client:

  - Attributes
  - Attribute values
  - Travel type

> The **Travel type** report object is not included within the M6SU3 version of Unit4 Business World as default. A custom setup script is available as part of the M6SU3 package to import the required data. The required data will be included within the upcoming M6 update (fall 2018).

For more details on the used service endpoints, see the [Travel and expenses service reference](expenses-services.md).


## Receipt recognition setup
Set up automated receipt recognition according to the  [Expenses mobile application reference manual](http://abwdocs.agresso.no/Restricted/Docs/CustDocSpring2017/Spring2017/RefMan_MobileExpenses_Spring2017.pdf) (password required). A summary of the procedure is:

* Activate the receipt recognition system parameter **TT\_RECEIPT_RECOGNITION** (default off)
* Define a confidence level threshold via the **TT\_CONF\_LEVEL_THR parameter** (or use default)
* Configure the following system parameters:

            TT_WEB_EXT_TRANS
            TT_MOBILE_DOCTYPE
            TT_RECEIPT_DOCTYPE
            TT_MILEAGE_UNIT_NAME (if mileage is used)
            TT_MILEAGE_UNIT_FACTOR (if mileage is used)
            TT_MIL_EXP_TYPE (if mileage is used)

* Map expense types to receipt types. For optimal performance, make sure that every receipt type is properly mapped to an expense type. This might require expense type re-implementation. You should map one receipt to one expense type whenever possible, unless a domestic/abroad split is necessary.


