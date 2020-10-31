# Module 2 - Lab 2 - Exercise 2 - Implement a Safe Links Policy

In this first phase of your pilot project for Adatum, you want to create a Safe Links policy and then validate the policy to ensure that it works properly.


### Task 1 – Create a Safe Links Policy

In this task, you will add the **tailspintoys.com** URL to the company-wide list of blocked URLs, and you will create a Safe Links policy that applies to all users in your tenant.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Admin** account, and you should still be logged into Microsoft 365 as **Holly Dickson**.

2. After finishing the previous task, you should still be in the **Microsoft 365 Security and Compliance center**. If not, in your browser, enter **https://protection.office.com.**

3. In the **Security &amp; Compliance center**, in the left-hand navigation pane, the **Threat Management** group should still be expanded from the prior task; if not, expand it now. Under this group, select **Policy**.

4. In the **Policy** window, select the **ATP Safe Links** tile.

5. In the **Safe Links** window, note that there are two sections of policies that can be created: **Policies that apply to the entire organization**, and below that, **Policies that apply to specific users.**

6. Under the **Policies that apply to the entire organization** section, there is one policy already defined for this group, which is the **Default** policy. Since this policy is already selected, select the **pencil (edit)** icon on the menu bar above the list.

7. In the **Safe links policy for your organization** window, under the **Settings that apply to content across Office 365** section, you can enter any URLs that you want to have blocked. For Adatum's pilot project, in the **Enter a valid URL** field, enter **http://tailspintoys.com** and then select the **plus (+)** sign to add it to the policy.

8. Select **Save**, and then in the dialog box indicating it was successfully saved, select **OK**.

9. Scroll down to **Policies that apply to specific users** section and select the **plus (+)** sign to add a new user policy.

10. In the **new safe links policy** window, enter the following information:

    - Name: **All company users**

    - Select the action for unknown potentially malicious URLs in messages: Select **On – URLs will be rewritten and checked against a list of known malicious links when user clicks on the link**.

    - Select the action for unknown potentially malicious URLs within Microsoft Teams: Leave set to **Off**

    - Apply real-time URL scanning for suspicious links and links that point to files: Select this check box.

    - Wait for URL scanning to complete before delivering the message: Select this check box.

    - Apply safe links to email messages sent within the organization: Select this check box.

    - In the **Applied To** section, below the **If…** condition, select the drop-down arrow in the **Select one** field and then select **The recipient domain is**.

    - In the pop-up window that appears, the only available domain is **xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider). Select **add-&gt;** and then select **OK.**

11. Select **Save** to close the window, and then select **OK** in the dialog box once the information is successfully saved.

12. Leave the Office 365 Security &amp; Compliance tab open for use in Task 3.

### Task 2 – Validate the Safe Links Policy

In this task, you will test the Safe Links Policy that you just created that blocks links to the http://tailspintoys.com URL.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.

2. In your **Microsoft Edge** browser, select the **Microsoft Office Home** tab and then select **Outlook.**

3. In the top right corner of Outlook, verify that the user icon is **HD** (for Holly Dickson). If the user icon is **HD**, then open a new tab in Edge and proceed to the next step. <br/>

    If the user icon is not **HD** (for example, if it's **MA** for the MOD Administrator), then select the user icon circle, and in the **My account** pane that appears, select **Sign out**. After you are signed out of the account, a good best practice that you should follow when signing out as one user before signing in as another is to close all other open tabs in your browser so that you don't confuse those tabs (associated with the previous user) with the new tabs that you will open for the new user. Only the tab with the sign-out message should be open. 

4. Enter the following URL in the address bar: **https://outlook.office365.com**

5. In the **Pick an account** window, select **Holly@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider). In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.

6. On the **Stay signed in?** dialog box, select the **Don't show this again** check box and then select **Yes.**

7. On the Outlook sign in page, select your **Language** and **Time zone** and then select **Save**.

8. In **Outlook on the web**, verify that **HD** is displayed in the user icon in the upper right corner of the form.

9. Select **New Message** in the upper left part of the screen.

10. In the email form in the right-hand pane, enter the following information:

    - To: You will be sending an email to the MOD Administrator, so enter **mod** in the **To** field and then select the **MOD Administrator** email address from the user list.

    - Add a subject: **Free stuff for Adatum users**

    - body of the message: **Please click on me for free toys from TailSpin Toys.**

11. Select the text that you added in the body of the message.

12. Below the body of the message is a long row of formatting icons. Select the **Insert hyperlink** icon, which depicts two overlapping circles.

13. In the **Insert link** window, the text that you highlighted in the body of the message should be displayed in the **Display as** field. In the **Web address (URL)** field, enter the following URL: **http://tailspintoys.com/aboutus/freetoys**.

14. Select **OK**.

15. In the body of the email, the message should still be selected. Click anywhere in the body of the message to remove the highlighting. The color of the text should now be blue, and it should be underlined, indicating that this message is hyperlinked to a URL.

16. Select either **Send** button (top or bottom of the form).

17. You now want to go the MOD Administrator&#39;s Inbox in Outlook and validate whether the ATP policy you created in the prior task worked on the email that you just sent from Holly to the MOD Administrator.<br/>

    To do this, you must first switch the Client 2 VM (**LON-CL2**). 

18. Log into the LON-CL2 VM as the **Admin** account by entering **Pa55w.rd** in the **Password** field.

19. Select the **Microsoft Edge** icon in the taskbar, maximize the window and then enter the following URL in the address bar: **https://outlook.office365.com**

20. In the **Sign-in** window, enter **admin@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider) and then select **Next**.

21. In the **Enter password** window, enter the tenant password provided by your lab hosting provider and select **Sign in**.

22. Close the **Let Microsoft Edge save and fill your password for this site next time?** banner by selecting **Never**.

23. On the **Stay signed in?** dialog box, select the **Don't show this again** check box and then select **Yes.**

24. You will have to navigate through a series of **Welcome** windows. Continue selecting the right arrow (**>**) until you reach the final window, and then select **Get started**.

25. In the MOD Administrator&#39;s **Inbox**, open the email that was sent by Holly.

26. When you hover over the blue link that appears in the body of the email, you can see a long URL in the bottom of the browser window; this URL starts with **https://namXX.safelinks.protection.outlook.com** (wehre XX is a number assigned to the policy) <br/>

27. Select the hyperlink in the body of the message to open it. A new tab should open in your **Edge** browser that takes you to the URL you just saw in the prior step. This site should display the following warning message: **This website has been blocked per your organization's URL policy.** This not only indicates that opening this website might not be safe, but it also verifies that the ATP Safe Links policy you just created is working properly.

28. Leave the Client 2 VM open and leave Outlook open to the MOD Administrator's Inbox for the next lab.


# End of Lab 2

