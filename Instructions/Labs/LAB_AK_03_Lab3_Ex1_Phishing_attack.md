# Module 3 - Lab 3 - Exercise 1 - Conduct a Spear Phishing attack using the Attack Simulator

Holly Dickson is concerned that some users at Adatum may require education about phishing attacks. As part of her pilot project, Holly has decided to use the Microsoft 365 Attack Simulator to determine her users' susceptibility to phishing attacks.


### Task 1: Enable Mulit-factor authentication for the Global Admin
To use Microsoft's Attack Simulator to simulate a phishing attack, you must first enable Multi-Factor Authentication (MFA) for your organization. For her pilot project, Holly does not want to set up MFA for the Adatum users at this point in time; however, to use the Attack Simulator, she must enable MFA. So in this task, she will enable MFA for Adatum, and then after she finishes running the Attack Simulator, she will turn off MFA. To set up or modify MFA, you must be a Global Admin, so Holly has entrusted this task to herself. 

Enabling MFA is a twpo-step process: 1) you must first enable security defaults for your organization (these are turned Off by default), and then you must enable Modern Authentication (this is actually turned on by default, so you really don't need to perform this stepp; however, you will verify this setting in this lab to familiarize yourself with the process).

1. Switch to the **LON-CL1** VM, where you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of Pa55w.rd. 

2. In your **Edge** browser, you should still have **Outlook** open for Holly Dickson's account from the prior task when you sent an email to the MOD Administrator that contained an unsafe hyperlink. Open a new tab in **Edge** and navigate to the **Office 365 Security and Compliance center** by entering the following URL in the address bar: **https://protection.office.com**

3. In the **Ofice 365 Security and Compliance center**, verify the user icon in the upper right corner of the screen displays **HD** (for Holly Dickson) in the user icon circle. If a  different user appears, then sign out as that user, sign back in as Holly, and then navigate to the Security and Compliance center's URL from the prior step. 

4. In the **Ofice 365 Security and Compliance center**, select **Threat management** in the left-hand navigation pane and then select **Attack simulator**. 

5. On the **Attack Simulator** page, scroll down to see the four types of attacks that you can simulate. Also note the warning message that indicates you must enable multi-factor authentication (MFA) to schedule or terminate attacks. This is required because the system wants to confirm your credentials before you conduct a simulated attack. In the upcoming steps, you will enable MFA for Holly and then perform a phishing attack.
5. To enable MFA, you must first enable security defaults that are built into Microsoft 365. Open a new browser tab and enter the following URL in the address bar: **https://portal.office.com**

6. On the **Office 365 home** page, select **Admin**. 

7. On the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Show all**, and then under the **Admin centers** section, select **Azure Active Dirctory*.

8. In the **Azure Active Directory admin center**, in the left-hand navigation pane, select **Azure Active Directory**.

9. In the **Adatum Corporation | Overview** page, scroll down through the middle navigation pane and select **Properties**.

10. In the **Properties** pane, scroll to the very bottom and select **Manage Security defaults**.

11. In the **Enable Security defaults** pane that appears on the right, the **Enable Security defaults** toggle switch is currently set to **No**. Select this option to set it to **Yes**, and then select **Save**.

12. In your browser, select the **Microsoft 365 admin center** tab. 

13. In the **Microsoft 365 admin center**, in the left-hand navigation pane select **Settings**, and then in the **Settings** group, select **Settings**.

14. In the **Settings** page, the **Services** tab is displayed by default. In the list of services, select **Modern authentication**.

15. In the **Modern authentication** pane, read the information and then note that the **Enable Modern authentication** check box is already selected by default. This means MFA was turned on by default for the entire organization.  <br/>

	**Important:** To turn on MFA, you must first enable security defaults, and then you must enable modern authentication. If you purchased your Microsoft 365 subscription after October 21, 2019, both of these settings were enabled by default. However, your lab hosting provider turned off security defaults for your Microsoft 365 tenant. So even though this Modern authetication setting was turned On, MFA was not enforced since the security defaults setting was turned Off. In the previous step, you enabled the security defaults, and since this Modern authentication setting was enabled by default, MFA is now implemented. While you don't need to do anything in this Modern authentication pane, you were instructed to navigate here so that you know where this setting is for future use. <br/>

	Close the **Modern authentication** pane.

16. Close the browser session, and in the **Do you want to close all tabs?** dialog box, select **Close all**. 

17. Select the **Edge** icon on your taskbar to open a new browser session, and then open the **Office 365 Security and Compliance center** by entering the following URL in the address bar: **https://protection.office.com**

18. Since MFA is now enabled, a **More information required** window appears. However, note the following option that is available: **Skip for now (14 days until this is required)**. So even though MFA is turned on (which is a requirement for running the Attack Simulator), you will skip actually entering a second form of authentication for the purpose of this lab. <br/>

	Select **Skip for now (14 days until this is required)** (note: if this dialog box appears again, select this option one more time).

19. You have now configured MFA and are ready to run the Attack Simulator to launch a spear phishing attack in the next task. Leave everything open in your browser. 

### Task 2: Configure and launch a Spear Phishing attack
3.  In the Spear Phishing (Credentials Harvest) area select the **Launch Attack** button.

4.  Name the campaign Spear Simulation and select **Next**.

5.  In the Target recipients area select the **Address Book** button and select **Lynne Robbins** and then then select  **Next**.

6.  In the Configure email details area enter a creative **From (Name), From (Email)**, and select any Phishing Login Server URL from the drop-down menu.

      **Note**: Ordinarily you would also include a URL link for the target to click into.  This would be entered in the Custom Landing Page URL field.  Since this is just an exercise we won't do that here.  The success rate of the spear phishing attack will be a function of how clever an email you contrive. 

7.  In the **Subject** field for the phishing email type Free Gift Cards and select **Next**.

8.  In the Compose email area enter a creative enticing email message intended to lure users and select **Next**.

9.  In the Confirm area select **Finish**.


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
