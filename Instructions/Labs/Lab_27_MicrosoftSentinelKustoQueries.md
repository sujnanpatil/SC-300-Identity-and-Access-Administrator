# Lab 27 - Microsoft Sentinel Kusto Queries for Microsoft Entra ID data sources

## Lab scenario

Microsoft Sentinel is Microsoft's cloud-native SIEM and SOAR solution.  Through connecting data sources from Microsoft and third-party security solutions, you have the ability to execute security operations tasks.  In this lab exercise, you will create a Microsoft Sentinel workspace with data connectors to Azure AD for executing hunting queries using Kusto Query Language (KQL). 

## Lab Objectives

In this lab, you will be performing the following tasks:

- Task 1 - Create a Microsoft Sentinel workspace
- Task 2 - Add Azure AD as a Data source
- Task 3 - Run Kusto query on User activity

## Architecture Diagram

![Screen image displaying the New Group page with Group type, Group name, Owners, and Members highlighted](./media/arch27.png)

#### Estimated time: 60 minutes

### Exercise 1 - Configure Microsoft Sentinel for Kusto Queries
Configuring Microsoft Sentinel for Kusto Queries enables advanced log and security data analysis within the Azure Sentinel platform, enhancing threat detection and response capabilities.

#### Task 1 - Create a Microsoft Sentinel workspace

1. In **Search resources, services, and docs** search and select for **Microsoft Sentinel**. 

1. On the **Microsoft Sentinel** page, select **+ Create**.

1. In the **Add Microsoft Sentinel to a workspace** tile, select **+ Create a new workspace**.

1. In **Resource group**, select **sc-300-rg**.

1. Name the workspace as **SentinelLogAnalytics**.

1. Select Region as **<inject key="Region" enableCopy="false"/>**.

1. Select **Review + Create** and then **Create**.

1. After the Log Analytics workspace deployment completes, choose the **Refresh** button. Then select your workspace and select **Add**.  This will add the workspace to Microsoft Sentinel and open Microsoft Sentinel.

1. If prompted, select **OK** to activate the Microsoft Sentinel free trial.

    > **Congratulations** on completing the task! Now, it's time to validate it. Here are the steps:
    > - Hit the Validate button for the corresponding task. If you receive a success message, you can proceed to the next task.
    > - If not, carefully read the error message and retry the step, following the instructions in the lab guide. 
    > - If you need any assistance, please contact us at labs-support@spektrasystems.com. We are available 24/7 to help you out.

   <validation step="4e426e86-3c79-41e6-b8e8-1c53996176e3" />

#### Task 2 - Add Microsoft Entra ID as a Data source

1. In **Microsoft Sentinel**, from the left-hand navigate menu under the **Configuration** section, select **Data connectors**.

1. Scroll down under the Getting started section Click on **Get these data connectors**. 

1. In the list of Data connectors, locate **Microsoft Entra ID** and select.

1. To the right, a preview tile will open.  Select **Install**.

1. Once installation is done, navigate back to the menu to **Configuration** and select **Data connectors (1)** .

1. Select **Microsoft Entra ID** connector name and to the right, a preview tile will open click on **Open connector page**.

   ![Screen image displaying the Azure AD roles page with the Settings menu highlighted](./media/lab27-1.png)

1. In the connector page, the instructions and next steps will be provided for the data connector. Verify that a check-mark is next to each of the **Prerequisites** to continue with the **Configuration**.

1. Under **Configuration**, check the boxes for **Sign-in logs** and **Audit logs**. Additional log sources are available but are currently in **Preview** and out of scope for this course and click on **Apply Changes**. 
   ![Screen image displaying the Azure AD roles page with the Settings menu highlighted](./media/lab27-3.png)

1. Notification will be provided that the changes were applied successfully. Navigate to the **Microsoft Sentinel** workspace by selecting the **X** on the top right of the connector page.

1. Select **Refresh** on the **Microsoft Sentinel | Data connectors** tile and the number 1 will show in the **Connected** count.

   ![Screen image displaying the Azure AD roles page with the Settings menu highlighted](./media/lab27-2.png)

   **Note** - The Microsoft Entra ID data connector may take a few minutes to show in the active count. 

#### Task 3 - Run Kusto query on User activity

1. In **Microsoft Sentinel** page, from the left-hand navigation page select **Logs** under the **General** menu section.

1. Close the **Welcome to Log Analytics** window.

1. A window will open with sample queries, select **Audit (1)**, search and scroll to find **User IDs**.

1. Select **Run (2)**.

   ![](./media/audit.png)

1. This will provide a list of User IDs on Microsoft Entra ID. Since we have just created the workspace, you may not see results. Note the format of the query.


## Review

In this lab you have completed the following tasks:

- Create a Microsoft Sentinel workspace
- Add Azure AD as a Data source
- Run Kusto query on User activity

## You have successfully completed the lab.
