# Set Up the Exchange Rate
## Enable Multiple Currencies

1. Click the **gear icon** ![Setup icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/set-up-the-exchange-rate/images/85611ddd90d69912997b57ea6502928f_gear-3.png) and select **Setup**.
2. Enter `Company Information` in the Quick Find box and select **Company Information**.
3. Click **Edit**.
4. Ensure Locale is set to **English (United States)** and Currency Locale is set to **English (United States) - USD**.  
    Note: Don't worry, you can change the currency back to your default currency after completing this project.
5. Within the Currency Settings section, select the **A****ctivate Multiple Currencies** box.
6. Click **Save**.
7. From the Company Information page, click the **Currency Setup** button.
8. Click **New** in the Active Currencies section.
9. Set up the Euro with the following information.
    
    

| Field           | Value          |
| --------------- | -------------- |
| Currency Type   | **EUR – Euro** |
| Conversion Rate | 1.5            |
| Decimal Places  | 2              |

10. Click **Save**.

Test the exchange rate on a new opportunity.

# Update the Exchange Rate with ACM

Another way to work with the exchange rate is through the advanced currency management tool. You can manage rates with specific dates.

## Enable Advanced Currency Management

1. Click the **gear icon** ![Setup icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/update-the-exchange-rate/images/85611ddd90d69912997b57ea6502928f_gear-3-2.png) and select **Setup**.
2. Enter `Manage Currencies` in the Quick Find box and select **Manage Currencies**. Note: If Manage Currencies does not appear in your Quick Find search, enter `Company Information`, and click **Currency Setup**.
3. Click **Enable** under Advanced Currency Management if not enabled.
4. On the confirmation that appears, select the **Yes, I want to enable Advanced Currency Management** box, and then click **Enable**. Note: Dependent on your browser, you may need to click **Open** and a new tab will open in Classic.

Update the Euro exchange rate with a start date.

1. Click **Manage Dated Exchange Rates**, and click **Continue** on the splash screen.
2. Click **New** **Exchange Rates**, and then complete the fields.
    - Start Date: (first day of next month)
    - Euro: `1.13`
3. Click **Save.** If you are in a Classic tab, close it.

## Edit the Euro Currency Test Opportunity

Next, edit the close date on the Euro opportunity to see how the converted amount changes depending on the exchange rate.

1. Click the **App Launcher** ![App launcher icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/update-the-exchange-rate/images/10d4b68878a5c78f9499b116879d2c3d_cjgntcbqr-000-e-0-v-4-babw-9-zmc-1-5-2.png) and select **Sales**.
2. Click the **Opportunities** tab.
3. From the Recently Viewed opportunities list, click **Euro Currency Test** and click the **Details** tab to compare the converted amount to the one you noted earlier.
4. Click **Edit**.
5. Change the **Close Date** to the first date of next month.
6. Click **Save**.

Notice how the converted amount has changed because the new exchange rate is being used.

Now that we have applied the advanced currency management option, let’s continue customizing, but this time for specific profiles. The VP of Support has requested a unique home page for the Support team. Let’s customize it!

# Customize the Home Page
## Create a New Home Page Using Lightning App Builder

1. From Setup, enter `Lightning App` in the Quick Find box and select **Lightning App Builder**.
2. Click **New**.
3. Select **Home Page**, then **Next**.
4. Assign the label `Support Home Page`, then click **Next**.
5. Click the **Standard Home Page** template.
6. Click **Done**.

Display the five most recent cases.

1. Drag the **Recent Items** component to any spot in the canvas.
2. For Custom Label, enter `Recent Cases`.
3. Click **Select**.
4. Move the currently selected object, **API Anomaly Event Store**, into the Available column by selecting it and clicking the Left Arrow.
5. Select **Case** from Available and click the Right Arrow to move it into the Selected Column.
6. Click **OK**.
7. For Number of Records to Display, enter `5`.

Show Chatter posts where the support rep is @mentioned.

1. Drag the **Chatter Feed** component to any spot in the canvas.
2. For Feed Type, select **To Me**.

Show today’s tasks and upcoming events.

1. Drag the **Today’s Tasks** component to any spot in the canvas.
2. Drag the **T****oday’s Events** component to any spot in the canvas.

Display a link to the Salesforce trust site.

1. Drag the **Rich Text** component into the Today’s Tasks box. A text entry field will appear below the box.
2. In the text entry field, enter `Be sure to check the Salesforce Trust site.`
3. Highlight the text "**Salesforce Trust**" and select the **Link** button.
4. For URL, enter `https://trust.salesforce.com`.
5. Click **Save**.

## Activate the new Home Page

1. Click **Save** in the upper right corner, then **Activate**.
2. Click **App** **and** **Profile**.
3. Click **Assign to Apps and Profiles**.
4. Select **Service Console** and click **Next**
5. Select **Custom: Support Profile** and **System Administrator**.
6. Click **Next** and **Save.**  
    **![Home page layout with custom features enabled.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/customize-the-home-page/images/049a3748514a5b81d674942ebe2b909e_4-a-5972-e-0-77-c-9-4849-9104-1-b-0-b-91-d-05-ee-4.png)**Note: Your layout may differ.
7. Click the **<-** **Back** button to leave the Lightning App Builder.

Your users with the support profile assigned now have a personalized home page. Now you see that a request has been sent your direction by the VP of Sales. Sales reps need quick access to industry-specific accounts. Let’s address this request and create a custom account list view to meet their needs.

# Create a Unique Account List View

Sales users need quick access to accounts in two specific industries. Let’s customize a list view so users can conveniently access these accounts.

## Create a New List View

Create a list view to display accounts in the biotechnology and energy industries.

1. Click the **App Launcher** ![App Launcher icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/create-a-unique-account-list-view/images/10d4b68878a5c78f9499b116879d2c3d_cjgntcbqr-000-e-0-v-4-babw-9-zmc-1-5-3.png) and select **Sales**.
2. Click the **Accounts** tab.
3. Click the **List View** icon ![Gear icon with down arrow](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/create-a-unique-account-list-view/images/3033264e42ef3fb69c85a648470eaf32_grear-icon-with-arrow-2.png) for List View Controls.
4. Select **New**.
5. Complete the New List View section.
    - List Name: `Energy and Biotech Accounts`
    - Who sees this list view: **All users can see this list view** 
6. Click **Save**.

Edit the list filters.

1. If you don’t see the Filters section on the right, click the **Filters** icon ![Filter icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/create-a-unique-account-list-view/images/720592c1e395bd385514ee7a57fceef9_cjgntjmxw-000-g-0-v-4-budai-0-afg.png) .
2. Filter by Owner: **All accounts**.
3. Click **Done**.
4. Click **Add Filter**.
    - Field = **Industry**
    - Operator = **equals**
    - Value = `Energy, Biotechnology`
5. Click **Done**.
6. Click **Save**.

Choose fields to display.

1. Click the **gear** icon ![Gear icon with down arrow](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/create-a-unique-account-list-view/images/3033264e42ef3fb69c85a648470eaf32_grear-icon-with-arrow.png) in the upper-right for List View Controls, then select **Select Fields to Display**.
2. Choose **Industry** from the Available Fields list, then click the **Add** arrow (**>**).
3. Click **Save**.
4. Click **Hide Filters** (the funnel icon in the upper right).

You have successfully created a customized list view. Users can now quickly access all of the biotech and energy accounts. The VP of Sales loves the new list view and now wants a way for their reps to collaborate. Chatter groups to the rescue!

# Create Chatter Groups

Chatter is a great collaboration tool for your users. Through the use of Chatter groups, users can communicate and share. Chatter groups are classified as either public or private. Public means anyone can see and add posts, comments, and files. Anyone can join a public group. Private means only group members can see and add posts, comments, and files. People must ask the group's [owner or managers](https://help.salesforce.com/articleView?id=collab_group_roles_overview.htm&type=5) to join a private group. But first, the groups need to be created.

## Create Chatter Groups for All Sales and All Support

First, create the All Sales Chatter group.

1. Click the **App Launcher** ![App Launcher icon](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/create-chatter-groups/images/10d4b68878a5c78f9499b116879d2c3d_cjgntcbqr-000-e-0-v-4-babw-9-zmc-1-5-4.png) .
2. Enter `Groups` in the Search apps and items... box and select **Groups**.
3. Click **New**.
4. Fill in the new group information:
    - Group Name: `All Sales`
    - Description: `Collaboration space for all things related to Sales`
    - Access Type: **Public**
5. Click **Save & Next**.
6. Skip adding a group photo by clicking **Next**.
7. Skip adding members for now and click **Done**.

Post a welcome message to the All Sales group.

1. In the “Share an update…” section, post the following message: `Welcome to the All Sales group, which replaces the All Sales email list.`
2. Click **Share**.

Next, create the All Support Chatter group.

1. Click the **Groups** tab, click **New**.
2. Fill in the new group information:
    - Group Name: `All Support`
    - Description: `Collaboration space for all things related to Support`
    - Access Type: **Private**
3. Click **Save & Next**, **Next**, then **Done**.
4. Post a welcome message to the All Support group. In the "Share an update..." section, post the following message: `Welcome to the All Support group, which replaces the All Support email list.`
5. Click **Share**.

Post a link to the All Support group that explains how to use @mentions.

1. On the All Support group page, post the following message: `Hi Support people! Here is some quick training on how to use the @mention feature, to bring another user or even an entire group into a Chatter conversation.`
2. Click **Enter** to move the cursor to the next line.
3. Add the link: `https://help.salesforce.com/articleView?id=collab_add_mentioning_people.htm&type=5`.  
    Note: Ensure you don't add any extra line breaks. Copy the text from step 1 then on the next line, add the URL. See screenshot below.  
    ![Successful Chatter post with a link to the Help and Support page.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/projects/prepare-your-salesforce-org-for-users/create-chatter-groups/images/ce8de52af38e1e4b531c279ad33620ed_screen-20-shot-202021-03-02-20-at-202-13-00-20-pm.png)
4. Click **Share**.

