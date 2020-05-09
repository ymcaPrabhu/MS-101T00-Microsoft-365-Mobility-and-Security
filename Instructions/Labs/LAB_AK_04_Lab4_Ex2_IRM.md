# Module 4 - Lab 4 - Exercise 2 - Validate Information Rights Management 

In this exercise, you will learn how to validate Information Rights Management for both Exchange Online and SharePoint Online.
 
### Task 1 - Validate Information Rights Management for Exchange Online

In the prior exercise, you set up Information Rights Management in Exchange Online for Adatum. In this exercise, you will validate that configuration by sending a protected email from Holly Dickson to Alex Wilber. You will then log into Alex’s mailbox on the Client 2 VM (LON-CL2), open the email, and verify that it’s protected.  

1. On the Client 1 VM (LON-CL1), you should still be logged into the Microsoft 365 admin center as Holly Dickson. 

2. In the earlier exercise in which you created an eDiscovery alert, you opened **Outlook on the web** for Holly. This tab should still be open in your browser; if not, open a new tab in your browser and enter the following URL: **https://outlook.office365.com**

3. At the top of the left-hand navigation pane, select **+New message** to create a new email.

4. You want to send the email to **Alex Wilber**. Type **Alex** in the **To** field and select **Alex Wilber** from the list of users that are displayed.

5. Enter a **Subject**, and then type some text in the message body. 

6. In the menu bar above the message pane, select **Encrypt** (this option appears because you set up IRM in Exchange in the prior task).

7. This displays a message below it that indicates the message is encrypted. In this message box, select **Change permissions**, which opens a **Change permissions** dialog box.

8. In the **Change permissions** dialog box, in the **Choose how recipients can interact with this message** field, select the drop-down arrow, select **Do not forward**, and then select **OK**. 

9. Select **Send** to send the email to Alex. 

10. Switch to the Client 2 VM (LON-CL2).

11. If you need to log in as the **Admin** account, then do so with a password of **Pa55w.rd**.

12. In an earlier lab exercise, you opened **Outlook on the Web** for Lynne Robbins. You must log out as Lynne so that you can sign back in as Alex. <br/>

	Select Lynne's user icon in the upper right corner, and in her **My account** window, select **Sign out**. Once you are signed out, close any other tabs in your browser. 

13. In your **Edge** browser enter the following URL in the address bar: **https://outlook.office365.com**. 

14. In the **Pick an Account** window, only Lynne's account appears. Select **Use another account** and log in as **AlexW@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) with a password of **Pa55w.rd**.<br/>

15. Verify that Alex received the email that you sent from Holly that is IRM protected. IRM protected emails display a lock icon to the right of the message. Select the message to display it in the right-hand pane.

16. In the message pane for this email, a message that says **Do Not Forward: Recipients can’t forward, print, or copy content** should appear.

17. In the message pane for this email, note how the **Forward** arrow is disabled. 

18. Select the **ellipsis icon (More actions)** to the right of the disabled Forward arrow. In the menu bar that appears, scroll down and verify the **Print** option is also disabled.

19. You want to remain logged into the Office 365 as Alex Wilber on LON-CL2 for the next task, so leave your browser tabs open and proceed to the next task. 

 
### Task 2 - Validate Information Rights Management for SharePoint Online

In Lab 1, you enabled Information Rights Management for Adatum in SharePoint Online. Ideally, you would have enabled IRM for SharePoint Online at the start of this exercise, just as you did when enabling IRM for Exchange Online. However, since it can take an hour or more for IRM to show up in SharePoint Online once it’s enabled, that task was moved to Lab 1 so that by the time you got to this task, IRM would be ready for you in SharePoint.

You will begin by having Holly create a new SharePoint site collection. You will then configure it for Information Rights Management, share it with Alex Wilber, and then have Alex validate IRM for the site. 

1. Switch to the LON-CL1 VM where you should still be logged into the Microsoft 365 admin center as Holly Dickson.

2. In the **Microsoft 365 admin center**, scroll down through left-hand navigation pane and under **Admin centers**, select **SharePoint**. This will open the SharePoint admin center.

3. In the **SharePoint admin center**, in the left-hand navigation pane, select **More features**.

4. In the **More features** window, scroll down to **Classic site collections page** and select **Open**.

4. On the **Site Collections** window, in the ribbon at the top, select **New** and then select **Private Site Collection**

5. On the **new site collection** window, enter the following information:

	- Title: **Marketing**  

	- Web Site Address: The web site URL will be **https://m365xZZZZZZ.sharepoint.com/sites/marketing**. As you can see, the address is broken into 3 fields. The first field displays the **https://m365xZZZZZZ.sharepoint.com** portion of the URL, and the second field display the **/sites/** portion. Do not change these fields. In the third field, which is blank, enter **marketing**.

	- Language: select your language

	- Select a template: leave the default value of **Team site (classic experience)** as the selected value from the Collaboration tab

	- Time zone: select the appropriate time zone in which the team site is located 

	- Administrator: Enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and then select the **Check Names** icon to the right of the field; once the username is validated, it will be replaced with **Holly Dickson.**

	- Server Resource Quota: leave the default value of **300**

6. Select **OK.** 

7. If the new **Marketing** site collection does not appear in the **Site Collections** list after a couple of minutes, select the **Refresh** icon to the left of the address bar. If it still doesn't appear, wait another minute or two and refresh the list again. Continue until the new site collection apears. 

9. In your web browser, open a new tab and enter the following URL in the address bar: **https://M365xZZZZZZ.sharepoint.com/sites/marketing** (where ZZZZZZ is your tenant ID provided by your lab hosting provider)

10. On the **Marketing** site, in the left-hand navigation pane, select **Documents.** 

11. In the **We’ve got a new look** window, select **NOT NOW**.

12. In the **Documents** page for the **Marketing** site, at the top right, select the **gear (Settings)** icon and then select **Library settings**. 

13. On the **Documents > Settings** page, in the **Permissions and Management** column, select **Information Rights Management**. 

14. On the **Settings > Information Rights Management Settings** page, select the **Restrict permissions on this library on download** check box. 

15. In the **Create a permission policy title** field, enter **Marketing Policy**. 

16. In the **Add a permission policy description** field, enter **Marketing policy for downloads**. 

17. Select **SHOW OPTIONS**. 

18. In the **Configure document access rights** section, select the **Allow viewers to write on a copy of the downloaded document** check box and then select **OK**. 

19. In the top-right corner of the **Documents > Settings** page, select **Share**.

20. In the **Share ‘Marketing’** window, in the **Invite people** field, enter **Alex**, then select **Alex Wilber** from the user list, and then select **Share**.

21. Select the **Start** icon in the bottom left corner fo the taskbar, and then in the Program menu, select **Microsoft Word**.

22. When **Microsoft Word** opens, select **Blank document**.  

23. Enter some text in the document, then save the file to the **Desktop** as whatever file name you wish (make sure you save it to the Desktop as you will upload it from there in the next few steps).

24. Close Word.

25. Now that Holly has created this new SharePoint site and used IRM to restrict permissions on the site, she has asked Alex Wilber to test this site to validate whether IRM is working for SharePoint Online. Alex will perform this test on the Client 2 (LON-CL2) VM.<br/>

	‎Switch to the **LON-CL2** VM, where you should still have **Outlook on the Web** open in your **Microsoft Edge** browser from the prior task. You should still be logged in as **Alex Wilber**.

26. ‎In the browser, open a new tab and enter the following URL in the address bar to navigate directly to the Marketing site: **https://M365xZZZZZZ.sharepoint.com/sites/marketing** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider)

27. If a **We've got a new look** window appears, select **NOT NOW**.

28. On the **Marketing** site, select **Documents** on the left-hand pane.  

29. On the **Documents** page, in the menu bar, select **Upload**, and then in the drop-down menu select **Files**. 

30. In the **File Explorer** window, select the address bar at the top of the form and enter the following: \\LON-CL1\C$\Users\Admin\Desktop\<file name.docx>  <br/>

	This will upload the file to the **Documents** page in the **Marketing** site collection.

31. In the list of Documents, right-click on **TestDocument.docx**, select **Open**, and then select **Open in browser**. 

32. Verify that the **Marketing Policy** displays in a warning message at the top of the page. 

33. Try to enter some text in the document. Verify that Alex cannot edit the document in Word Online because it’s protected in this site collection. A Read-only information line will display at the top of the page indicating the document is read-only.

34. Leave your browser open for the next lab. 


# End of Lab 4
