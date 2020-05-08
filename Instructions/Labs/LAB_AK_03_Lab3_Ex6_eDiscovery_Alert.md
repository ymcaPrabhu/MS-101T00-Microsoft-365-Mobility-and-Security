# Module 3 - Lab 3 - Exercise 6 - Test the Default eDiscovery Alert

In this exercise you will test a default Microsoft 365 alert policy that notifies all tenant admins, such as Holly Dickson, whenever an eDiscovery case has been created or exported.

**Note:** Creating an eDiscovery alert of this nature is important because an eDiscovery search, when left unregulated, can pull sensitive content that can be exported to an unauthorized source.

### Task 1 – Review the default eDiscovery Alert

In this task, you will verify whether a default Microsoft 365 alert is triggered when somebody in your tenant creates an eDiscovery case or exports data from an existing case. Since Holly Dickson is assigned the Global Admin role, she is automatically a member of the Tenant Admins and will be one of the recipients of this alert. 

1. You should still be logged into the Client 1 VM (LON-CL1) as the **Admin,** and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, select the **Microsoft 365 Security &amp; Compliance Center** tab.

3. In the **Microsoft 365 Security &amp; Compliance center**, the **Alert policies** window should still be open from the prior task; if not, select **Alerts** and then **Alert Policies** from the left-hand navigation bar. <br/>

4. You want to search through the default system policies for a policy named **eDiscovery search started or exported**. In the **Search** field at the top of the screen, enter **eDiscovery**. In the list of policies, you should see **eDiscovery search started or exported**. Select the check box next to this policy.

5. An **eDiscovery search started or exported** pane should appear. Scroll down through **eDiscovery search started or exported** pane and verify the settings are configured as follows:

	- Status: **On**
	
	- Conditions: **Activity is eDiscoverySearchStartedOrExported**

	- Aggregation: **Single event**

	- Scope: **All users**

	- Email recipients: **TenantAdmins**

6. If all settings are correct, select the **Close** button to close the **eDiscovery search started or exported** pane.

7. In the **Alert policies** list, select the **ellipsis** icon that appears on the far right side of **eDiscovery search started or exported** row, and then in the menu that appears, select **Edit**.

8. An **Edit recipients** pane appears. This window enables you to edit the email recipients who are notified when this policy is triggered. You will not change the value here, instead, the purpose of this step is to show you how to change the recipient list in your real-world implementations for any of the default system policies. Select **Close**.

You have now reviewed the default Microsoft 365 eDiscovery alert that notifies tenant admins when an eDiscovery case is created or exported.

### Task 2 – Validate the default eDiscovery Alert

To test this default alert, Holly Dickson will create an eDiscovery case. This activity should trigger the alert policy, which should send an alert notification email to all tenant admins. Since Holly is a Tenant Admin, she should receive this alert. 

1. You should still be logged into the Client 1 VM (LON-CL1) as the **Admin,** and you should still be logged into Microsoft 365 as **Holly Dickson**. 

2. In your **Microsoft Edge** browser, select the **Microsoft 365 Security &amp; Compliance Center** tab. 

3. In the **Microsoft 365 Security &amp; Compliance Center**, in the left-hand navigation pane, select **eDiscovery**, and then under it, select **eDiscovery**.

4. On the **eDiscovery** window, select the **+Create a case** button.

5. In the **New case** window, enter the following information:

	- Case Name: **Testing eDiscovery Alerts**

	- Case description: **This case will be used for testing the default Microsoft 365 eDiscovery alert.**

6. Select **Save**. 

7. By creating this alert, an email notiification should automatically be sent to the Inbox of all users with tenant admin permissions whenever an eDiscovery case is opened or exported. To test this alert, open a new tab in your browser and go to **Outlook on the web** by entering the following URL in the address pane: **https://outlook.office365.com**

8. When Outlook opens, if the language and time zone window appears, select your Language and Time zone and select **Save**. 

9. Monitor Holly's Inbox for the email that was automatically sent by the Alerts notification system to inform her that an eDiscovery case was created. <br/>

	**Note:** Based on lab testing, the time for an email to be generated and received in Holly's Inbox can range from a couple of minutes to an hour. <br/>
	
	Once the email is received, open it and review the contents, then close the message.

10. In your **Edge** browser, switch back to the **Microsoft 365 Security &amp; Compliance Center** tab and under the **Search** group in the left-hand navigation pane, select **Audit Log Search**. 

11. At the bottom of the page, select the **Search** button to display all recent activity. This will display the activity that created this alert. <br/>

	**Note:** It may take a minute or so for the **Search** button at the bottom of the page to become enabled.

12. In your browser, leave the Outlook tab (**Mail-Holly Dickson - Outlook**) open as you will use it shortly in another lab exercise. Leave all your other browser tabs open as well.

13. Leave your Client VMs open for the remaining labs in this course.  

You have now successfully tested the default Microsoft 365 eDiscovery alert that monitors the creation of an eDiscovery case or data export from an existing case.


# End of Lab 3
