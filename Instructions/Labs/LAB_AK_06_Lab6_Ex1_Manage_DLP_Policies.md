# Module 6 - Lab 6 - Exercise 1 - Manage DLP Policies  


In your role as Holly Dickson, Adatum’s Enterprise Administrator, you have Microsoft 365 deployed in a virtualized lab environment. As you proceed with your Microsoft 365 pilot project, your next steps are to implement Data Loss Prevention (DLP) policies at Adatum. You will begin by creating a custom DLP policy, and then you’ll test DLP policies related to email message archiving and emails with sensitive data. 

### Task 1 – Create a DLP policy with custom settings

In this lesson you will create a Data Loss Prevention policy in the Security & Compliance Center to protect sensitive data from being shared by users. The DLP Policy that you create will inform your users if they want to share content that contains IP addresses.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**. 

2. In **Microsoft Edge**, the Office 365 Security & Compliance Center tab should still be open; if not, then open a new tab and navigate to **https://protection.office.com**.

3. In the **Security &amp; Compliance Center**, in the left-hand navigation pane, select **Data loss prevention** and then select **Policy**.

4. In the **Policy** window, select **+Create a policy** to start the wizard for creating a new data loss prevention policy.

5. On the **Start with a template or create a custom policy** page, there are four types of policies listed in the left-hand pane - Financial, Medical and health, Privacy, and Custom. The first three (Financial, Medical and health, and Privacy) provide templates that can be used to create a policy. The **Custom** type is not based on a template. The column in the left-hand pane displays the policy type, while the middle pane displays the available templates to choose from for that policy type. When you select a template in the middle pane, the right-hand pane displays the type of information that is protected in that tempate. <br/> 

    Select **Financial** in the left-hand pane and note the various templates that you can choose from in the middle pane. Select one or two of the templates to see what type of information it protects. Do the same for the **Medical and health** and **Privacy** policy types.  <br/>
  
    Select **Custom** in the left-hand pane, which automatically selects **Custom policy** in the middle pane (since there are no templates to choose from for this policy type). Select **Next**.

6. In the **Name your policy** page, enter **IP Address DLP Policy** in the **Name** field and **Protect IP addresses from being shared** in the **Description** field. Select **Next**.

7. On the **Choose locations** page, select the **Protect content in Exchange email, Teams chats, and channel messages and OneDrive and SharePoint documents** option (if it isn't already selected by default) and then select **Next**.

8. On the **Customize the type of content you want to protect** page, select the **Find content that contains:** option (if it isn't already selected by default). 

9. Under **You must select at least one classification type**, select **Edit.**

10. In the **Choose the types of content to protect** page, select the **Add** drop-down field, and in the drop-down menu, select **Sensitive info types**.

11. In the **Sensitive info types** window, select **(+) Add**.

12. In the search field type **Address** and wait until the search results are displayed.

13. In the list of search results, select the **IP Address** check box and then select **Add.**

14. Once you receive the message indicating **1 sensitive info type added,** select **Done**.

15. On the **Choose the types of content to protect** window, under the **Content contains** bar, select **Any of these** in the drop-down field (this should be selected by default), and then select **Save**.

16. On the **Customize the type of content you want to protect** page, **IP Address** should now appear under the **Find content that contains** option.

17. Verify that the **Detect when this content is shared:** check box is selected.

18. In the field below this, select the drop-down arrow and select **only with people inside my organization**.

19. Select **Next**.

20. On **What do you want to do if we detect sensitive info?** page, there are two groups of settings that you must configure: <br/>

    - Under the **Notify users when content matches the policy settings** section, verify the **Show policy tips to users and send them an email notification** check box is selected. Select **Customize the tip and email**. <br/>
    
        In the **Customize policy tips and email notifications** window, the email notification option is selected by default. However, sending policy tips is not selected by default, so select the **Customize the policy tip text** check box (otherwise, a policy tip will not be displayed). In the policy tip field that appears, enter **Warning: The email contains sensitive info (IP Address).** Select **OK**.

    - Under the **Detect when a specific amount of sensitive info is being shared at one time** section, verify the **Detect when content that's being shared contains** option is selected. In the field below this, **10** is entered. Change this to **2** and then select **Next.**

21. On the **Customize access and override permissions** page, the **Let people who see the tip override the policy** option is turned On by default. Leave this option **On**, but also select the **Require a business justification to override** check box, and then select **Next**.

22. On the **Do you want to turn on the policy or test things out first?** page, select **Yes, turn it on right away** and then select **Next**.

23. Check the configuration on the **Review your settings** page. Two policy settings should be displayed (these are dependent on the number of IP addresses in the message): <br/>

    - If the content contains an IP address, then notify people with a policy tip and email the message.

    - If there are at least 2 instances IP addresses, then block access to the content and send an incident report with a high sensitivity level but allow people to override it if they provide a business justification. 
        
    Select **Back** if you need to correct any settings, and then select **Create** once you’re satisfied with the settings.

You have now created a DLP policy that scans for IP addresses in emails and documents that are sent or shared in your organization.


# Proceed to Exercise 2 
