# Module 7 - Lab 7 - Exercise 1 - Implement Sensitivity labels with Azure Information Protection  Unfied labels client


In your role as Holly Dickson, Adatum’s Enterprise Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, your next steps are to implement Sensitivity Labels with Azure Information Protection (AIP) and Windows Information Protection (WIP) at Adatum. You will begin by configuring AIP and then using AIP on a client and verifying an AIP policy. You will then perform similar steps for WIP by configuring it for Adatum and then implementing WIP.

### Task 1 – Install the Azure Information Protection Unified Labeling client

To implement Sensitivity labels as part of your pilot project at Adatum, you must first install the AIP client from the Microsoft Download Center.

1. You should still be logged into LON-CL1 as the **lon-cl1\admin** account, and you should be logged into Microsoft 365 as **Holly Dickson** with a password of **Pa55w.rd**. 

2. In **Microsoft Edge**, open a new tab and enter the following URL in the address bar: **https://www.microsoft.com/en-us/download/confirmation.aspx?id=53018**, this will start the download for the AIP Unified label client.

3. In the Microsoft download center tab, the **AzinfoProtection_UL.exe** will prompt a request to **run, save or cancel**. Select **Run** 

4. Once the Download has completed. The **AIP Unifed labeling client** interface will open. select the **I agree** button. You will then be prompted by the User **Accont Control notification** that requests if you want to all the app to make changes to this device? Select Yes.

5. The **AIP Unfied labeling client installer** will finish the installation. Select Close

6. In the **Choose the download you want** window, select **AzInfoProtection.exe** and then select **Next.**

You have successfully installed the AIP Unfied Label client on Client 1 VM.


### Task 2 – Configure Sensitivity Labels

In this exercise you will create an Sensitvity label and add it to the default policy so that it’s valid for all users of the Adatum tenant.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.

2. In **Microsoft Edge**, open a new tab and enter the following URL in the address bar: **https://protection.office.com/**

3. In the **Sign in** dialog box, enter **HOlly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant suffice ID username provided by your lab hosting provider) and then select **Next****.

	**Important:** Your Microsoft 365 tenant came with a default system administrator account already created. The name of this user account is **MOD Administrator**. The user name that you just entered, **admin@M365xZZZZZZ.onmicrosoft.com**, is the user name for the MOD Administrator. 
4. In the **Enter password** dialog box, copy and paste in the **Tenant Password** provided by your lab hosting provider for the **admin@M365xZZZZZZ.onmicrosoft.com** account and then select **Sign in**.

5. At this point you should be in the **Microsoft 365 Security & Complaince Admin center**. On the **Navigation pane** select **classification**, then select **Sensitivity Labels.**

6. In the **Sensitivity Labels** window, there is a Button that states **Turn on now** select the button. this will enable the ability to apply the Sensitivity labels inisde your Micrsoft 365 enviroment.

7. In the **Microsoft 365 Security & Complaince | Sensitivity Labels** window, select **Create a label**.

8. In the **new Senesitivity Label** window, enter the following information:

	- Label display name: **PII**

	- Description : **Documents, files, and emails with PII**

	- Description for admins : **Documents, files, and emails with PII**

9. Select **Next**.

10. In the **Scope** Section confirm that the**Files & Emails** box is checked. Then select **Next**.

11. In the **Sensitivity Labels** window, under **Files** Select both check boxes for **Encrypt files and emails** and **Mark the content of files**, then select **Next**.

12. In the **Sensitivity Labels** window, under **Encryption** Select  the **Remove encryption if the file is encrypted**, then select **Next**.

13. In the **Sensitivity Labels** window, under **Content Marking** set the switch to the**On** postion, then select all check boxes and enter the folloiwing. :
	- Add a watermark : Sensitive do not share.
		- font size : 25
		- Font Color : Red
		- Text layout : Diagonal
			- Select **Save**.

	- Add a header : Sensitive do not share.
		- font size : 25
		- Font Color : Red
		- Align text : Center
			- select **Save**.
	- Add a footer : Sensitive do not share.
		- font size : 25
		- Font Color : Red
		- Align text :  Center
			- select **Save**.

14. In the **Sensitivity Labels** window, under **Content Marking** select **Next**. 

15. In the **Sensitivity Labels** window, under **Auto-Labeling for Office apps**  set the switch to the**On** postion. then enter the following. :

	- Detect content that matches these condistions :
		- content contains:
			- Default
			- All of these
			- Select the **Add** dropdown then **Sensitve info types**.
			- a new window will open then select **Select All**. then select **Add**.
		- When Contnent Matches these conditions :
			- **Automatically apply the Label**.

		- Display this message to users when the label is applied :
			- **Sensitivie content has been dectected and will be encrypted**.
		

16. In the **Sensitivity Labels** window, under **Auto-Labeling for Office apps** select **Next**.

17. In the **Sensitivity Labels** window, under **Define Protection settings for groups and sites** select **Next**.

18. In the **Sensitivity Labels** window, under **Review your settings and Finish** review and validate the settings that you have implemented and then select **Create label**.

19. There should be an error message the pops up. this message is stating the rule is to long. this is to show you the maxium amount selections you can make at one time per rule which is **49152**. To correct this issue go back to **Auto-labeling for Office apps** under the **Files** section, and select the **Trash can** next to the **Default** action and repeat **step 15** but instead of selecting  **Select all**, just select **ABA routing number** and **U.S. Social security Number.**

20. In the **Sensitivity Labels** window, under **Review your settings and Finish** review and validate the settings that you have implemented and then select **Create label**. 

21. Congratulations you have successfully added a New custom label name PII,
Select **Done**.

22. Now its time to publish the **PII** label. In the **Sensitivity labels** section, select **Publish Labels**.

23. In the **Sensitivity Labels policy** window, under **Choose sensitivty labels to publish** select choose **Choose sensitivty labels to publish**. Then select **PII** and select **Add**.

24. In the **Sensitivity Labels policy** window, under **Choose sensitivty labels to publish** select **Next**.

25. In the **Sensitivity Labels policy** window, under **Publish to users and groups** select **Choose users or groups**.

26. In the **Publish to users and groups** window, under **Edit Locations**  select **Add**. A new window will appear select **All company** and then select **Add**.

27. In the **Publish to users and groups** window, under **Edit Locations**  select **Done**

28. In the **Sensitivity Labels policy** window, under **Publish to users and groups** select **Next**.

29. In the **Sensitivity Labels policy** window, under **Policy settings** select **PII** under the **Apply this label by default to documents and emails** section. then select the **Users must provide justification to remove a label or lower classification label** checkbox. Then select **Next**.

30. In the **Sensitivity Labels policy** window, under **Name your policy** enter the following information:

	- Name : **PII Policy**

	- Description : *This policy is to detect and apply an encryption to emails and documents that have sensitive information such as ABA bank routing numbers and US social security numbers. the user must provide an explanation for removing the classification label.*

31. In the **Sensitivity Labels policy** window, under **Name your policy** select **Next**.

32. In the **Sensitivity Labels policy** window, under **Review your policy** select **Finish**.

33. Congratulations you have successfully added a New custom label Policy name PII policy, Select **Done**.

### Task 3 – Assign an Sensitivity label to a document

In this exercise you will use the Sensitivity label that you created in the previous task to classify a document. For this task, you will sign into Microsoft Apps as Alex Wilber, who is a regular user without any elevated privileges.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.

2. In **Microsoft Edge**, open a new tab and enter the following URL in the address bar: **https://portal.office.com/** 

3. then sign in as **AlexW@M365xZZZZZZ.onmicrosoft** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider) and then select **Next**.

4. On the **Enter password** window, enter **Pa55w.rd** and select **Sign in**.

5. Open **Word online,** select **Blank document**.
	


6. If the **Privacy** window appears, close it.

7. In the **Word** document, type **Testing personally identifiable information (PII).**

8. There are two new additions to Word that appear as a result of having Sensitivity labels enabledat the start of this exercise: <br/>

	- In the **Home** ribbon, locate the **Sensitivity** group. 
	
	- Below the **Home** ribbon, locate the **Sensitivity dropdown**tab Congratulations you have successfully added a New custom label name PII, (**Note:** you may not see it if it hasn't been 24 hours) Select **Search**.bar. then type **Sensitivity** the select the arrow to view the newly created a label titled **PII** in the prior task, **PII** will appear in the left side of the Sensitivity label bar. 
	
	Select the **PII** button on the **Sensitivity** bar.

9. In the **Justification Required** window appears, select the following options:

	- Select Other (explain): **Testing what happens when i remove the label**

10. In the **Justification Required** window appears, select  "Change".

11. Re-apply the Senstivity label by selecting the**Sensitivity** group and then selecting **PII**

12. Enter the following text: **111-11-1111**

13. Save the file by selecting **Docutment1** from the **Header** tab in the Middle of word online. 

14. Confirm the file **Location** says **Alex Wilber>Documents**. 

15. In the **Word Online** rename the file to **ProtectedDocument** as the name of the file and then select out of the **file name** section.

16. Select the **Share** option in the top right corner.

17. Select the Anyone with the link can edit. change this to **Specific people** then select **Apply**.

18. In the **Enter a name or Email address**, Enter **Joni Sherman** and select **Send**.

You have just successfully created an AIP protected Word document that is read-only protected, and is accessible only by its creator, Alex Wilber, and Joni Sherman (with Read-only permission).


### Task 4 – Verify Sensitivity label policy

In the prior task, you created a Word document and protected it with a Sensitivty label by inserting a watermark and restricted permissions. To verify whether the protection that you assigned to the document works, you will first email the document to Joni Sherman and to your own personal email address. You will then test what functionality is possible for both Joni and Alex Wilber.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Alex Wilber**. 

2. If you have **Outlook on the web** open in a tab in your **Edge** browser, then select it now and proceed to the next step; otherwise, if you have a tab with the **Microsoft Office Home** page, then select the tab, select **Outlook**, and then proceed to the next step. If you have neither tab open, then in a new tab enter **https://outlook.office365.com** and sign in as **AlexW@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).

3. In **Outlook on the web**, select **New Message** in the upper left part of the screen.

4. In the right-hand pane, enter the following email information:

	- To: Enter **Joni** and then select **Joni Sherman** from the user list. 

	- CC: Enter your own personal email address (not Holly's; in this case, enter your own email address)

	- Add a subject: **Protected Document Test**

	- Add a message or drop a file here: **If you can open the protected and restricted document attached to this email, then try to change it.**

	- Select **Attach** from the top menu and under  **Suggested Attachments**.  select **ProtectedDocument.docx** file that you created in the prior task, and then select **Open.**

5. Select **Send**.

6. Switch to LON-CL2. 

7. In LON-CL2, you should be logged into **Outlook on the Web** as **Lynne Robbins** from a previous lab exercise. Sign out as Lynne and then navigate to **https://outlook.office365.com** and sign back in as Joni Sherman (**JoniS@M365xZZZZZZ.onmicrosoft.com**, where ZZZZZZ is the tenant suffix ID provided by your lab hosting provider) with a password of **Pa55w.rd**.

8. In Joni’s **Inbox** in **Outlook on the web**, select the email that Holly just sent her, and then select **Open** file to open it. 

9. You should receive an notification indicating that the file is protected 

10. This will return you to **Outlook on the web** with the email still displayed in the right-hand pane. In the body of the email, the document appears in a tile, with a drop-down arrow in the lower right corner of the tile. Select the drop-down arrow, and in the menu, select **Download**.

11. In the notification bar that appears at the bottom of the screen, select **Save.** 

12. Once the file has finished downloading, in the notification bar, select **Open.**

13. **Microsoft Word** should open along with a **Sign in** window (it may open behind the Outlook window, in which case select the **Word** icon on the taskbar to bring it forward). 

14. Because the file is RMS protected and no AIP unified labeling client is installed on LON-CL2, you need to use the native RMS features of Word Microsoft Apps and register this installation to Joni’s account. <br/>

	‎In the **Sign in** window, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** and then select **Next.** 

15. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in.**

16. In the **Use this account everywhere on your device** window that appears, select **This app only** to register this Office 365 ProPlus installation to **Joni Sherman’s** Microsoft 365 account.

17. The file should open in Word, since you assigned Joni with Read-only permission. Review the three notification bars that appear above the document. 

18. Try to change the file. Word should not recognize any keystrokes, and it should display the following message above the taskbar: **This modification is not allowed because the document is open for viewing only.** <br/>  

	‎**Note:** You have just verified that the permissions assigned to the file are working properly. Joni can read the file (since she was assigned Read-only permission), but she is unable to change it (no one was assigned Edit permission).

19. Close Word.

20. You will now test what happens when you attempt to open the document that was sent to your personal email address. Use your phone or classroom PC to access your personal email address. Open the email that you (in the role of Holly) just sent to your personal email address, and then attempt to open the attached file. 

21. You should receive a messaging indicating that you are not signed into Office with an account that has permission to access the document. You can optionally sign in with an account that has permission to access the file, or request access from the **AlexW@M365xZZZZZZ.onmicrosoft.com** account, or Cancel out of the operation. Select **Cancel**.  <br/>

	‎Since only Joni was assigned permission to read the document, you just verified that Azure Information Protection protected the document based on the PII policy parameters that you configured.

22. Remain signed into LON-CL2 and signed into Outlook on the Web as Joni. Do not close your browser.


# Proceed to Lab 7 - Exercise 2
