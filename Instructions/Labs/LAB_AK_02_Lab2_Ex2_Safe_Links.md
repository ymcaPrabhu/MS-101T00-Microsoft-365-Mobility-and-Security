# Module 2 - Lab 2 - Exercise 1 - Implement ATP Policies  

In this first phase of your pilot project for Adatum, you want to create an ATP Safe Links policy and then validate the policy to ensure that it works properly.


### Task 1 – Create a Safe Links Policy

In this task, you will add the URL **tailspintoys.com** to the company-wide list of blocked URLs, and you will create an ATP safe links recipient policy that applies to all users in your tenant.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **lon-cl1\admin** account, and you should still be logged into Microsoft 365 as **Holly Dickson**.
2. After finishing the previous task, you should still be in the Microsoft 365 Security and Compliance center. If not, in your browser, enter **https://protection.office.com.**
3. In the **Security &amp; Compliance center**, in the left-hand navigation pane, select **Threat Management** and then select **Policy**.
4. In the **Policy** window, scroll to the right (if necessary) and select the **ATP Safe Links** tile.
5. In the **Safe Links** window, note that there are two sections of policies that can be created: **Policies that apply to the entire organization**, and below that, **Policies that apply to specific recipients.**
6. Under the **Policies that apply to the entire organization** section, there is only one policy in the list, which is the **Default** policy. Since this policy is already selected, select the **pencil (edit)** icon on the menu bar.
7. In the **Safe links policy for your organization** window, under the **Settings that apply to content across Office 365** section, you can enter any URLs that you want to have blocked. For this test lab, in the **Enter a valid URL** field, enter **http://tailspintoys.com** and then select the **plus (+)** sign to add it to the policy.
8. Select **Save**.
9. Scroll down to **Policies that apply to specific recipients** and select the **plus (+)** sign to add a new recipient policy.
10. Insert the following to the windows fields:

    - Name: **All company users**

    - Select the action for unknown potentially malicious URLs in messages: This is set to Off by default. Select **On – URLs will be rewritten and checked against a list of known malicious links when user clicks on the link**.

    - Check the **Apply safe links to email messages sent within the organization** check box.

    - In the **Applied To** section, below the **If…** condition, select the drop-down arrow in the **Select one** field, and then in the drop-down menu, select **The recipient domain is**.

    - In the pop-up window that appears, the only available domain is **M365xZZZZZZ.onmicrosoft.com**. Select **add-&gt;** and then select **OK.**

11. Select **Save** to close the window.
12. Leave the Office 365 Security &amp; Compliance tab open for use in Task 3.

### Task 2 – Validate the Safe Links Policy

In this task, you will test the Safe Links Policy that you just created that blocks links to the http://tailspintoys.com URL.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **lon-cl1\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.
2. In your **Microsoft Edge** browser, select the **Microsoft Office Home** tab and then select **Outlook.**
3. If you receive a **We updated Outlook** message, select **Not Now**, or if you see a **Welcome** message, then close it.
4. In **Outlook on the web**, select **New Message** in the upper left part of the screen.
5. In the right-hand pane, enter the following email information:

    - To: You will be sending an email to the MOD Administrator, so enter **mod** in the **To** field and then select the **MOD Administrator** email address from the dropdown list.

    - Add a subject: **Free stuff from Microsoft**

    - Add a message or drop a file here: **Please click on me for free toys from Microsoft.**

6. Select the text that you added in the body of the message.
7. At the bottom of the detail pane, below the body of the message, is a taskbar. On the taskbar, select the **ellipsis (…)** icon to display more formatting options.
8. In the icon window that appears, select the **Insert Link** icon, which is the picture of two combined circles.
9. In the **Insert link** window, the text that you highlighted in the body of the message should be displayed in the **Text to display** field. In the **Web address (URL)** field, enter the following URL: **http://tailspintoys.com/aboutus/freetoys.**
10. Select **OK**.
11. In the body of the email, the message should still be selected. Click anywhere in the body of the message to remove the highlighting. The color of the text should now be blue and it should be underlined, indicating that this message is hyperlinked to a URL.
12. Select **Send** in the menu bar that appears above the message (or the **Send** button at the bottom of the page).
13. You now want to go the MOD Administrator&#39;s Inbox in Outlook and validate whether the ATP policy you created in the prior task worked on the email that you just sent from Holly.<br/>

    To do this, you must switch the Client 2 VM (LON-CL2). In the **Virtual machine** field at the top of the page, select the Client 2 VM (LON-CL2).
14. Log into the LON-CL2 VM as the **Admin** account by entering **Ps55w.rd** in the **Password** field.
15. Select the **Microsoft Edge** icon in the taskbar, maximize the window and then enter the following URL in the address bar: **https://outlook.office365.com**
16. Since you want to sign in as the MOD Administrator, in the **Sign-in** window, enter **admin@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) and then select **Next**.
17. In the **Enter password** window, enter the password provided by your lab hosting provider and select **Sign in**.
18. Close the **Let Microsoft Edge save and fill your password for this site next time?** banner by selecting **Never**.
19. On the **Stay signed in?** dialog box, select the **Don't show this again** check box and then select **Yes.**
20. Close the **Welcome** window that appears.
21. In the MOD Administrator&#39;s **Inbox**, open the email that was sent by Holly.
22. When you hover over the blue link that appears in the body of the email, you can see a long URL in the bottom of the browser window; this URL starts with **https://nam03.safelinks.protection.outlook.com**.<br/>

    When you select the hyperlink to open it, a new tab in **Edge** opens that displays the following warning message: **Opening this website might not be safe.** This message indicates that your ATP Safe Links policy is working correctly and access to the URL is blocked with ATP Safe Links.
23. Leave the Client 2 VM open and leave Outlook open to the MOD Administrator&#39;s Inbox for the next lab.


# End of Lab 2

