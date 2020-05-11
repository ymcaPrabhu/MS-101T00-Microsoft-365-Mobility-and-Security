# Module 6 - Lab 6 - Exercise 2 - Test MRM and DLP Policies


You are now at the point in your pilot project where you want to test policies. You have decided to test an MRM policy that affects how email messages are archived, and then you want to test a DLP policy related to emails that contain sensitive information. 

### Task 1 – Test an MRM Policy to Archive Email Messages

In this exercise, you will send an email from Holly Dickson to one of your test users, Lynne Robbins. You will then log into Microsoft 365 as Lynne on the Client 2 VM, locate the email in her Inbox, and then assign the email a custom retention tag that you created. This personal retention tag will override the parent folder tag for this specific message, which will be moved to Lynne’s In-Place archive mailbox after 3 years rather than 2 years.

1. You should still be logged into your Client 1 VM as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In **Microsoft Edge**, If you have an **Outlook on the web** tab open for Holly, then select it now; otherwise, open a new tab and navigate to **https://outlook.office365.com** and then if necessary, sign in as **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) using a password of **Pa55w.rd.** <br/>

	If **Outlook on the web** was already open, then verify that you are logged in as **Holly** by checking the user icon in the upper right corner (the **HD** circle). If Outlook was open for any other user, then close the tab and repeat the instructions in this step to open Outlook on the Web for Holly.

3. In **Outlook on the web**, in the upper left corner of the screen, select **+New message**. 

4. In the message pane that appears, enter the following information:

	- To: enter **Lynne** and then select **Lynne Robbins** from the user list that appears

	- Add a subject: **Archive Test**

	- Message area: type **Use this email to test archiving.**

5. Select **Send**.

6. Switch to LON-CL2.

7. If necessary, log in as the **Admin** with a password of **Pa55w.rd**.

8. In the **Edge** browser, if there are still signed in Microsoft 365 sessions (such as Outlook or SharePoint), then select one of those tabs, sign out of the current user account, and then close all other **Edge** browser tabs.

9. In the browser tab in which you are signed out, enter the following URL in the address bar: **https://outlook.office365.com**

10. You want to sign into **Outlook on the web** as **Lynne Robbins.** If the **Pick an account** window appears, Lynne’s account won’t appear since she hasn’t signed in before. Therefore, select **Use another account**. 

11. In the **Sign in** window, enter **LynneR@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and then select **Next.**

12. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.

13. In **Outlook on the web**, in Lynne’s **Inbox**, you should see the email message that Holly just sent to Lynne.

14. Back in Lab 3, you changed the assigned retention policy for Lynne’s mailbox to **Office Retention Policy**. This policy contains the **3 Year Move – Archive after three years** personal retention tag that you created in Lab 3. <br/>

	‎Upon receiving this email from Holly, Lynne has decided to tag Holly’s email to automatically archive it after three years instead of two years, which is the default policy.  <br/>
	
	‎To accomplish this, begin by selecting the **Settings** icon in the upper right corner of the toolbar (the gear-shaped icon).

15. In the **Settings** pane that appears, select **View all Outlook settings**. 

16. In the **Settings** window that appears, the **Mail** option is already selected by default in the left-hand pane. In the center pane, scroll down and select **Retention policies**. 

17. In the **Retention policies** pane that appears on the right side of the screen, select **+Add new policy**. 

18. In the **Retention policies** pane, after a few seconds the default and custom retention policies will appear. Select the **3 Year Move - Archive after three years** retention policy that you created in a prior lab, and then select **Save**.

19. Verify you selected the correct retention policy and then close the **Settings** window by selecting the **X** in the upper right corner. This returns you to Lynne’s mailbox.

20. In the **Inbox**, right-click the message that she received from Holly with the subject: **Archive Test**. In the menu that appears, scroll to the bottom and select **Assign Policy**. In the **Assign Policy** menu that appears, under the **Archive Policy** section, select **3 Year Move - Archive after three years.**  <br/>

	‎**Note:** This personal retention policy will now override the parent folder policy for this specific message, which will be moved to Lynne’s In-Place archive mailbox after 3 years.

21. Leave Outlook open in the LON-CL2 VM as you will return there as Lynne in the next task after receiving another email from Holly.


### Task 2 – Test a DLP Policy for Sensitive Emails

In the previous exercise, you created a custom DLP policy that searches emails for sensitive information related to IP addresses in your Adatum tenant. In this exercise, you will send two emails from Holly Dickson to Lynne Robbins; the first will include one IP address, and the second email will include two IP addresses. You will verify how each email is handled due to the DLP policy.

1. Switch to LON-CL1, where you should still be logged into Microsoft 365 as Holly Dickson (**holly@M365xZZZZZZ.onmicrosoft.com)** with a password of **Pa55w.rd**. 

2. You will now send an email from Holly to Lynne, and you will include an IP address in the body of the email. In **Microsoft Edge**, the **Outlook on the web** tab should still be open for Holly. If necessary, select the **Outlook on the web** tab.

3. In the upper left corner of the screen, select **+New message**. 

4. In the message pane that appears on the right-side of the screen, enter the following information:

	- To: enter **Lynne** and then select **Lynne Robbins** from the user list that appears

	- Add a subject: **DLP Policy Test**

	- Message area: type **I will configure this IP address: 192.168.0.1.**

5. Select **Send.**

6. Immediately after sending the email, Holly should receive an email in her Inbox from **Microsoft Outlook** with the subject **Notification: <policy name>** (in this case, <policy name> should be the name of the policy you created that tested for IP addresses in emails, which was **DLP policy test**. Review the content of this email. 

7. You will now send a second message from Holly to Lynne that contains multiple IP addresses. Repeat the process as before for creating an email to Lynne Robbins with the following information: 

	- Add a subject: **Second DLP Policy Test**

	- Message area: **Test IP address 192.168.0.1 and then IP address 172.16.0.1.**

8. Immediately after sending the email, Holly should receive two emails in her Inbox from **Microsoft Outlook**. <br/>

	- The first email should have the subject **Rule detected - High volume of content detected IP address DLP policy**. Select this email and review its contents.  <br/>
	
	- The second email should be a **Message Blocked** notiification for the email that you just sent. Select this email to review its contents. 

11. Switch to LON-CL2. 

12. If you need to sign into the VM, the **Admin** account should appear by default, so enter **Pa55w.rd** in the **Password** field to log in. 

13. You should still be logged into **Outlook on the Web** in the LON-CL2 VM as **Lynne Robbins**. In your **Edge** browser, Lynne’s mailbox should still be open in **Outlook on the web** from when you last used it in the previous task.

14. In Lynne’s **Inbox**, you should see the first message that you sent, but not the second. Remember, when Holly sent the second email, she received a notification that it had been blocked. 

15. Leave both client VMs open for the next lab. Do not close any of the browser tabs.


# End of Lab 6
