# Module 3 - Lab 3 - Exercise 4 - Implement Mailbox Permission Alert


In this exercise you will configure and test an alert that will notify Lynne Robbins when FullAccess permissions are granted to any mailbox within Adatum.

### Task 1 – Create a Mailbox Permission Alert

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Admin** account and into Microsoft 365 as Holly Dickson (**holly@M365xZZZZZZ.onmicrosoft.com)** with a password of **Pa55w.rd**. 

2. In the **Microsoft 365 Security &amp; Compliance center**, in the left-hand navigation pane, select **Alerts,** and then under it, select **Alert policies**.

3. In the **Alert policies** window, select **+New alert policy**.

4. In the **New alert policy** window, enter the following information:

	- Name: **Mailbox permission change**

	- Description: **This alert notifies Lynne Robbins when FullAccess permissions are granted to any mailbox in Adatum Corp.**

	- Severity: **Medium**

	- Category: **Permissions**

5. Select **Next.**

6. On the **Choose an activity, conditions and when to trigger the alert** window, enter the following information:

	- Activity is: select the drop-down arrow in the field, enter **mail** in the search box, and select **Granted mailbox permission**

	- How do you want the alert to be triggered? **Every time an activity matches the rule**

7. Select **Next.**

8. On the **Decide if you want to notify people when this alert is triggered** window, enter the following information:

	- Email recipients: Selecf the "X" to the right of **Holly Dickson's** account to remove her, enter **Lynne**, and then select **Lynne Robbins** from the user list

	- Daily notification limit: **No limit**

9. Select **Next.**

10. Review your settings. When everything is correct, verify the **Yes, turn it on right away** option is selected (select it if necessary) and then select **Finish**.

11. Verify your new alert policy appears in the list on the **Alert policies** page and its **Status** in **On**.

11. Leave the Client 1 VM and the Microsoft 365 admin center and Security and Compliance Center tabs open for the next task.

You have now created an activity alert in the Security & Compliance Center that is triggered when FullAccess permissions are granted to any mailboxes.


### Task 2 – Validate the Mailbox Permission Alert

In the prior task, you configured an alert that will notify Lynne Robbins when FullAccess permissions are granted to any mailbox within Adatum. To test this alert, Holly Dickson will change the FullAccess permission on Alex Wilber’s mailbox by granting Joni Sherman FullAccess to his mailbox. This activity should trigger the alert policy that you just created, which should send an alert notification email to Lynne Robbins’ mailbox. You will then log into the Client 2 VM as Lynne Robbins and see if she received this email. 

1. You should still be logged into the Client 1 VM (LON-CL1) as the **Admin** account, and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In the **Microsoft 365 admin center**, in the left-hand navigation pange, select **Show all** (if necessary). In the list of admin centers, select **Exchange**.

3. This opens a new tab in your browser for the **Exchange admin center.** Select **recipients** from the left-hand navigation pane. In the **recipients** window, the **mailboxes** tab is displayed by default.

4. Select **Alex Wilber** from the list and then select the **pencil (Edit)** icon from the menu bar to edit his mailbox settings.

5. In the **Edit User Mailbox** window, select **mailbox delegation** from the bottom of the menu and wait until all settings are loaded.

6. Scroll down to **Full Access** and select the **(+) plus** icon.

7. In the **Select Full Access** window, select **Joni Sherman**, select **add -&gt;**, and then select **OK**.

8. In the **Edit User Mailbox** window, select **Save**, and then select **OK** once the information is saved.

9. Since **Holly Dickson** has changed the mailbox permissions for Alex Wilbur by giving Joni Sherman FullAccess permissions to his mailbox, an alert email should automatically be sent to Lynne Robbins’ Inbox that notifies her of this event.

	‎Switch to the Client 2 VM (LON-CL2) and log in as the **Admin** account with a password of **Pa55w.rd**. 

10. In Lab 1, you had signed into the Client 2 VM as the **Admin** account, and you logged into Outlook as the MOD Administrator. You should sign out of the MOD Administrator account by selecting the **MA** user icon in the upper-right corner of the screen, and then in the **My Account** pane, select **Sign out**. 

11.  Once you’re signed out, enter the following URL in the address bar: **https://outlook.office365.com**

12. In the **Sign in** window, enter **LynneR@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant ID provided by your lab hosting provider) and then select **Next**.

13. In the **Enter Password** window, enter **Pa55w.rd** as the password and select **Sign in**, and then select **Yes** to stay signed in. 

14. If a **Welcome** window appears, select the **X** to close it.

15. In **Outlook on the web**, in Lynne Robbins’ **Inbox**, an email should be received from the Alerts notification system (**Office365Alerts@microsoft.com**) to let her know that Holly Dickson has made a Mailbox permission change. <br/>

	**Note:** In can take up to 15 minutes or so for the email to be received in Lynne's Inbox.

16. Open the email and review the contents. Scroll to the bottom of the email and select the **View alert details** button. This opens the **Security and Compliance Center**, displays the **View alters** window, and opens the **Mailbox permission change** alert. <br/>

	Scroll down through the **Mailbox permission change** alert and review all the information. When you are done, select **Close** to close the **Mailbox permission change** alert, then close the **View alerts** tab in your browser.

17. Switch back to the LON-CL1.

18. In the **Microsoft 365 Security &amp; Compliance center**, in the left-hand navigation pane, select **Alerts,** and then under it, select **View Alerts**. The notification that was just created based on the **Mailbox permission change** alert should appear in the list.

19. In your browser, close the Exhange admin center tab (**mailboxes - Microsoft Exchange**), but leave the other browser tabs open.

20. Leave your Client 1 and Client 2 VMs open for the remaining tasks in this lab.

You have just successfully tested a mailbox permission alert that sent an alarm message on granting FullAccess to a user mailbox.

# Proceed to Exercise 5
