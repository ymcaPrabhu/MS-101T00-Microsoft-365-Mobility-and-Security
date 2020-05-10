# Module 5 - Lab 5 - Exercise 2 - Configure Retention Tags and Policies  

In this exercise, you will configure retention tags and policies, and you will implement archiving with MRM retention tags. 

### Task 1 – Activate In-Place Archiving

In this next phase of your Adatum pilot project, you will access the Security & Compliance Center to activate Holly Dickson’s archive mailbox.   

1. You should still be logged into LON-CL1 as the **Admin** and into **Microsoft 365** as Holly Dickson.

2. In Microsoft Edge, select the **Microsoft 365 admin center** tab; if you closed this tab earlier, then open a new tab and go to https://admin.microsoft.com.

3. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Information governance**, and then under it select **Archive**.

4 On the **Archive** window, note that the archive mailboxes for all users other than Holly Dickson are **enabled**. These archive mailboxes were enabled when the VM lab environment was built for this training course and these users were preconfigured in the tenant. However, since Holly's user account was added in Lab 1, her archive mailbox is **disabled** by default.

5. To enable Holly’s archive mailbox, select **Holly Dickson** in the user list. 

6. In the details pane on the right, Holly’s archive mailbox is currently listed as **disabled**. Select **Enable**, and then in the **Warning** dialog box that appears, select **Yes** to confirm this action.

7. In your Microsoft Edge browser, leave the Office 365 Security & Compliance Center tab open as you will use it in a later task in this lab. 
 

### Task 2 – Create an MRM retention tag and policy in the Exchange Admin Center

As part of your pilot project for Adatum, you will configure MRM retention by creating an MRM retention tag and adding it to a new MRM retention policy. You will also assign several default tags to the policy as well. You will then assign this retention policy to Joni Sherman and Lynne Robbins’ mailboxes.

1. In **Microsoft Edge**, select the **Microsoft 365 admin center** tab.

2. In the **Microsoft 365 admin center**, in the left-hand navigation pane under the **Admin centers** group, select **Exchange**. This will open the Exchange admin center.

3. In the **Exchange admin center**, in the left-hand navigation pane, select **compliance management**.

4. In the **compliance management** window, select the **retention tags** tab that appears at the top of the page.

5. You want to create a retention tag, so select the **plus (+)** **sign** in the toolbar that appears across the list of existing retention tags. In the drop-down menu that appears, select **applied by users to items and folders (personal)**.

6. In **new tag applied by users to items and folders (personal)** window, under **Name**, enter **3 Years Move – Archive after three years**.

7. Under **Retention Action**, select the **Move to Archive** option.

8. Under **Retention period**, select the **When the item reaches the following age (in days)** option and enter **1095** in the retention period field that appears below this option (1095 days = 3 years).

9. In the **Comment** field, enter **Personal tag to archive email three years after being received**.

10. Select **Save**.

11. On the menu bar on the top of the page, select the **retention policies** tab.

12. You want to create a retention policy, so select the **plus (+)** **sign** in the toolbar that appears across the list of existing retention policies. 

13. In **new retention** **policy** window, under **Name**, type **Office Retention Policy**.

14. Below **Retention tags**, select the **(+)** sign.

15. In the **select retention tags** window, select the tag that you just created, whose name starts with **3 Years Move** (the column width will truncate the displayed name).

16. Select **add -&gt;** and then select **OK**.

17. In addition to the personal retention tag that you just added to the retention policy, you also want to add the following default tags as well:

	- Default 2 year move to archive

	- Deleted Items

	- Junk Email

	- Recoverable Items 14 days move to archive

To add these tags, repeat steps 15-17. Hold down the **Ctrl** key as you select each tag in the list; this will enable you to select all four default tags at one time before selecting **add-&gt;.**

18. On the **new retention policy** window, select **Save**.

19. In the **Exchange Admin Center**, in the left-hand navigation pane, select **recipients**.

20. You are now going to apply this retention policy to the mailboxes for your two test users, Joni and Lynne. In the list of recipient mailboxes, select **Joni Sherman** and then select the **pencil (edit) icon** in the toolbar to edit the properties of Joni’s mailbox.

21. In the **Joni Sherman** properties window, select **mailbox features**.

22. On the **Warning** dialog box, select **OK**.

23. Select the drop-down arrow in the **Retention policy** field and select **Office Retention Policy**.

24. Select **Save.**

25. Repeat steps 21-25 for **Lynne Robbins**.

26. Leave your web browser open and proceed to the next task.

You have now created a new retention policy with several retention tags, including a custom personal retention tag. Then you have assigned the retention tags via a retention policy to Lynne and Joni’s mailboxes.


### Task 3 – Create a Retention Policy in the Security and Compliance Center

As part of your pilot project for Adatum, you will create a retention policy in the Security & Compliance Center to preserve the content of all Exchange Online mailboxes from deletion for 7 years after the last modification. 

1. In **Microsoft Edge**, select the **Security &amp; Compliance Center** tab that you left open after completing Task 1.

2. In the left-hand navigation pane, select **Data Governance** and then select **Retention**.

3. In the **Retention** window, select **+Create** to start the wizard that’s used to create a new retention policy.

4. On the **Name your policy** page, type **Exchange Preservation** in the **Name** field and select **Next**.

5. On the **Decide if you want to retain content, delete it, or both** page, leave the **Yes, I want to retain it** option selected, as well as the **For this long** and **7 years**. Do not change these fields.<br/>

	However, in the **Retain the content based on** field, it currently indicates **when it was created**. Select the drop-down arrow for this field and select **when it was last modified**. 

6. Select **Next**.

7. In the **Choose locations** page, select **Let me choose specific locations.** 

8. Scroll down the page and deselect all sliders except for **Exchange email.**

9. Select **Next**.

10. On the **Review your settings** page, review all the settings. If any need to be corrected, select the **Edit** option and make the appropriate correction. Select **Create this policy** to finish the wizard.

11. Do not close your Client 1 VM or Microsoft Edge. Leave your web browser open as well as all tabs for the next lab.

You have now created a new retention policy in the Security & Compliance Center that retains all Exchange emails from all mailboxes for 7 years after last modification.

 # End of Lab 5
 
