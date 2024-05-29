## What Is a User?
A user is anyone who logs in to Salesforce. Users are employees at your company, such as sales reps, managers, and IT specialists, who need access to the company's records. You can also have external users, such as end customers, prospects, and partners who access Experience Cloud sites.

A user account exists for every user in Salesforce. The user account identifies the user, and the user account settings determine what features and records the user can access. Each user account contains at least the following.
- Username  
- Email Address  
- User's First Name (optional)  
- User's Last Name  
- Alias  
- Nickname  
- License  
- Profile  
- Role (optional)  

You view and manage users from the Users page in Setup. The user list shows all the users in Salesforce. From the list, you can:
- Create one or more users.  
- Reset passwords for selected users.  
- View a user’s detail page by clicking the name, alias, or username.  
- Edit a user’s details.  
- Log in as any user if the system permission is enabled or if the user has granted you system administrator login access.

## Key Terms

We’ve thrown many terms at you as we’ve described the background information you need to get started adding users. Here are some key terms you should know and their definitions.

### Usernames

Each user has both a username and an email address. The username must be formatted like an email address and must be unique across Salesforce. It can be the user’s email address, so long as it’s unique.

### User Licenses

A user license determines which features the user can access in Salesforce. For example, you can allow users access to standard Salesforce features and Chatter with the standard Salesforce license. But if you want to grant a user access to only some features in Salesforce, you have a host of licenses to choose from. For example, if you have to grant a user access to Chatter without allowing them to see any data in Salesforce, you can give them a Chatter Free license.

To learn more about licenses at Salesforce, check out [Salesforce Licensing](https://trailhead.salesforce.com/content/learn/modules/salesforce-licensing).

### Profiles

Each user has one profile that defines default settings. It’s possible to use profiles to grant permissions and access to users. However, we recommend you grant users the Minimum Access - Salesforce profile, and then use permission sets and permission set groups to grant users the permissions they require.

**What should be in a permission set vs. a profile?**

  

| **Permission Set**                  | **Profile**             |
| ----------------------------------- | ----------------------- |
| User, object, and field permissions | Default record types    |
| Custom permissions                  | Default assigned apps   |
| Connected app access                | Page layout assignments |
| Apex class access                   | Login hours             |
| Visualforce page access             | Login IP ranges         |
| Tab settings                        |                         |

### Roles
Roles determine what users can see in Salesforce based on where they’re located in the role hierarchy. Users at the top of the hierarchy can see all the data owned by users below them. Users at lower levels can't see data owned by users above them, or in other branches, unless sharing rules grant them access. Roles are optional but each user can have only one. If you have an org with many users, you may find it easier to assign roles when adding users. However, you can set up a role hierarchy and assign roles to users at any time. Roles are only available in Professional, Enterprise, Unlimited, Performance, and Developer editions of Salesforce.

### Alias
An alias is a short name to identify the user on list pages, reports, or other places where their entire name doesn't fit. By default, the alias is the first letter of the user's first name and the first four letters of their last name.

## Guidelines for Adding Users

You have many options for adding users and multiple tools at your disposal in Salesforce. Here are some guidelines to help you get started.
- **Username:** Each user must have a username that is unique across all of Salesforce.  
- **Username format:** Users must have a username in the format of an email address (jdoe@domain.com), but they don't have to use a real email address. They can use their email address if they wish as long as their email address is unique across all of Salesforce.  
- **Email:** Users can have the same email address across organizations.  
- **Passwords:** Users must change their password the first time they log in.  
- **Login link:** Users can only use the login link in the sign-in email once. If a user follows the link and doesn’t set a password, you (the admin) must reset their password before they can log in.

## Add Users

You may have already added some users if you launched the Setup Wizard. However, you’ll probably need to add users in the future, especially as your company grows and you hire more employees.

Depending on the size of your organization or your new hire onboarding process, you may add users one at a time or several at a time. You can do either in Salesforce. The maximum number of users you can add is determined by your Salesforce edition and the number of user licenses you purchase.
To add users:
1. From Setup, in the Quick Find box, enter `Users`, and then select **Users**.  
2. Click **New User** to add a single user, or click **Add Multiple Users** to add up to 10 users at a time.![Create a New User screen.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_user_setup_mgmt/lex_implementation_user_setup_mgmt_adding_users-hoc/images/80216063dad01fb01c00e813a17946df_kix.b5mw1lmdebcb.png)  
    
3. Enter each user’s name, email address, and a unique username in the form of an email address. By default, the username is the same as the email address, but you can overwrite this.  
4. Select the user license you want to associate with the users you create (the license determines which profiles are available for each user).  
5. Select a profile.  
6. Select **Generate password and notify user immediately** to email a login name and temporary password to each new user.  
7. Click **Save**.

## Freeze a User

Pop quiz: You get an email saying a user’s Salesforce account may have been compromised. What do you do?

Well, because you’re a seasoned admin, you don’t panic. You know you can head right over to Setup and ensure there’s no risk from this user’s account.

1. From Setup, in the Quick Find box, enter `Users`, and then select **Users**.  
    
2. Click the username of the account you want to freeze.  
    
3. Click **Freeze** to prevent the user from logging in to the account.![User record screen with a callout on the Freeze button.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_user_setup_mgmt/lex_implementation_user_setup_mgmt_adding_users-hoc/images/3b7f87cfefd697ed46cc5cceaac00b9f_kix.sde2n3y7rrjo.png)  
    

Now the user’s compromised account is frozen to prevent any trouble, and you can relax knowing your org is secure. Freezing accounts can also come in handy when a user leaves your company and you don’t want them logging in, but you have some cleanup to do before deactivating them.

## Deactivate a User

What’s the difference between freezing and deactivating users? Both actions prevent the user from logging in to their account. But freezing user accounts doesn’t make their user licenses available in your organization. That’s why you’ll want to deactivate a user after they leave your company.

1. From Setup, in the Quick Find box, enter `Users`, then select **Users**.  
    
2. Click Edit next to a user’s name.  
    
3. Deselect the **Active** checkbox, and then click **Save**.![Edit User screen with a callout on the disabled Active checkbox.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_user_setup_mgmt/lex_implementation_user_setup_mgmt_adding_users-hoc/images/d017211bf3836b1552200417ceb8b90d_kix.12eep0ljtx0g.png)  
    

You can deactivate users, but you can’t delete them. Why is this? Deleting a user can result in orphaned records and the loss of critical business information. So to ensure the user’s records and data are preserved, you deactivate users instead.

Now you know how to add users to Salesforce, as well as freeze and deactivate users when necessary. In the next unit, you learn how to keep your data safe by configuring what your users can access.

## Resources

- [_Salesforce Help_](https://help.salesforce.com/s/articleView?id=sf.users_mgmt_overview.htm&_ga=2.182300455.1848710669.1697469711-1555315375.1693603930)[: Manage Users](https://help.salesforce.com/s/articleView?id=sf.users_mgmt_overview.htm&_ga=2.182300455.1848710669.1697469711-1555315375.1693603930)
- [_Salesforce Help_](https://help.salesforce.com/s/articleView?id=sf.admin_users.htm&_ga=2.182300455.1848710669.1697469711-1555315375.1693603930)[: View and Manage Users](https://help.salesforce.com/s/articleView?id=sf.admin_users.htm&_ga=2.182300455.1848710669.1697469711-1555315375.1693603930)
- [_Salesforce Help_](https://help.salesforce.com/s/articleView?id=sf.users_licenses_overview.htm&_ga=2.179302052.1848710669.1697469711-1555315375.1693603930)[: Licenses Overview](https://help.salesforce.com/s/articleView?id=sf.users_licenses_overview.htm&_ga=2.179302052.1848710669.1697469711-1555315375.1693603930)
- [_Salesforce Help_](https://help.salesforce.com/s/articleView?id=000389249&type=1&_ga=2.179302052.1848710669.1697469711-1555315375.1693603930)[: User Management Best Practice Guide](https://help.salesforce.com/s/articleView?id=000389249&type=1&_ga=2.179302052.1848710669.1697469711-1555315375.1693603930)


# Control What Your Users Can Access

## Introduction to Data Security

Now that you know how to add users, you probably want to know how to ensure they can see what they need to see and only what they need to see. In this unit, you learn how to configure your users’ access to your Salesforce records, so they can access only the information they need.

Salesforce includes simple-to-configure security controls that make it easy to specify which users can view, create, edit, or delete any record or field in the app. You can configure access at the level of the organization, objects, fields, or individual records. By combining security controls at different levels, you can provide just the right level of data access to thousands of users without having to specify permissions for each user individually.

In this unit, we cover the levels of data access and some of the available features for managing object, record, and field access. But we’re only scraping the surface here. For more info and hands-on practice with controlling access to data, check out [Data Security](https://trailhead.salesforce.com/content/learn/modules/data_security).

## Levels of Data Access

You can configure access to data in Salesforce at four main levels.

### Organization

At the highest level, you can secure access to your organization by maintaining a list of authorized users, setting password policies, and limiting login access to certain hours and certain locations.

### Objects

Object-level security provides the simplest way to control which users have access to which data. By setting permissions on a particular type of object, you can prevent a group of users from creating, viewing, editing, or deleting any records of that object. For example, you can use object permissions to ensure interviewers can view positions and job applications but not edit or delete them. We recommend you use permission sets and permission set groups to configure object permissions.

### Fields

Field-level security restricts access to certain fields, even for objects a user has access to. For example, you can make the salary field in a position object invisible to interviewers but visible to hiring managers and recruiters. Field permissions are also configured in permission sets.

### Records

To control data with greater precision, you can allow particular users to view an object, but then restrict the individual object records they're allowed to see. For example, record-level access allows interviewers to see and edit their own reviews, without exposing the reviews of other interviewers. You set the default level of access that users have to each others’ records using organization-wide defaults. Then, you can use the role hierarchy, sharing rules, manual sharing, and other sharing features to open up access to records.

Let’s take a closer look at two features used to configure data access: permission sets and organization-wide defaults.

## Permission Sets

Permission sets are collections of settings and permissions that determine what users can do in Salesforce. Use permission sets to grant access to objects, fields, tabs, and other features and extend users’ access without changing their profiles.

What’s so great about permission sets? Because you can reuse smaller permission set building blocks, you can avoid creating dozens or even hundreds of profiles for each user and job function. That’s why we recommend you assign users the Minimum Access - Salesforce profiles, and then use permission sets and permission set groups to manage your users’ access.

When you create permission sets, include all permissions necessary for a job or task.