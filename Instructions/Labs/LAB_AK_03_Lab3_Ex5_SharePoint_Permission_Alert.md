# Module 3 - Lab 3 - Exercise 5 - Implement SharePoint Permission Alert


In this exercise you will configure and test an alert that notifies Lynne Robbins when a user is added to the site collection administrators for a SharePoint site collection.

### Task 1 – Create a SharePoint Permissions Alert

1. You should still be logged into the Client 1 VM (LON-CL1) as the **Admin,** and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In the **Microsoft 365 Security &amp; Compliance center**, the **Alert policies** window should still be open from the prior task; if not, select **Alerts** and then **Alert Policies** from the left-hand navigation bar. In the **Alert policies** window, select the **+New alert policy** button.

3. In the **New alert policy** window, enter the following information:

	- Name: **Site collection admin permissions**

	- Description: **This alert notifies Lynne Robbins when a user is added to the site collection administrators on a SharePoint site collection..**

	- Severity: **Medium**

	- Category: **Permissions**

4. Select **Next.**

5. On the **Choose an activity, conditions and when to trigger the alert** window, enter the following information:

	- Activity is: select the drop-down arrow in the field, enter **site collection** in the search box, and select **Added site collection admin**

	- How do you want the alert to be triggered? **Every time an activity matches the rule**

12. Select **Next.**

13. On the **Decide if you want to notify people when this alert is triggered** window, enter the following information:

	- Email recipients: Remove **Holly Dickson** and add **Lynne Robbins**

	- Daily notification limit: **No limit**

14. Select **Next.**

15. Review your settings. When everything is correct, verify the **Yes, turn it on right away** option is selected and then select **Finish**.

16. Leave the Client 1 VM and the Microsoft 365 admin center and Security and Compliance Center tabs open for the next task.

You have now configured an additional alert policy that monitors when a site collection administrator is added to SharePoint Online site collections.

### Task 2 – Validate the  SharePoint Permissions Alert

In the prior task, you configured an alert that will notify Lynne Robbins when a site collection admin is added to a site collection. To test this alert, Holly Dickson will add Alex Wilber as a site collection admin to the global Sharepoint Communication site. This activity should trigger the alert policy that you just created, which should send an alert notification email to Lynne Robbins’ mailbox. You will then switch to the Client 2 VM to see if Lynne received this email. 

1. You should still be logged into the Client 1 VM (LON-CL1) as the **Admin**, and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, open a new tab and enter the following URL in the address bar: **https://M365xZZZZZZ.sharepoint.com/_layouts/15/settings.aspx** (replace ZZZZZZ with the tenant ID provided by your lab hosting provider). This opens the **Site Settings** for the global SharePoint Communication site.

3. On the **Site Settings** window, under **Users and Permissions**, select **Site permissions**. 

4. In the ribbon at the top of the page, the **Permissions** tab is displayed by default. Under the **Manage** group, select **Site Collection Administrators**.

5. In the **Site Collection Administrators** dialog box, the Company Administrator is displayed by default in the data entry field. To the right of Company Administrator, enter **Alex**, select **Alex Wilber** from the list of users that appears, and then select **OK**. 

6. Since a new site collection admin has been added, an alert should automatically be sent to Lynne Robbins’ Inbox notifying her of this event. Perform the remaining steps to verify that Lynne received this email.

	‎Switch to the Client 2 VM (LON-CL2) and log in as the **Admin** account with a password of **Pa55w.rd**. 

7. From the prior task, you should still be logged into **Outlook on the web** as **Lynne Robbins**. Select the **Refresh** icon to the left of the address bar to reload Lynne's Inbox. <br/>

	**Note:** In can take up to 15 minutes or so for the email to be received in Lynne's Inbox.

8. Open the email and review the contents. Scroll to the bottom of the email and select the **View alert details** button. This opens the **Security and Compliance Center**, displays the **View alters** window, and opens the **Site collection admin permissions** alert. <br/>

	Scroll down through the alert and review all the information. When you are done, select **Close** to close the alert, then close the **View alerts** tab in your browser.

9. Leave your Client 1 and Client 2 VMs open for the remaining tasks in this lab.

You have now successfully tested the SharePoint alert to monitor site collection admin permissions on SharePoint sites. 


# Proceed to Exercise 6
