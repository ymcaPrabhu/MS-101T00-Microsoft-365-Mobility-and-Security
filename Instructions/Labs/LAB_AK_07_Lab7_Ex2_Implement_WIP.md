# Module 7 - Lab 7 - Exercise 2 - Implement Windows Information Protection  

Now that Holly Dickson has implemented Sensitivity labels as part of her pilot project at Adatum, she is now ready to implement Windows Information Protection (WIP). In your role as Holly Dickson, you will use this exercise to create a WIP policy that will be applied to any member of the WIP Users group who has an MDM-enrolled device in Intune.

### Task 1 – Configure Windows Information Protection

In this lesson you will create a WIP policy and assign it to the WIP Users group that you created in an earlier lab. 

1. Switch to LON-CL1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson.** 

2. In **Microsoft Edge**, if you have the Azure portal open in a tab, then select it now; otherwise, enter **https://endpoint.microsoft.com/** and, if necessary, sign in as **holly@M365xZZZZZZ.onmicrosoft.com.**

3. In the **Microsoft Endpoint manager Admin center**, select **Apps* then  select **App protection policies** and then select **Create Policy** for **Windows 10**.

4. In the **Create policy** window, the steps to create a policy are displayed at the top of the page. You are currently in **Step 1 - Basics**. Enter the following information:

	- Name: **WIP Client Protection**

	- Description: leave blank

	- Enrollment state: **With enrollment****

5. In the **Create Policy** window, in the navigation pane under **Apps**, select **Next**.

6. In the **Create policy** window, you are now in **Step 2 - Targeted apps**. Enter the following information:

	- Protected apps: select **+ Add**. In the **Add apps** pane that appears on the right, scroll to the bottom and select **Office-365-ProPlus-1810-Allowed.xml**, and then select **OK**. 

	- Exempt apps: leave blank as there are no exempt apps in this policy

7. Select **Next**.
8. In the **Create policy** window, you are now in **Step 3 - Required settings**. Enter the following information:

	- Windows Information Protection mode: **Block**
	
	- Corporate identity: verify that it displays **M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) and then select **OK.**

9. Select **Next**.

10. 13. In the **Create policy** window, you are now in **Step 4 - Advanced settings**. Do not change any of the default settings, so select **Next**.

11. In the **Create policy** window, you are now in **Step 5 - Assignments**. Enter the following information:

	- Selected groups: select **+Select groups to include**. In the **Select groups to include** pane that appears on the right, select the **WIP Users** group and then select the **Select** button at bottom of the pane.

12. Select **Next**.

13. In the **Create policy** window, you are now in **Step 6 - Review + create**. Review the settings and then select the **Create** button at the bottom of the page.

17. On the **Apps | App protection policies** window, note the value of the **Deployed** column is **No** for the **WIP Client Protection** policy that you just created. Select **Refresh** on the menu bar above the list of policies. The **Deployed** status should now display **Yes**.

18. Leave your Client 1 VM and browser open for the next lab.

You have now created an **App protection policy** (which is a Windows Information Protection policy) that protects files in Office 365 ProPlus for users with enrolled devices in the **WIP Users** group.


### Task 2 – Use Windows Information Protection

In this exercise you will enroll your LON-CL2 device to Azure AD. You will then test the WIP policy that you created in the prior task by creating a work document and then copy and pasting from it to a personal location. This will test the WIP protection feature that prevents copy and pasting between a protected Word document and an untrusted website in your Edge browser. Since the WIP policy that you created was assigned to the WIP Users group, you must switch to LON-CL2 and create the document while signed in as Joni Sherman, who is one of the members of the WIP Users group.

1. Switch to LON-CL2, where you should still be logged in as the **Admin** account, and you should be logged into **Outlook on the Web** as **Joni Sherman**. 

2. Minimize your **Edge** browser.

2. In the **Search** box on the taskbar at the bottom of the window, type **Work** (not **Word**, but **Work**). In the menu that appears, if **Settings** is not expanded, then select it now. Under **Settings**, select **Access work or school**.

3. In the **Access work or school**  window, select **Connect**.

4. In the **Set up a work or school account**, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant suffix ID provided by your lab hosting provider) in the **Email address** field and then select **Next**.

5. On the **Enter password** window, enter **Pa55w.rd** and select **Sign in**.

6. At this point, the system will register your device with Adatum. On the **You're all set!** window, select **Done**.

7. Open **Microsoft Word**. 

8. Select **Blank document**.

9. If a **What’s New** window opens, close it.

10. In the document, type **Protected business content**.

11. Select **File** from the menu bar above the ribbon, select **Save As** on the left menu, and then select **Browse** from the **Save As** menu.

12. In the **File Explorer** window, you should see a **lock symbol** that appears to the left of the **File name** field. Next to this lock symbol is a drop-down arrow. Select this arrow, and in the menu that appears, select **Work (m365xZZZZZZ.onmicrosoft.com).**

13. Accept the default file name **Protected business content.docx**, change the file path to your **Documents** folder and select **Save**.

14. In the Word document, select the sentence that you typed in the document, then right-click on the selected text and select **Copy**.

15. Select the **Edge** icon on the taskbar. In your browser, open a new tab, click in the Search box and press **Ctrl-V** on your keyboard to paste in the copied text. Instead of seeing the copied text, a pop-up window should appear with the following message: **Can’t use work content here. Your organization doesn't allow you to use work content here.** Select **OK**.

	You have just verified that WIP protection prevents copy and pasting between a protected Word document and an untrusted website in your Edge browser.

16. Leave your LON-CL2 VM and browser open for the next lab.

You have just enrolled the Client 2 VM to your tenant, so the Client app protection policy **WIP Client Protection** that you configured in the last task could be applied to protect the content of a Word document.


# End of Lab 7
