# API style guide and standards manual

This sample is the style guide and standards manual I wrote for an API documentation program. It defines how writers document each part of an API reference.

## About this sample

The project details are as follows:

- **Audience:** Technical writers and product analysts documenting APIs
- **Problem:** Writers needed consistent standards for API reference content as a new API program began
- **My role:** Defined the standards and wrote the manual as lead writer
- **Collaborators:** Technical writing manager and director of development
- **Tools and standards:** OpenAPI and Markdown
- **Outcome:** Established consistent API documentation across the product suite

## Excerpts

The following excerpts show the reasoning behind two of the standards. Product and platform names have been removed.

### Resource collection descriptions

Each group of endpoints is organized by a developer-determined group that limits the number of endpoints displayed in the API user interface. The description for this group should provide a high-level overview of the endpoints a developer can expect to find in a resource collection.

- Always start the description with "Endpoints for…".
- Use complete sentences.
- Don't limit your description in a way that would require you to make revisions.

!!! note
    While some APIs start with a simple present tense verb, this creates an issue when new endpoints are added that use different methods. For example, "Sends and receives payment information" must be revised if a DELETE endpoint is added. Once all methods are used in a resource collection, each description would need to read "Creates, receives, updates, and deletes payment information," which is wordy and adds unnecessary detail.

**Examples:**

| Resource collection | Description |
| --- | --- |
| Accounts | Endpoints for account-level information available for all accounts across the financial institution and individually for selected accounts. |
| External Accounts | Endpoints for accounts managed by the financial institution but controlled by an external service, such as a credit card processor. |
| Utilities | Endpoints for access token management and other calls that assist with technical requirements used to manage the API service. |

### Endpoint titles

Each endpoint title must be unique to the resource collection and clearly describe the business function performed by the call.

- Capitalize titles according to current heading conventions.
- Follow the CRUD method for title creation, in which the endpoint's method determines the verb used at the beginning of the title.

| Method | Corresponding verb | Example |
| --- | --- | --- |
| GET | Retrieve or Search for | Retrieve Deposit Accounts by Account Type<br>Search for a Deposit Account |
| DELETE | Delete | Delete Bill Memo for a Loan Account |
| POST | Create New | Create New Combined Statement |
| PATCH | Update | Update Phone Number for a Customer/Member |
| PUT | Create New or Update | Create New Loan Account<br>Update Rate Index for a Financial Institution |

!!! note
    Use "Search for" only when a GET call includes parameters intended to return a single record. GET endpoints designed to return a list of records, such as a list of branches for an institution, always use "Retrieve."

**Exceptions:** In some cases, the business function doesn't match the method used to perform it. In those cases, choose the verb that best represents the business function, not the method. For example, creating a new account is always called origination in the product, so those endpoint titles follow the product standard:

- Deposit Account Origination
- Loan Account Origination
- Safe Deposit Account Origination
