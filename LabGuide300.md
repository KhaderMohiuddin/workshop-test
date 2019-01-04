
![](images/300/Picture300-lab.png)  
Updated: January 4, 2019

## Introduction

This lab walks you through the steps to provision an Oracle Analytics Cloud (OAC) instance and connect it to your Autonomous Data Warehouse (ADW) instance. 


**_To log issues_**, click here to go to the [github oracle](https://github.com/oracle/learning-library/issues/new) repository issue submission form.

## Objectives
-   Learn how to provision a new Oracle Analytics Cloud Instance
-   Learn how to connect the OAC instance to your to the ADW

## Required Artifacts
-   The following lab requires an Oracle Public Cloud account. You may use your own cloud account, a cloud account that you obtained through a trial, or a training account whose details were given to you by an Oracle instructor.



# Getting Started with Oracle Analytics Cloud (OAC)

# Part 1. Create an OAC Instance
In this section you will create an OAC instance.


#### **STEP 1: Sign in to Oracle Cloud**

-   Go to [cloud.oracle.com](https://cloud.oracle.com), click **Sign In** to sign in with your Oracle Cloud account.

![](./images/300/Picture100-2.png)

-   Enter your **Cloud Account Name** and click **My Services**.

![](./images/300/Picture100-3.jpg)

-   Enter your Oracle Cloud **username** and **password**, and click **Sign In**.

![](./images/300/Picture100-4.png)



#### **STEP 2: Create an OAC Instance**

-   Go to your **Dashboard** page and click on **Create Instance**.

![](./images/300/Picture300-21.png)

-   Under **All Services**, find **Autonomous Analytics** and click on **Create**.

![](./images/300/Picture300-22.png)

-   On the **Autonomous Analytics** page, click on **Create Instance**.

![](./images/300/Picture300-23.png)

-   Provide all the required information (fields specified by *) and then click on **Next**.

![](./images/300/Picture300-24.png)

-   After validating your configuration, click on **Create**.

![](./images/300/Picture300-25.png)

-   It will take a few minutes until your instance is fully provisioned and ready to use. Note the Status and the sign which indicate that the service is being creating. Wait until this process is fully completed.

![](./images/300/Picture300-26.png)

-   After a few minutes refresh your page and you will see the status and the sign are disappeared. Now your OAC instance is ready. In order to access your instance, click on the  icon on the right side of your instance.

![](./images/300/Picture300-27.png)

-   Now click on Autonomous Analytics URL which redirects you to a new page.

![](./images/300/Picture300-28.png)


-   Welcome to the Oracle Analytic Cloud! Enjoy exploring it!

![](./images/300/Picture300-29.png)




# Part 2. Connect OAC to ADW

#### **STEP 3: Connect OAC to ADW**

-   In the Oracle Analytics Cloud Homepage, click on the **Create** button on the top-right and then click on **Connection** in the popped menu.

![](./images/300/Picture300-31.png)

-   Select the **Oracle Autonomous Data Warehouse Cloud** from the existing connection types.

![](./images/300/Picture300-32.png)

-   Complete all the required fields in the wizard as described in the table below and Save the connection. Note that you need the ADW instance **Wallet** in order to be able to complete these fields (similar to connecting the SQL Developer to the ADW instance). Please refer to the instruction in **Lab100** for accessing the **Wallet**.

![](./images/300/Picture300-33.png)

-   You should fill the following connection fileds:

-   **Connection Name:** Type a name for this connection (e.g. ADWDBBIKESHARE)

-   **Host:** Copy the Host value from the **tnsnames.ora** file in the (unzipped) **Wallet** (e.g. adb.us-ashburn-1.oraclecloud.com) 

-   **Port:** Copy the Port value from the **tnsnames.ora** file in the (unzipped) **Wallet** (e.g.  1522)

-   **Client Credentials:** Click on **‘Select’** and select the file **cwallet.sso** from the (unzipped) **Wallet**

-   **Username:** Admin (the username you created during the ADW provisioning)

-   **Password:** The password you specified during provision of your ADW instance

-   **Service Name:** Copy the desired service name from three available options (low, medium,high). The Service name is accessible in the **tnsnames.ora** file in the (unzipped) **Wallet** under **<DatabaseName>_<ServiceLevel>** (e.g.  esjdxrwocdkdvja_testadw_medium.adwc.oraclecloud.com)


-   You can see your connection listed under the Connections tab in the Data page.

![](./images/300/Picture300-34.png)



# Part 3. Import Datasets from ADW to OAC

#### **STEP 4: Import the Training Datasets for the ML Model to OAC**

-   In the Oracle Analytics Cloud Homepage, click on the **Create** button on the top-right and then click on **Data Set** in the popped menu.

![](./images/300/Picture300-41.png)

-   Select the connection that you have created in previous step.

![](./images/300/Picture300-42.png)

-   Select the **ADMIN** user from the list of users to import the datasets prepared in the SQL Developer.

![](./images/300/Picture300-43.png)


Now we should import the **STATION_INFO** and **STATION_ST_WTH_TRAINING** tables prepared in the SQL Developer to our OAC instance. We need the **STATION_INFO** table for creating the graphs and the **STATION_ST_WTH_TRAINING** table for training the ML model in OAC. In next steps, we show you how to import the **STATION_ST_WTH_TRAINING** table. You can repeat the same steps to import the **STATION_INFO** table.


-   Select the desired table (**STATION_ST_WTH_TRAINING**) from the list.

![](./images/300/Picture300-44.png)

-   Add all columns to your selection.

![](./images/300/Picture300-45.png)

-   Give a name to the table (**STATION_ST_WTH_TRAINING**) and add it to your data set.

![](./images/300/Picture300-46.png)

-   When the data set is loaded, change the **STATIONID** column from **Measure** type to **Attribute** type. In order to do so, click on the # sign next to the column name and select **Attribute** from the drop-down menu.

![](./images/300/Picture300-47.png)


-    Then click on **Apply Script**.

![](./images/300/Picture300-48.png)


-   After importing all tables, you can see them under the **Data Set** tab in the **Data** section.

![](./images/300/Picture300-45.png)

<table>
<tr><td class="td-logo">[![](images/obe_tag.png)](#)</td>
<td class="td-banner">
## Great Work - All Done!
**You are ready to move on to the next lab. You may now close this tab.**
</td>
</tr>
<table>
