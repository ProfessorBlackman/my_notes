**Reference:** https://trailhead.salesforce.com/content/learn/modules/data_modeling/objects_intro?trail_id=force_com_admin_beginner
## Salesforce Objects:
## Definition:
It's just database entities given a fancy name 🙄

### Types of Objects:
- Standard objects
- Custom objects
- external objects
- platform events
- BigObjects

1. **Standard Objects:** Basic objects that come with each instance of Salesforce. E.g.: Account, Contact, Lead, Opportunity.
2. **Custom objects:** Objects that are created by an admin or other Salesforce roles. They store information specific to your company.
If it were a django database, then django_session and django_migrations are standard objects and user, products, etc that a Django developer would create are custom objects.

### Fields:
If Objects are database entities (tables), then fields are the columns.

| Field Type | What is it?                                                                                                                                                            | Can I get an example?                                                                  |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Identity   | A 15-character, case-sensitive field that’s automatically generated for every record. You can find a record’s ID in its URL.                                           | An account ID looks like 0015000000Gv7qJ.                                              |
| System     | Read-only fields that provide information about a record from the system, like when the record was created or when it was last changed.                                | CreatedDate, LastModifiedById, and LastModifiedDate.                                   |
| Name       | All records need names so you can distinguish between them. You can use text names or auto-numbered names that automatically increment every time you create a record. | A contact’s name can be Julie Bean. A support case’s name can be CA-1024.              |
| Custom     | Fields you create on standard or custom objects are called custom fields.                                                                                              | You can create a custom field on the Contact object to store your contacts’ birthdays. |

### best practices to keep in mind as you start customizing your own org.
- **Be thoughtful about names.** Once you start creating a bunch of objects, it can be tempting to give them “lazy” names. So basically same rule as in naming in software development

- **Help out your users.** Even with careful naming, your users might not always be clear about the purpose of a particular object or field. Include descriptions for your custom objects and fields. For specialized or complicated customizations, use help text to give more details. (So basically good documentation and comments just like in software development)

- **Require fields when necessary.** Sometimes, you’ll want to force your users to fill out a field when they’re creating a record on a certain object. Every property needs a price, right? Make important fields required to avoid incomplete data.

## Object Relationships:
It's basically database relationships.

### Types of Relationships:
#### Lookup Relationships:
The default object Account has a lookup relationship with Contact object.This means when you retrieve an account record it will come with its related Contact objects.

### Master-Detail Relationships
Say you are a real estate agency, you have a property object and an offer object which are in a master-detail relationship. This means the master; Property controls certain behaviors of the detail that is offer. Like when you delete a property you would want to delete its offers too, you would do this with such a relationship.

## Schema Builder
Just like the average database visualizing and modelling tool