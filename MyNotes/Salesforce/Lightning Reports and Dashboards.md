

## What Is a Report?

In its simplest form, a report is a list of records (like opportunities or accounts) that meet the criteria you define. But reports are much more than simple lists. To get the data you need, you can filter, group, and do math on records. You can even display them graphically in a chart!
Every report is stored in a folder. Report folders determine how reports are accessed, and who can access them to view, edit, or manage. Folders can be public, hidden, or shared. You control who has access to the contents of the folder based on roles, permissions, public groups, territories, and license types. You can make a folder available to your entire organization, or make it private so that only the owner has access.

## What Is a Dashboard?

A dashboard is a visual display of key metrics and trends for records in your org. Each dashboard widget is based on a single source report. You can use the same or different source reports for the various widgets in a dashboard (for example, use the same report in a bar chart and pie chart). By adding multiple dashboard widgets to a single dashboard page, you can create a powerful visual display of data on a common theme, such as sales performance or customer support.

Like reports, dashboards are stored in folders. If you have access to a folder, you can view its dashboards. To view the individual dashboard widgets, you also need access to the underlying reports.

Each dashboard has a running user, whose security settings determine which data to display in a dashboard. If the running user is a specific user, all dashboard viewers see data based on the security settings of that user—regardless of their own personal security settings. For this reason, you’ll want to choose the running user wisely, so as not to open up too much visibility. For example, set the sales manager as the running user for a leader board for her team. This allows her team members to view the leader board for their individual team, but not other teams.

Dynamic dashboards are dashboards for which the running user is always the logged-in user. This way, each user sees the dashboard according to his or her own access level. If you’re concerned about too much access, dynamic dashboards might be the way to go.

## Resources
- [_Salesforce Help:_ Reports and Dashboards Overview](https://help.salesforce.com/articleView?id=analytics_overview.htm&language=en_US&_ga=2.132959630.146644227.1684260886-138552625.1654533480)[](http://salesforce.vidyard.com/watch/6sEtckzxSxa2uwuKFk6DwW?_ga=2.132959630.146644227.1684260886-138552625.1654533480&_gl=1*1h89zhk*_ga*MTM4NTUyNjI1LjE2NTQ1MzM0ODA.*_ga_H6M98GGB18*MTY4NDQ0MTE5OS43OC4xLjE2ODQ0NDEyMDYuMC4wLjA.)
- [_Salesforce Video Series:_ Get Started with Lightning Experience Reports and Dashboards](http://salesforce.vidyard.com/watch/6sEtckzxSxa2uwuKFk6DwW?_ga=2.132959630.146644227.1684260886-138552625.1654533480&_gl=1*1h89zhk*_ga*MTM4NTUyNjI1LjE2NTQ1MzM0ODA.*_ga_H6M98GGB18*MTY4NDQ0MTE5OS43OC4xLjE2ODQ0NDEyMDYuMC4wLjA)
- [_Salesforce Help:_ Create a Custom Report Type](https://help.salesforce.com/s/articleView?id=sf.reports_defining_report_types.htm&type=5https://help.salesforce.com/s/articleView?id=sf.reports_defining_report_types.htm&type=5)

## Creating Reports with Reports builder
### Create a Report
1. In your Trailhead Playground, click the App Launcher and go to Reports.
2. Click **New Report**.
3. Select the **Accounts** report type.  
    When you choose a report type, you select the records and fields you’re able to see in your report. If you don’t see the report type you’re looking for right away, try changing the category or filtering by objects or fields in the Create Report window.
4. Click **Start Report**.  
    The report builder opens to show settings on the left and a report preview on the right. Whether you see data in the preview depends on the underlying data and the filters that are applied. For now, if you don’t see any data in the preview area, click the **All Time** link to apply a standard filter that shows results for all time.
    ![[Pasted image 20240520101551.png]]

5. Click **Save**.
6. Save the report as `Direct Customer Accounts` and accept the auto-generated unique name.
7. Click **Save**.

Before leaving the report builder, let’s take a minute to find out what you can do in the left panel. 

- The Outline tab lets you group the report by rows (summary report) or rows and columns (matrix report). We explore these options in the Format Reports unit.
![[Pasted image 20240520101728.png]]
- The Filters tab lets you apply standard filters and add field filters, filter logic, cross-filters, and row limit filters. The number to the right of the tab name indicates the number of filtering restrictions that are currently applied to the report. We explore filtering options in the Filter Your Report unit.  
    ![Filters tab in the report builder.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_using_report_builder/images/b4abdd9250d9f71c705304324b465590_38785-df-0-adc-9-4-b-87-9-a-09-9-ca-1-a-3-dc-6-ca-3.png)
- The Fields panel contains a list of all the fields you can add to your report. The available fields depend on the report type. To show the fields list, click the right-facing arrow, or to hide the list, click **X**.  
      
    To add a field on the Outline or Filtering tab, start typing in the search box and then select from the list of matching fields. Alternatively, find the field in the list on the Fields list and drag it to the Outline or Filter tab or directly to the report preview.![Fields tab collapsed and expanded, showing how to drag a field to add it as a column.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_using_report_builder/images/066ce4abfa43612bd03badb385d7b042_5-dd-7-f-3-bd-5-c-80-4-d-2-f-b-16-f-3-b-3-a-7-f-9-fb-61-d.png)

When you’re ready to leave the report builder, click **Run** to execute the report and go to the report run page. 

![Report run page showing a sample report.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_using_report_builder/images/4cc7efc415db59a143002b7888e1f7d1_4766-cffc-4-f-1-c-4-cde-b-227-9-e-357-f-6-cfda-4.png)

## Resources

- [_Salesforce Help:_ Reports and Dashboards Overview](https://help.salesforce.com/articleView?id=analytics_overview.htm&language=en_US&_ga=2.132959630.146644227.1684260886-138552625.1654533480)
- [_Salesforce Video Series:_ Get Started with Lightning Experience Reports and Dashboards](http://salesforce.vidyard.com/watch/6sEtckzxSxa2uwuKFk6DwW?_ga=2.132959630.146644227.1684260886-138552625.1654533480&_gl=1*1h89zhk*_ga*MTM4NTUyNjI1LjE2NTQ1MzM0ODA.*_ga_H6M98GGB18*MTY4NDQ0MTE5OS43OC4xLjE2ODQ0NDEyMDYuMC4wLjA)

## Add Filters
You can filter the data in a report using the following filter options.

| Filter Type     | Description                                                                                                                                                                                                                                                                                                                                                               |
|:--------------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Standard Filter | Most objects include standard filters. Different objects have different standard filters, but most include the standard filters Show Me and Created Date. Show Me filters the object around common groupings (like My accounts or All accounts). Date Field filters by a field (such as Created Date or Last Activity) and a date range (such as All Time or Last Month). |
| Field Filter    | \|Field filters are available for reports, list views, workflow rules, and other areas of the application. For each filter, set the field, operator, and value. To add a field filter, use the search bar in the Filters tab or drag the field from the Fields list.                                                                                                      |
| Filter Logic    | Add Boolean conditions to control how field filters are evaluated. You must add at least 1 field filter before applying filter logic. Filter logic applies to field filters, but not standard filters.                                                                                                                                                                    |
| Cross Filter    | Filter a report by a child object using WITH or WITHOUT conditions. Add subfilters to further filter by fields on the child object. For example, if you have a cross filter of Accounts with Opportunities, click **Add Opportunity Filter** and create the Opportunity Name equals ACME subfilter to include only those opportunities.                                   |
| Row Limit       | For ungrouped (tabular) reports, select the maximum number of rows to display, choose a field to sort by, and specify the sort order. You can use a tabular report as the source report for a dashboard table or chart component if you limit the number of rows it returns.                                                                                              |
Let’s see how to tune report results by adding a filter to show only direct customers.

1. Go to the Reports, open the `Direct Customer Accounts` report, and click **Edit**.
2. Click **Filters**.
3. Click the **Show Me** standard filter, select **My accounts**, and click **Apply**.
4. In the Filters tab, click **Add filter**.
    1. Choose the **Type** field.
    2. Set the filter operator to **equals**.
    3. Under Value, select **Customer - Direct**, and click **Apply**.
5. Click **Save & Run**.
**For more operators:**  [Filter Operators Reference](https://help.salesforce.com/HTViewHelpDoc?id=filter_operators.htm&language=en_US).

## Use Cross Filters
These filter types allow you to extend your reports to objects related to the original objects defined in the report type. Cross filters help you fine-tune your results without writing code or using formulas. The most common use case is exception reporting.
1. Go to Reports and click **New Report**.
2. Select the **Accounts** report type and click **Start Report**.
3. Click **Filters**, then set the Show Me filter to **All accounts** and the Created Date range to **All Time**.
4. On the Filter tab, click the More Actions arrow and select **Add Cross Filter**.

![Add cross filter menu item.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_filter_your_report/images/832198505f56d8f1d15eb028656302a7_1692288231986.png)

5. Select a parent object from the **Show Me** dropdown list. Your choice determines which related objects you see in the child object list. Select **Accounts**.

6. Choose **with** as the operator.

7. Select a child object from the **Secondary Object** dropdown or search by its name. Select **Opportunities** and click **Apply**.  
![Settings to create a cross filter.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_filter_your_report/images/ab801a95ec1519d5f4dc7e2ee08b1c84_4-e-8-cc-76-c-ec-9-a-4-fcc-8-bfa-5-b-09-e-3-c-2-f-947.png)

8. Optionally add subfilters:

1. Click in the **Add Opportunities Filter** search box.
2. Select a field. The child object in the cross filter determines the available fields. For example, if your cross filter is Accounts with Opportunities, you can use opportunity fields for your subfilter. Select **Stage** for our subfilter.
3. Select **equals** for the operator.
4. Under Value(s), select **Prospecting**, **Qualification**, **Needs Analysis**, and **Value Proposition**.
5. Click **Apply**.  
    ![Interaction to define a subfilter with selection of multiple stages.](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_filter_your_report/images/5d472c4f058a7584c431ba2ae8b1c8d5_ceaf-0-d-3-d-f-812-4549-ad-50-0-cebcc-9283-a-6.png)

9. Click **Save**.

10. Name the report `Accounts with Early Stage Opportunities`, and accept the default report unique name.

11. Click **Save**.

## Use Filter Logic
Filter logic lets you apply filters based on conditions.
Create an Opportunities report. First set the Close Date to **All Time** so you can see some data in this sample report. 
Then set up two field filters:
1. Amount greater than 100000.
2. Probability (%) greater than 50.
With this setup, results are returned if the data matches both 1 and 2. But we want to see results if the data matches either or both of the filters. 
In the Filters pane, Click the More Actions arrow and select **Add Filter Logic**.
![](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_filter_your_report/images/39ed84f24e2b3e0ce478ac786e790c28_th-246-filter-logic.jpg)
Change 1 AND 2 to 1 OR 2 and click **Apply**. Now Erin sees report results if the opportunity amount is more than $100,000 or the probability is greater than 50% .
These operations are supported in filter logic. You can use parentheses for grouping, for example, (1 OR 2) AND 3 AND NOT 4.

| Operator | Definition                                                                                                                                                         |
|:-------- |:------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| AND      | Finds records that match both values.                                                                                                                              |
| OR       | Finds records that match either value.                                                                                                                             |
| NOT      | Finds records that exclude values. You can exclude values by using NOT in your filter logic or by using not equal to or does not contain in the filter definition. |

## Lock Filters on the Report Run Page

When you add filters in the report builder, the filter values become available for selection on the report run page. The person viewing the report can select filter values that are different from the ones set in the report builder.

But what if you don’t want anyone to change the filter value on the report run page? You can lock filter values
![[Pasted image 20240527103800.png]]

## Use Report Formats
There are three report formats available: Tabular, Summary, and Matrix. Tabular is the default format.

| Report Format | Primary Use Case                       | Supported in Dashboards | Report Charts Supported | Bucket Fields | Formulas    | Cross-Object Formulas* |
| ------------- | -------------------------------------- | ----------------------- | ----------------------- | ------------- | ----------- | ---------------------- |
| Tabular       | Make a list                            | :luc_check:             |                         | :luc_check:   |             |                        |
| Summary       | Group and summarize                    | :luc_check:             | :luc_check:             | :luc_check:   | :luc_check: |                        |
| Matrix        | Group and summarize, by row and column | :luc_check:             | :luc_check:             | :luc_check:   | :luc_check: |                        |

## Tabular Reports

Tabular reports are the simplest and fastest way to look at your data. Similar to a spreadsheet, they consist simply of an ordered set of fields in columns, with each matching record listed in a row. They're often best used for tasks like generating a mailing list. When Lincoln asked Maria for a report of all open opportunities, Maria knew that a tabular report would fit the bill.

1. On Reports, click **New Report**, choose the ‘Opportunities’ report type, and click **Start Report**.
2. Click **Filters**, then apply the following filters:
    1. For the Show Me standard filter, select **All opportunities** and click **Done**.
    2. For the Opportunity Status standard filter, select **Open** and click **Apply**.
    3. For the date standard filter, select **Created Date** and **All Time** for the range and click **Apply**.  
        For your Trailhead playground, we're suggesting **All Time** for the range, but for the fastest results in your production environment, always set the smallest date range you can. If your report has to sift through a great many dates, it can take longer to show the information you’ve asked for.
3. The following columns should already be included in your report: Opportunity Name, Type, Lead Source, Amount, Close Date, Next Step, Stage, Probability (%), Fiscal Period, Age, Created Date, Opportunity Owner, Owner Role, Account Name.
4. Click **Save**.
5. Name your report `Open Opportunities This Year`.
6. Enter a description and save the report in the Public Reports folder.
7. Click **Run**. The report should look something like this:

![Tabular report example](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_report_formats/images/f8f291e041c31c03f6f7b90cce04c3c7_rd-report-tabular.png)


## Summary Reports

Summary reports are similar to tabular reports, but also allow you to group rows of data, view subtotals, and create charts. Summary reports give us many more options for organizing the data, and are great for use in dashboards. Yes!

Summary reports are the workhorses of reporting—most people find that most of their reports tend to be of this format.

1. From the Reports tab, click **New Report**, select the ‘Customer Support Reports’ category, choose the ‘Cases’ report type, and click **Start Report**.
2. Click **Filters**, then apply these standard filters:
    1. For Show Me, select **All Cases** and click **Apply**.
    2. For Date Field, select **Opened Date** and **All Time** for the range. Then click **Apply**.
3. From the **Add filter** picklist, apply a field filter for cases where **Closed** equals **True**.
    1. Search for and select **Closed**.
    2. From the dropdown list, select **True** and click **Apply**.
4. Verify that these columns appear in your report: Case Owner, Subject, Date/Time Opened, Age, Open, Closed, and Account Name. If necessary, add them.
5. To make this report a summary report, you need to group rows. To group rows, first click **Outline**.
6. Under GROUP ROWS, from the **Add group** picklist, select **Priority**. ![Creating a summary report](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_report_formats/images/a6633d9b92eeb7a893d0be773a8faf81_admin-intro-report-drag-priority.png)
7. To see just the totals for each priority level, turn off **Detail Rows** at the bottom of the preview page.
8. Save the report as `Closed Cases for All Time`, and accept the auto-generated unique name.
9. Enter a description, choose the Public Reports folder, and click **Save**.
10. Click **Run**. The report should look something like this:![Example of summary report](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_report_formats/images/62ac5d6945593d61c9a81f8a76c8b242_d-29-a-56-dc-9-aa-1-4-ae-3-99-a-8-0-a-64-a-69-c-49-c-3.png)

## Matrix Reports

Matrix reports allow you to group records both by row and by column. These reports are the most time-consuming to set up, but they also provide the most detailed view of your data.

So why would you want to use a matrix report? If you’re looking for an at-a-glance overview of data, especially for something like totals of revenue or quantity of products sold, then the matrix report format is for you.

1. On the Reports tab, click **New Report**, choose the ‘Opportunities’ report type, and click **Start Report**.
2. Click **Filters**, then apply these standard filters:
    1. For the Show Me standard filter, select **All Opportunities** and click **Done**.
    2. For the Opportunity Status standard filter, select **Closed Won** and click **Apply**.
    3. For the Date Field standard filter, select **Close Date**. For Range, select **All Time**. Click **Apply**.  
        For the fastest results, always set the smallest date range you can. If your report has to sift through a great many dates, it can take longer to show the information you’ve asked for.
3. To summarize the report by Sum of Amount, click the ![dropdown arrow](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_report_formats/images/0546f4b3f1c493de89c4ef822054bcd7_dropdown-arrow.jpeg) on the **Amount** column. Then, click **Summarize** and select **Sum**.
4. To change the report format to matrix, first group rows by Close Month and columns by type. To start grouping, click **Outline**.
    1. Under GROUP ROWS, from the **Add group** picklist, select **Close Month**.
    2. Under GROUP COLUMNS, from the **Add group** picklist, select **Type**.
5. You may want to hide the report details when viewing a matrix report. Matrix reports are usually easiest to consume with details hidden. To hide the report details, turn off **Detail Rows**.
6. Save your report as `Opportunities by Sum of Amount` and accept the auto-generated unique name.
7. Click **Run Report**.
8. The report should look something like this. ![Example of matrix report](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_report_formats/images/22e96b7c30666f9fae2eb1591666901d_step-8.jpeg)

## Resources

- [_Salesforce Help:_ Build a Report in Lightning Experience](https://help.salesforce.com/s/articleView?id=sf.reports_build_lex.htm&type=5)

# Visualize Your Data with the Lightning Dashboard Builder

## Create Dashboards
Salesforce dashboards present multiple reports side-by-side using dashboard widgets on a single dashboard page layout. Dashboard widgets come in various chart types, tables, metrics, and gauges, and you can customize how data is grouped, summarized, and displayed for each widget. The dashboard builder is an intuitive interface for building dashboards from source reports you’ve created in Salesforce.

In addition to dashboards, you also have options to add charts to reports and record page layouts. Read on to learn how to visualize data with report charts and dashboard widgets.

## Dashboard Builder

Dashboard builder is your way to visualize your data for easy consumption at-a-glance. Launch the dashboard builder from the Dashboards tab by clicking **New Dashboard**. Enter a name for your dashboard, and click **Create**.

Insert a widget onto your dashboard by clicking **+ Widget**, or add a filter by clicking **+ Filter** **[1]**. When prompted, select the type of content for your new widget, or a field and criteria for a filter. Each widget shows rich text, an image, or data from one report. After you’ve added a widget, click it to resize it, delete it, or change its data-supplying source report ( ![Edit pencil](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/028e48aa29b5e5f4cbc75d896563f521_rd-edit-pencil.png)) **[2]**. Position your widgets by dragging them **[3]**. A responsive grid layout supports widgets of different sizes in diverse arrangements **[4]**.
![[Pasted image 20240527123127.png]]

When selecting the widget type, consider the following.

| Widget Type                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | When to Use It                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| ![horizontal bar chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/efbfa5f0f413c3337f383eb5859b9849_rd-chart-icon-hbar.png) ![vertical bar chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/436b1bd09cbb2a9eec1cb826accbf47e_rd-chart-icon-vbar.png) ![stacked horiztonal bar chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/7034f56e18437665a5ed7320d51ee1f4_rd-chart-icon-stackedhbar.png) ![stacked horizontal bar chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/5af15e64ef0f31af652ef8d0cf6cf58c_rd-chart-icon-stackedvbar.png) ![line chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/4aa10335fed94dc7438c3e346a7fe879_rd-chart-icon-line.png) ![donut chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/d303d13cdad68bb9e425f714e9667805_rd-chart-icon-donut.png) ![funnel chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/4d115559e5dc2c410bd51b7a68776907_rd-chart-icon-funnel.png) ![scatter chart](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/e50430a5f42e11d7fe56761fbf5a0083_rd-chart-icon-scatter.png) | Use a chart when you want to show data graphically. You can choose from various chart types.    |
| ![gauge](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/f1427965dca7cb212b998d003093a651_rd-chart-icon-gauge.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | Use a gauge when you have a single value that you want to show within a range of custom values. |
| ![metric](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/3babd151845ccac886cfbfd01043f28a_rd-chart-icon-metric.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Use a metric when you have one key value to display.                                            |
| ![Lightning table](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/4e963089b044da4a7cf34daed11c5ef2_rd-chart-icon-table-lightning.png) ![legacy table](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/b1eed8ac741aa360448b3ad3404df5d7_rd-chart-icon-table.png)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Use a table to show a set of report data in column form.                                        |

Finally, when selecting a source report for use in a dashboard widget, keep in mind that you can’t choose joined reports or historical trend reports.

## Create a Dashboard
1. Click the Reports tab, click **New Report** and select Leads as the report type. Click **Start Report**.
2. Click **Filters** and edit these standard filters:
    1. For the Show Me standard filter, select **All Leads**. Click **Apply**.
    2. For the Date Field standard filter, select **Create Date**. For Range, select **All Time**. Click **Apply**.
3. Click **Outline** and group rows by Lead Source. From the **Add group** lookup, select **Lead Source**.
4. Ensure that these columns are included in your report: Lead Owner, First Name, Last Name, Title, Company/Account, Rating, Street, Email.
5. Click **Save**, name your report `Leads by Lead Source`, and accept the auto-generated unique name. Click **Save**.
6. Click **Run**. The report should look something like this: ![Leads by source report](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/349f75485ebbe83de76b4cd8cd26b174_rd-report-run.png)

Now that your report is created, let’s visualize it using a dashboard widget.

1. From the Dashboards tab, click **New Dashboard**.
2. Name your dashboard `Leads Dashboard` and, optionally, enter a description.
3. Click **Create**.
4. To insert a widget, click **+ Widget**.
5. Choose **Chart or Table**.
6. From Select Report, choose the Leads report you created earlier, **Leads by Lead Source**, and click **Select**. From Add Component, select the donut chart. ![Adding a dashboard component](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/7ca5e3a2cf71579e54a1f4b5ee731b68_step-6.jpeg)
7. Confirm that your widget is titled `Leads by Lead Source`.
8. Optionally give your widget a subtitle and footer.
9. Click **Add**. Your new widget appears on the dashboard.
10. Optionally, resize your dashboard widget by clicking it, then dragging the corners and sides.
11. Click **Save** and then click **Done**. Your dashboard should look something like this. ![Leads dashboard example](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/bbe2fd2d47d9f9706901b7fb1a895663_rd-dashboard-run.png)

Great job! You just built a simple report and dashboard for visualizing leads by source.

## Use Dynamic Dashboards

With dynamic dashboards, each user sees the data they have access to without needing to create separate dashboards for each user.

This means a single powerful dashboard can be used for multiple users in your company, because the logged-in user viewing the dashboard sees the data they should see, based on their security and sharing settings.

**Set up a Dynamic Dashboard**

1. To store the dynamic dashboard and corresponding source reports, create a dashboard folder and a report folder from the Dashboards, Reports, or Analytics tabs. Share these folders with the intended audience.
2. On the Analytics or Dashboards tab, create a dashboard or edit an existing one.
3. Open the properties menu by clicking **![Edit Dashboard Properties](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/8053bff4588a41f8fdbf2a2a9197b23d_edit-dashboard-properties-icon.png)**.
4. Under View Dashboard As, select **The dashboard viewer**.
5. To let users change the dashboard’s running user, select **Let dashboard viewers choose whom they view the dashboard as**.
6. From the Properties window, click **Save**. Then, from the Dashboard Builder, click **Save** again.

When people open your dashboard, they see data as the person that you specified.

## Report Charts

If you don’t want to create a dashboard, but just want to add a chart to your report, then report charts may be right for you. Report charts allow you to place a single chart right at the top of your report, so that when you view the report, you can see the chart and the report results in one view.

Here’s how you add a report chart:

1. From the Reports tab, open the report you made earlier, Leads by Lead Source.
2. A chart may already appear at the top of your report. If not, click the add chart button ![Add Chart button](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/7fc3fc0e30f85a70ad42322f6d3c2244_add-chart.jpeg). You can show or hide the chart at any time by clicking the icon ![Chart button](https://res.cloudinary.com/hy4kyit2a/f_auto,fl_lossy,q_70/learn/modules/lex_implementation_reports_dashboards/lex_implementation_reports_dashboards_visualizing_data/images/de51efbe457835a778f208350f7b297e_toggle-chart-icon.png).

Presto! Your report now has a chart.

## Resources

- [_Salesforce Help_: Build a Lightning Experience Dashboard](https://help.salesforce.com/articleView?id=dashboards_create_lex.htm&language=en_US)
- [_Salesforce Help_: Edit and Customize Lightning Experience Dashboard Components](https://help.salesforce.com/articleView?id=dashboards_components_edit_lex.htm&language=en_US)
- [_Dynamic Dashboards_: Choose Who People View a Dashboard as in Lightning Experience](https://help.salesforce.com/articleView?id=dashboards_view_as.htm&language=en_US)
- [_Trailhead:_ Embed Dashboards and Report Charts on Lightning Pages](https://trailhead.salesforce.com/content/learn/projects/rd-embed-reports-dashboards)
- [Create Reports and Dashboards for Sales and Marketing Managers](https://trailhead.salesforce.com/content/learn/projects/create-reports-and-dashboards-for-sales-and-marketing-managers)
-  [Discover CRM Analytics](https://trailhead.salesforce.com/content/learn/trails/discover-tableau-crm)
- [CRM Analytics Basics](https://trailhead.salesforce.com/content/learn/modules/wave_analytics_basics) 
