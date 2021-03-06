# Schemas

There are two schemas that are necessary for working with Contributors:

* [https://grcschema.org/Person](https://grcschema.org/Person), which provides the schema for a known individual contributor, and
* [https://grcschema.org/Organization](https://grcschema.org/Organization), which provides the schema for a known organizational contributor.

## The difference between a simple User record and a known Person (or Contributor)

There is a huge difference between an account user and a disambiguated (known) Person. A User of an account can request information from the federated database and can change _local_ information within their own application. In order to contribute content _to_ the federated database, the user must be vetted and disambiguated and be registered as a known Person. The content in these wireframes shows _all_ of the content that pertains to a Person, and the User’s content is a subset of that. Throughout this document, we will distinguish between a User’s information and a Person’s information.

### **JSON Schema for User and Person**

The JSON Schema for a User ([GRCschema.org/User](https://grcschema.org/User)) is as follows:

![User JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/UserJSON.png)

The JSON Schema for a Person ([GRCSchema.org/Person](https://grcschema.org/Person)) is as follows:

![Person JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/PersonJSON.png)

The two can be connected through a one-to-one relationship from the User to the Person:

![User to Person](https://www.complianceascode.net/wp-content/uploads/2021/11/User-to-Person.png)

## The difference between an Account and an Organization

Much like the difference between a User and a known Person, an Account is a subset of data that is maintained for an Organization.

### JSON Schema for an Account and Organization

The JSON Schema for an Account ([GRCSchema.org/Account](https://grcschema.org/Account)) is as follows:

![Account JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/AccountJSON.png)

The JSON Schema for an Organization ([GRCSchema.org/Organization](https://grcschema.org/Organization)) is as follows:

![Organization JSON](https://www.complianceascode.net/wp-content/uploads/2021/11/OrganizationJSON.png)

The two can be connected through a one-to-one relationship from the Account to the Organization:

![Account to Organization](https://www.complianceascode.net/wp-content/uploads/2021/11/AccounttoOrganizationERD.png)
