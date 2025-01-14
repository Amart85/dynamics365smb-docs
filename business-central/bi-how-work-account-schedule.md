---
title: Build financial reports using account schedules
description: Describes how to use account schedules to create various views and report for analyzing financial performance data.
author: edupont04


ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bi, power BI, analysis, KPI
ms.search.form: 103, 104, 197, 196, 195, 198, 490, 764, 765, 766
ms.date: 04/01/2021
ms.author: edupont

---
# Prepare Financial Reporting with Account Schedules and Account Categories

Use account schedules to get insight into the financial data stored in your chart of accounts. Account schedules analyze figures in G/L accounts, and compare general ledger entries with general ledger budget entries. The results display in charts and reports on your Role Center, such as the Cash Flow chart and the Income Statement and Balance Sheet reports.

You access these two reports, for example, with the **Financials Statements** action on the Business Manager and Accountant Role Centers.  

[!INCLUDE[prod_short](includes/prod_short.md)] provides sample account schedules that you can use right away. You can also set up your own rows and columns to specify the figures to compare. For example, you can create account schedules to calculate profit margins on dimensions such as departments or customer groups. The number of customized financial statements you can create is unlimited.  

Setting up account schedules requires an understanding of the financial data in the chart of accounts. For example, you can view general ledger entries as percentages of budget entries, but that requires that you've created budgets. For more information, see [Create G/L Budgets](finance-how-create-budgets.md).

## Account Schedules

Account schedules arrange accounts from your chart of accounts in ways that make data easy to present. You can set up various layouts to define the information that you want to extract from the chart of accounts. Account schedules provide a place for calculations that can't be made directly in the chart of accounts. For example, you can create subtotals for groups of accounts and then include that total in other totals. Another example is to calculate profit margins on dimensions such as departments or customer groups. Additionally, you can filter general ledger entries and general ledger budget entries, for example, by net change or debit amount.

You can also compare two or more account schedules and column layouts by using formulas, which lets you take the following actions:

* Create customized financial reports.
* Create as many account schedules as needed, each with a unique name.
* Set up various report layouts and print the reports with the current figures.

## G/L Account Categories

You can use G/L account categories to change the layout of your financial statements. After you set up your account categories on the **G/L Account Categories** page, and you choose the **Generate Account Schedules** action, the underlying account schedules for the core financial reports are updated. The next time you run one of these reports, such as the **Balance Statement** report, new totals and subentries are added, based on your changes.

> [!NOTE]
> The top-level account categories, such as the **Liabilities** node are fixed and you cannot add your own. However, you can delete and add account categories at lower levels and change their structure to define how the related account schedule appears in reports.
>
> It is recommended to create and structure your own lower-level G/L account categories from scratch, in a hierarchy if needed, rather than try to rearrange the existing ones. For example, you can restructure the **Liabilities** node to contain a new **Equity** node followed by the **Current Liabilities** and **Long Term Liabilities** nodes.

## To create a new account schedule

You use account schedules to analyze figures in general ledger accounts or to compare general ledger entries with general ledger budget entries. For example, you can view the general ledger entries as percentages of the budget entries.

The account schedules in the standard version of [!INCLUDE[prod_short](includes/prod_short.md)] are the basis of the standard financial reports, which may not suit the needs of your business. To quickly create your own financial reports, you can start by copying an existing account schedule, as described in step 3.

> [!TIP]
> After you create an account schedule, you can use the **Acc. Schedule Overview** page to preview and validate the financial report that the account schedule defines. To open the page, choose the **Overview** action.  

1. Choose the ![Lightbulb that opens the Tell Me feature 1.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.  
2. On the **Account Schedules** page, choose the **New** action to create a new account schedule name.
3. Alternatively, if you want to reuse settings from an existing account schedule, choose the **Copy Account Schedule** action.
4. Fill in the fields as necessary. In the **Default Column Layout** field, select an existing layout. You can edit it later if you want.

    Column layouts define columns for the parameters by which the financial data on the rows is shown. For example, a column layout might contain four columns that let you compare net change and balance for the same period this year and last year. For more information, see [To edit a column layout](bi-how-work-account-schedule.md#to-edit-a-column-layout).

5. Choose the **Edit Account Schedule** action.
6. Depending on what you want to analyze, choose the **Insert G/L Accounts**, **Insert CF Accounts**, and **Insert Cost Types** actions to create a row for each financial element. For example, you might have one row for current assets and another row for fixed assets. For inspiration, see the account schedules in the CRONUS demonstration company.

    > [!NOTE]
    > The **Row No.** field will show the first 10 characters of an identifier, for example, an account number. If you add elements with identifiers that start with the same 10 characters you'll have duplicates in the **Row No.** field. If needed, you can manually edit the identfiers after you insert the elements. The full identifiers are displayed in the **Totaling** field.

7. Choose the **Overview** action to see the resulting financial report.
8. On the **Acc. Schedule Overview** page, in the **Column Layout Name** field, select another column layout to see the financial data by other parameters.
9. Choose the **OK** button.

You've now defined the basis of the account schedule, the rows of financial data to be displayed, and an existing layout of columns to show the data on the rows per different parameters. If the default column layout that you selected in step 4 doesn't suit your purpose, follow the next procedure.

### To edit a column layout

You use column layouts to define what columns should be included in the resulting report. For example, you can design a layout to compare net change and balance for the same period this year and last year. You can have up to 15 columns, which is useful, for example, for viewing budgets for 12 months with a column that shows the total.

> [!NOTE]
> A printed/previewed/saved version of an account schedule can display a maximum of five columns. If the account schedule is only meant for analysis on the **Acc. Schedule Overview** page, you can create as many columns as you want.

1. On the **Account Schedules** page, select the relevant account schedule, and then choose the **Edit Column Layout Setup** action.
2. On the **Column Layouts** page, create a row for each column by which financial data is shown in the financial report. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Choose the **OK** button.
4. Open the **Acc. Schedule Overview** page from time to time to verify that the new column layout works as intended.

> [!NOTE]
> The columns that you define on each row represent columns 3 and up on the **Acc. Schedule Overview** page. The first two columns, **Row No.** and **Description**, are fixed.  

### To create a column that calculates percentages

Sometimes you may want to include a column in an account schedule to calculate percentages of a total. For example, if you have rows that break down sales by dimension, you may want a column to indicate the percentage of total sales in each row.

1. Choose the ![Lightbulb that opens the Tell Me feature 2.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.
2. On the **Account Schedule Names** page, select an account schedule.  
3. Choose the **Edit Account Schedule** action to set up an account schedule row to calculate the total on which the percentages will be based.  
4. Insert a line immediately above the first row for which you want to display a percentage.  
5. Fill in the fields on the line as follows: In the **Totaling Type** field, enter **Set Base for Percent**. In the **Totaling** field, enter a formula for the total that the percentage will be based on. For example, if row 11 contains the total sales, enter **11**.  
6. Choose the **Edit Column Layout Setup** action to set up a column.  
7. Fill in the fields on the line as follows: In the **Column Type** field, select **Formula**. In the **Formula** field, enter a formula for the amount that you want to calculate a percentage for, followed by %. For example, if column number N contains the net change, enter **N%**.  
8. Repeat steps 4 through 7 for each group of rows that you want to break down by percentage.

## To set up account schedules with overviews

You can use an account schedule to create a statement comparing general ledger figures and general ledger budget figures.

1. Choose the ![Lightbulb that opens the Tell Me feature 3.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.
2. On the **Account Schedule Names** page, select an account schedule.  
3. Choose the **Edit Account Schedule** action  
4. On the **Account Schedule** page, in the **Name** field, select the default account schedule name.
5. Choose the **Insert G/L Accounts** action.  
6. Select the accounts that you want to include in your statement, and then choose the **OK** button.

    The accounts are now inserted into your account schedule. If you want, you can also change the column layout.  
7. Choose the **Overview** action.  
8. On the **Acc. Schedule Overview** page, on the **Dimension Filters** FastTab, set the budget filter to the filter name you want to use.  
9. Choose the **OK** button.  

Now you can copy and paste your budget statement into a spreadsheet.  

## Comparing Accounting Periods using Period Formulas

Your account schedule can compare the results of different accounting periods, such as this month versus same month last year. To do that, open the **Column Layout** page, and personalize it by adding the **Comparison Period Formula** field as a column. For more information, see [Personalize Your Workspace](ui-personalization-user.md). You can then set that field to a period formula.  

An accounting period doesn't have to match the calendar. However, each fiscal year must have the same number of accounting periods, even though each period can be different in length.  

[!INCLUDE[prod_short](includes/prod_short.md)] uses the period formula to calculate the amount from the comparison period in relation to the period represented by the date filter on the report. The comparison period is based on the period of the start date of the date filter. The abbreviations for period specifications are:

| Abbreviation | Description                                                                           |
| ------------ | ------------------------------------------------------------------------------------- |
| P            | Period                                                                                |
| LP           | Last period of a fiscal year, half-year, or quarter.                                   |
| CP           | Current period of a fiscal year, half-year, or quarter. Use CP in formulas to set the period that starts or ends the formula. For example, FY\[1..CP\] denotes the time from the beginning of the current fiscal year to the current period.|
| FY           | Fiscal year. For example, FY\[1..3\] denotes first quarter of the current fiscal year |

Examples of formulas:

| Formula         | Description                                                                                     |
| --------------- | ----------------------------------------------------------------------------------------------- |
| \<Blank\>       | Current period                                                                                  |
| \-1P            | Previous period                                                                                 |
| \-1FY\[1..LP\]  | Entire previous fiscal year                                                                     |
| \-1FY           | Current period in previous fiscal year                                                          |
| \-1FY\[1..3\]   | First quarter of previous fiscal year                                                           |
| \-1FY\[1..CP\]  | From the beginning of previous fiscal year to current period in previous fiscal year, including both periods |
| \-1FY\[CP..LP\] | From current period in previous fiscal year to last period of previous fiscal year, including both periods   |

If you want to calculate by regular time periods, you must enter a formula in the **Comparison Date Formula** field instead. For example, if the field is set to -1Y, [!INCLUDE [prod_short](includes/prod_short.md)] compares to the same period 1 year earlier.

> [!NOTE]
> It is not always transparent which periods you are comparing because you can set a date filter on a report that spans different dates than the accounting periods that are reflected in the data in the chart of accounts. For example, you create an account schedule where you want to compare this period with the same period last year, so you set the **Comparison Date Formula** field to *-1FY*. Then, you run the report on February 28th and set the date filter to January and February. As a result, the account schedule compares January and February this year to January last year, which is the only completed accounting period of the two for last year.  

For more information about date formulas, see [Work with Calendar Dates and Times](ui-enter-date-ranges.md).  

## Import or Export Account Schedules
You can import and export account schedules as RapidStart configuration packages. For example, configuration packages are useful for sharing them with other companies. The package is created in a .rapidstart file, which delivers the package contents in a compressed format.

### To import and export account schedules
1. Choose the ![Lightbulb that opens the Tell Me feature 4.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Account Schedules**, and then choose the related link.
2. Choose the account schedule, and then choose the **Import Account Schedule** or **Export Account Schedule** actions, depending on what you want to do. 

> [!NOTE]
> When you import account schedules, existing records that have the same names as those you are importing will be deleted.

## See related training at [Microsoft Learn](/learn/modules/configure-financial-reports-dynamics-365-business-central/index)

## See Also

[Business Intelligence](bi.md)  
[Finance](finance.md)  
[Setting Up Finance](finance-setup-finance.md)  
[The General Ledger and the Chart of Accounts](finance-general-ledger.md)  
[Work with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]