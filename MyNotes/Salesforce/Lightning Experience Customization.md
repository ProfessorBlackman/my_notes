## What Is a Lightning App?

An app is a collection of items that work together to serve a particular function. In Lightning Experience, Lightning apps give your users access to sets of objects, tabs, and other items all in one convenient bundle in the navigation bar.

Lightning apps let you brand your apps with a custom color and logo. You can even include a utility bar and Lightning page tabs in your Lightning app. Members of your org can work more efficiently by easily switching between apps. What’s most important to sales reps? Accounts, events, and organizations. How about sales managers? Reports and dashboards make the top of the list.

Let’s jump into the details.

Each Lightning app has a navigation bar at the top of the page, letting your users:

- Find what they need using item names for easy recognition
- Complete actions and access recent records and lists with a single click
- Personalize the navigation bar to suit the unique way they work

### Things you can put in an app:
- Most standard objects, including Home, the main Chatter feed, Groups, and People
- Your org’s custom objects
- Visualforce tabs
- Lightning component tabs
- Canvas apps via Visualforce tabs
- Web tabs

## Meet The Lightning Experience App  Manager
The App Manager is your go-to place for managing apps for Lightning Experience. It shows all your connected apps and Salesforce apps.
![[Pasted image 20240510162213.png]]
Use the App Manager in Lightning Experience to:
- View all your Salesforce apps.
- Create Lightning apps or connected apps (**1**).
- See which apps are visible in Lightning Experience (**2**).
- Easily manage apps (**3**).
## Tips for creating apps in lightning experience
- Find out what your users priorities are. So you can know what to to add to the nav bar
	- Ask users to post feedback to a Chatter group.
	- Publish polls.
	- Schedule lunch sessions. Everyone likes a free lunch, and nearly everybody is happy to express their opinion.
- Find the common objects and give them high priority.
## Resources

- [_Salesforce Help_: Salesforce App Considerations](https://help.salesforce.com/s/articleView?id=apps_considerations.htm&type=5)
- [_Salesforce Help_: Personalized Navigation Considerations](https://help.salesforce.com/articleView?id=user_userdisplay_tabs_lex_considerations.htm&language=en_US)
- [_Salesforce Help_: Create or Clone a List View in Lightning Experience](https://help.salesforce.com/HTViewHelpDoc?id=customviews_lex.htm&language=en_US)
- [_Salesforce Help_: Edit List View Filters in Lightning Experience](https://help.salesforce.com/HTViewHelpDoc?id=customviews_edit_filters_lex.htm&language=en_US)
- [_Salesforce Help_: Create a List View Chart in Lightning Experience](https://help.salesforce.com/HTViewHelpDoc?id=customviews_listview_chart_create_lex.htm&language=en_US)
- [_Salesforce Help_: Update Records Inline from a List View in Lightning Experience](https://help.salesforce.com/HTViewHelpDoc?id=customviews_edit_inline_listview_lex.htm&language=en_US)

## Customizing Record Page Components and Fields
**The Lightning App Builder lets you:**
- Control which components appear on Lightning pages
- Create custom Lightning pages for different apps and users
- Control which fields appear on record pages

**The page layout editor lets you:**
- Control which lists of related records and custom links users see
- Control which standard and custom buttons appear on records and related lists
- Control which quick actions appear on the page

**These are the parts of a record page that you can customize to create a personalized view for different teams and processes in your org.**

- In the previous unit, you learned about **record highlights** (1) and how to customize the fields it shows using compact layouts. The record highlights area also contains a set of **buttons and actions** (2), which you’ll learn how to customize in a later unit.
- The **Related** tab (3) contains _related lists_, which are lists of other records that are associated with the record you’re viewing. For example, an account can have related products, contacts, opportunities, and other custom records.
- The **Details** tab (4) shows information about a record. By default, fields and links appear here. For example, a contact record detail page shows the name, address, owner, account, and other fields that are used to store information about the contact and other related records.
- ![[Pasted image 20240514134336.png]]

## Resources
- [_Salesforce Help:_ Create and Configure Lightning Experience Record Pages](https://help.salesforce.com/apex/HTViewHelpDoc?id=lightning_app_builder_customize_lex_pages.htm&language=en_US)
- [_Salesforce Help:_ Activate Lightning Experience Record Pages](https://help.salesforce.com/articleView?id=lightning_app_builder_customize_lex_pages_activate.htm)
- [_Salesforce Help:_ Lightning App Builder Considerations](https://help.salesforce.com/apex/HTViewHelpDoc?id=lightning_app_builder_considerations.htm&language=en_US)


## Customizing Buttons and Links
Custom links can link to an external URL, such as www.google.com, a Visualforce page, or your company’s intranet. Custom buttons can connect users to external applications, such as web pages, and launch custom links.
There are three primary types of custom buttons and links that you can create.
- List button—Appears on a related list on an object record page.
- Detail page link—Appears in the Links section of the record details on an object record page.
- Detail page button—Appears in the action menu in the highlights panel of a record page.

## Resources

- [_Salesforce Help_: Define Custom Buttons and Links](https://help.salesforce.com/HTViewHelpDoc?id=defining_custom_links.htm&language=en_US)
- [_Salesforce Help_: Custom Button and Link Samples](https://help.salesforce.com/HTViewHelpDoc?id=links_useful_custom_buttons.htm&language=en_US)
- [_Salesforce Help_: Constructing Effective Custom URL Buttons and Links](https://help.salesforce.com/HTViewHelpDoc?id=custom_links_constructing.htm&language=en_US)
- [_Salesforce Help_: Custom Button Considerations](https://help.salesforce.com/HTViewHelpDoc?id=links_considerations.htm&language=en_US)

## Quick Actions
Quick Actions let your users quickly do tasks, such as create records, log calls, send emails, and more. With custom actions, you can make your users’ navigation and workflow as smooth as possible by giving them quick access to information that’s most important.

### Object-specific actions
Object-specific actions have automatic relationships to other records and let users quickly create or update records, log calls, send emails, and more, in the context of a particular object. For example, you add an object-specific action on the Account object that creates contacts. If a user creates a contact with that action on the detail page for the Acme account, that new contact is associated with Acme. Object-specific actions live on the page layout for the object.

There are several types of object-specific actions.
- **"Create"** actions create records that are automatically associated with related records.
- **"Update a Record"** actions make it easy for users to edit records. You can define the fields that are available for update.
- **"Log a Call"** actions let users enter notes about calls, meetings, or other interactions that are related to a specific record.
- **Custom actions** invoke Lightning components, flows, Visualforce pages, or canvas apps that let users interact with or create records that have a relationship to an object record. If you’re new to Visualforce, don’t worry. 
- **"Send Email"** actions, available only on cases, give users access to a simplified version of the Case Feed Email action in the Salesforce mobile app. 

### Global actions
You create global actions in a different place in Setup than you create object-specific actions. They’re called global actions because they can be put anywhere actions are supported. Use global actions to let users log call details, create records, or send email, all without leaving the page they’re on.