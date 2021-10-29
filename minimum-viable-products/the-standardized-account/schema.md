# Schema

The schema for an account is found in multiple locations:

* [https://grcschema.org/Account](https://grcschema.org/Account), which provides the core schema for an account; and
* [https://grcschema.org/Organization](https://grcschema.org/Organization), which provides the schema for the domain to organization match.
* [https://grcschema.org/User](https://grcschema.org/User), which provides the schema for a typical user found within an ac-count.
* [https://grcschema.org/Group](https://grcschema.org/Group), and [https://grcschema.org/Initiative](https://grcschema.org/Initiative), which provides the schema for grouping users (an initiative is only different in that it has a beginning and end-date) within the account.

The ERD for working with an account looks like the diagram that follows: ![Account ERD](https://www.complianceascode.net/wp-content/uploads/2021/10/AccountSchema.png)

### What needs to be understood about this structure

Organizations exist outside of Accounts. When you think of an organization, think of, say, IBM. It exists whether IBM has an account within this system or not. Then, when someone that has ibm.com in their email address wishes to establish an Account in the system, they can do so, and it is tied to the IBM Organization. And then another person with ibm.com in their email address might want to establish a different account – they can do so – and that account, too, will be linked to the IBM Organization. Both accounts are tied to the IBM Organization through the domain in their email addresses. Each Account can have its own, private, Groups and Initiatives. As well as its own addresses and phone numbers, not directly associated with the formal addresses associated with the Organization.
