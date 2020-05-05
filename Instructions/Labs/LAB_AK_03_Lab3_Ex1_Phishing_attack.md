# Module 3 - Lab 3 - Exercise 1 - Conduct a Spear Phishing attack using the Attack Simulator

Holly Dickson is concerned that some users at Adatum may require education about phishing attacks. As part of her pilot project, Holly has decided to use the Microsoft 365 Attack Simulator to determine her users' susceptibility to phishing attacks.


### Task 1: Enable Mulit-factor authentication for the Global Admin
To use Microsoft's Attack Simulator to simulate a phishing attack, you must first enable Multi-Factor Authentication (MFA) for your organization. For her pilot project, Holly does not want to set up MFA for the Adatum users at this point in time; however, to use the Attack Simulator, she must enable MFA. So in this task, she will enable MFA for Adatum, and then after she finishes running the Attack Simulator, she will turn MFA back off. 

Enabling MFA is a twpo-step process: you must first enable security defaults for your organization, and then you must enable Modern Authentication. As of October 2019, all new Microsoft 365 subscriptions comes with both of these options enabled. However, your lab hosting provider has disabled security defaults, so MFA is not enforced for Adatum. In this lab, you will enable security defaults, which  turns on MFA since Modern Authentication is enabled. After launching the spear phishing attack using the Attack Simulator in the next task, you will disable the security defaults so that MFA is not enforced for the remainder of the labs in this course. 

**Important:** To implement MFA, you will need to use your mobile phone to receive verification codes so that you can enter them into your tenant as a second form of authentication. If you do not have a phone, you will have to skip this lab. If this is the case, notify your instructor, who can potentially partner you with another student to follow along through this lab.

1. Switch to the **LON-CL1** VM, where you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of **Pa55w.rd**. 

2. In your **Edge** browser, you should still have **Outlook** open for Holly Dickson's account from the prior task when you sent an email to the MOD Administrator that contained an unsafe hyperlink. Open a new tab in **Edge** and navigate to the **Office 365 Security and Compliance center** by entering the following URL in the address bar: **https://protection.office.com**

3. In the **Ofice 365 Security and Compliance center**, verify the user icon in the upper right corner of the screen displays **HD** (for Holly Dickson) in the user icon circle. If a  different user appears, then sign out as that user, sign back in as Holly, and then navigate to the Security and Compliance center's URL from the prior step. 

4. In the **Ofice 365 Security and Compliance center**, select **Threat management** in the left-hand navigation pane and then select **Attack simulator**. 

5. On the **Attack Simulator** page, scroll down to see the four types of attacks that you can simulate. Also note the warning message that indicates you must enable multi-factor authentication (MFA) to schedule or terminate attacks. This is required because the system wants to confirm your credentials before you conduct a simulated attack. In the upcoming steps, you will enable MFA for Holly and then perform a phishing attack.

6. To enable MFA, you must first enable the security defaults that are built into Microsoft 365. Open a new browser tab and enter the following URL in the address bar: **https://portal.office.com**

7. On the **Office 365 home** page, select **Admin**. 

8. On the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Show all**, and then under the **Admin centers** section, select **Azure Active Dirctory*.

9. In the **Azure Active Directory admin center**, in the left-hand navigation pane, select **Azure Active Directory**.

10. In the **Adatum Corporation | Overview** page, scroll down through the middle navigation pane and select **Properties**.

11. In the **Properties** pane, scroll to the very bottom and select **Manage Security defaults**.

12. In the **Enable Security defaults** pane that appears on the right, the **Enable Security defaults** toggle switch is currently set to **No** (this was set to **No** by your lab hosting provider). Select this option to set it to **Yes**, and then select **Save**.

13. In your browser, select the **Microsoft 365 admin center** tab. 

14. In the **Microsoft 365 admin center**, in the left-hand navigation pane select **Settings**, and then in the **Settings** group, select **Settings**.

15. In the **Settings** page, the **Services** tab is displayed by default. In the list of services, select **Modern authentication**.

16. In the **Modern authentication** pane, read the information and then note that the **Enable Modern authentication** check box is already selected by default.   <br/>

	**Important:** To turn on MFA, you must first enable security defaults, and then you must enable modern authentication; BOTH settings must be enabled. If you purchased your Microsoft 365 subscription after October 21, 2019, both of these settings were enabled by default. However, for the purposes of the labs in this training course, your lab hosting provider turned off security defaults for your Microsoft 365 tenant. So even though this Modern authetication setting is turned On, MFA has not been enforced in your labs up until this point because security defaults were turned Off. <br/>

	In the previous step, you enabled the security defaults, and since this Modern authentication setting was enabled by default, MFA is now implemented. While you don't need to do anything in this Modern authentication pane, you were instructed to navigate here so that you know where this setting is for future use. <br/>

	Close the **Modern authentication** pane.

17. Close the browser session, and in the **Do you want to close all tabs?** dialog box, select **Close all**. 

18. Select the **Edge** icon on your taskbar to open a new browser session, and then open the **Office 365 Security and Compliance center** by entering the following URL in the address bar: **https://protection.office.com**

19. Since MFA is now enabled, a **More information required** window appears. <br/>

	**Note:** This dialog box is where you initiate entering your second form of authentication. However, note the following option that is available: **Skip for now (14 days until this is required)**. If you select this option to avoid entering a second form of authentication, the system will treat it as if MFA has been disabled. This means you will not be able to run the Attack Simulator.  <br/>

	So on this dialog box, select **Next**.

20. In the **Additional security verification** window, in Step 1 you must enter the information on how you want to be contacted. If you already have the **Microsoft Authenticator app** installed on your phone, you can use that; however, the simplest way is to simply authenticate using your phone. <br/>

	- Select the drop-down arrow in the first field and select whether to use Authentication phone or Mobile app. For the purposes of this lab, we recommend you select **Authentication phone** so that you do not have to take time installing the Microsoft Authenticator app that you may not use again after this training class. 
	- Select your country or region from the drop-down list.
	- In the field to the right of the country/region, enter your phone number.
	- In the **Method** field, there is only the text message option availble when you select **Authentication phone**. If you selected **Mobile app**, then additional options are displayed here. 
	
21. Select **Next**.

22. Once you receive the text message on your phone, enter the verification code that you received into the verification code field on the screen and then select **Verify**.

23. Select **Done** once the security verification is successful.

24. In the **Enter password** window that appears, enter **Pa55w.rd** and then select **Sign in**.

25. Another code will be texted to your phone. In the **Enter code** screen, enter the code that you received and select **Verify**.

26. In the **Stay signed in?** dialog box, select **Don't show this again** and select **Yes**.

27. The **Office 365 Security and Compliance center** should now be displayed in your browser. You will resume from here in the next task when you launch a spear phishing attack using the Attack Simulator. Leave this tab open in your browser. 

28. You have now configured MFA, you have signed into the **Security and Compliance center** using MFA, and you are ready to run the Attack Simulator. Leave everything as is in your VM and proceed to the next task.


### Task 2: Configure and launch a Spear Phishing attack
Now that Holly has turned on MFA, she is ready to run the Attack Simulator and launch a simulated spear phishing attack. This will provide visibility into how well Adatum is prepared to handle such a security attack. 

1. You should still be on **LON-CL1**, and you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of **Pa55w.rd**.

2. You should still have the **Office 365 Security and Compliance center** open in in your **Edge** browser from the prior task. If not, enter **https://protection.office.com** in the address bar, and then when you receive the dialog box asking for a second form of authentication, proceed through the verification process. 

3. In the **Ofice 365 Security and Compliance center**, select **Threat management** in the left-hand navigation pane and then select **Attack simulator**. 

4. On the **Attack Simulator** page, you reviewed the four types of simulated attacks that are available in the prior task. For this simulation, Holly has decided to conduct an account breach in which she will use a URL to try and obtain user names and passwords. This is referred to in the Attack Simulator as a **Spear Phishing (Credentials Harvest)** attack. <br/>

	You can launch this attack either from this page or the **Attack Details** page. Since the **Attack Details** page has additional information on what this attack will do, it is recommended that you launch it from there so that you can learn about the specifics of this type of attack. <br/>
	
	To the right of the **Spear Phishing (Credentials Harvest)** section, select **Attack Details**.

5. On the **Attack details** page, review the specific information related to the **Spear Phishing (Credentials Harvest)** attack type.

6. In the **Launch attack** section for the **Spear Phishing (Credentials Harvest)** attack type, select **Launch attack**.

7. In the **Configure Phishing Attack** page, the steps involved in the simulation are displayed in the left-hand pane. You will start by providing a name to the simulation for historical purposes. Enter **Spear Simulation** in the **Name** field and select **Next**.

6. In the next step, you will select the users that will receive the phishing email. You can select users from the company address book (the Active Users), or for large-scale attacks, you can import users from a .csv file. For this simple simulation, you will only send the email to one user, so select **Address Book**. <br/>

	Enter **Lynne** in the **Search for users or groups within your organization** field. In the list of users that appears, select **Lynne Robbins**. Lynne's user account record will display in the list of **Recipients**. Select **Next**. 

7. In the next step, you will configure the email that you want to send to the Lynne. <br/>

	- **From (Name)** and **From (Email)** fields - enter any values you want. 
	- **Phishing Login Server URL** - select any value from the drop-down menu.
	- **Custom Landing Page URL** - Ordinarily you would include a URL link for the target to click into; this would be entered in the Custom Landing Page URL field. Since this is just an exercise, you will not do that here. The success rate of the spear phishing attack will be a function of how clever an email you contrive. 

8. In the **Subject** field for the phishing email, enter**Free Gift Cards!!** and select **Next**.

9. In the **Please edit email body** page, compose the message in the **Email body** field. Enter a creative, enticing email message intended to lure users and then select **Next**.

10. On the **Confirmation** page, select **Finish**.


### Task 3: Confirm target received phishing email attack

2.  Open a new browser window in InPrivate or incognito mode and browse to **`https://office.com**.
 
3.  Log in as the user Lynne Robbins **LynnR@M365xZZZZZZ.onmicrosoft.com** where ZZZZZZ is your specific Office 365 tenant.

4.  Click the Outlook icon to open Microsoft Outlook for Lynne. You should see a spear phishing email that includes the details you just entered in the previous task.


### Task 4: Review the results

3. In your browser session where you are logged in as Holly Dickson go back to the Attack simulator.

4. In the Spear Phishing (Credentials Harvest) area click **View Report**.

5. The report lists the current results of the spear phishing campaign including number of users targeted and success rate.  
    
		**Note**: Since you can run multiple spear phishing simulation campaigns simultaneously you could create different emails for different users.

# Proceed to Exercise 2
