# Module 3 - Lab 3 - Exercise 1 - Conduct a Spear Phishing attack using the Attack Simulator

Holly Dickson is concerned that some users at Adatum may require education about phishing attacks. As part of her pilot project, Holly has decided to use the Microsoft 365 Attack Simulator to determine her users' susceptibility to phishing attacks.


### Task 1: Enable Multi-factor Authentication for the Global Admin
To use Microsoft's Attack Simulator to simulate a phishing attack, you must first enable Multi-Factor Authentication (MFA) for either your entire organization or for just the Global admin who will run the simulator. For her pilot project, Holly does not want to set up MFA for all the Adatum users at this point in time; therefore, she will enable MFA for her user account only, and then after she finishes running the Attack Simulator, she will turn MFA back off. 

**Important:** To implement MFA, you will need to use your mobile phone to receive a verification code so that you can enter it into your tenant as a second form of authentication. If you do not have a phone, you will have to skip this lab. If this is the case, notify your instructor, who can potentially partner you with another student to follow along through this lab.

1. Switch to the **LON-CL1** VM, where you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of **Pa55w.rd**. 

2. In your **Edge** browser, you should still have **Outlook** open for Holly Dickson's account from the prior task when you sent an email to the MOD Administrator that contained an unsafe hyperlink. Open a new tab in **Edge** and navigate to the **Office 365 Security and Compliance center** by entering the following URL in the address bar: **https://protection.office.com**

3. In the **Office 365 Security and Compliance center**, verify the user icon in the upper right corner of the screen displays **HD** (for Holly Dickson) in the user icon circle. If a  different user appears, then sign out as that user, sign back in as Holly, and then navigate to the Security and Compliance center's URL from the prior step. 

4. In the **Office 365 Security and Compliance center**, select **Threat management** in the left-hand navigation pane and then select **Attack simulator**. 

5. On the **Attack Simulator** page, scroll down to see the four types of attacks that you can simulate. Also note the warning message that indicates you must enable multi-factor authentication (MFA) to schedule or terminate attacks. This is required because the system wants to confirm your credentials before you conduct a simulated attack. In the upcoming steps, you will enable MFA for Holly and then perform a phishing attack.

6. To enable MFA for Holly Dickson's user account, you must first access the **Active users** list in the **Microsoft 365 admin center**. Open a new browser tab and enter the following URL in the address bar: **https://portal.office.com**

7. On the **Office 365 home** page, select **Admin**. 

8. On the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Users** and then select **Active users**.

9. In the **Active users** window, on the menu bar at the top of the user list, select **Multi-factor authentication**.

10. In the **multi-factor authentication** window, the **users** tab is displayed by default. Note the MFA status for all existing user accounts, which is **Disabled**. Select the check box for **Holly Dickson**, and in Holly's properties pane on the right, select **Enable**.

11. On the **About enabling multi-factor auth** dialog box, select **enable multi-factor auth**. 

12. When the **Updates successful** dialog box appears, select **close**. In the **multi-factor authentication** window, verify Holly's MFA Status has changed to Enabled. 

13. You now need to sign out of Microsoft 365 as Holly, close your browser session (to clear cache), open a new session, and then log back in as Holly using MFA. The first time you sign back in after having MFA enabled for your user account, you will be asked for the authentication information needed for MFA, such as your phone number and authentication options. You will then be texted a verification code to validate the authentication process works. You will perform these steps in the remaining portion of this task.<r/>

	You will begin by signing out as Holly, so select the **HD** user icon in the upper right corner of the browser and in the **My account** pane, select **Sign out**. 

14. Once you are signed out, close the browser session and all the browser tabs.

15. Select the **Edge** icon on your taskbar to open a new browser session, and then open the **Office 365 Security and Compliance center** by entering the following URL in the address bar: **https://protection.office.com**

16. In the **Pick an Account** window, select **Holly@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix provided by your lab hosting provider). In the **Enter password** window, enter **Pa55w.rd** and select **Sign in**.

17. Because MFA is enabled for Holly, a **More information required** window appears. Select **Next**.

18. Setting up the additional information required by MFA is a 3-step process. In Step 1, in the **Additional security verification** window, enter the information on how you want to be contacted. <br/>

	- Select the drop-down arrow in the first field and select whether to use Authentication phone or Mobile app. For the purposes of this lab, we recommend you select **Authentication phone** so that you do not have to take time installing the Microsoft Authenticator app that you may not use again after this training class. 
	- Select your country or region from the drop-down list.
	- In the field to the right of the country/region, enter your phone number (**xxx-xxx-xxxx**).
	- In the **Method** field, only the text message option is available when you select **Authentication phone**. If you selected **Mobile app**, then additional options are displayed here. Leave this option selected.
	- Select **Next**.

19. In Step 2, you will receive a text message with a verification code to test whether the phone number you entered is correct. Once you receive the text message on your phone, enter the code into the verification code field on the screen and then select **Verify**.

20. In Step 3, select **Done**.

21. If you take too long to complete this process, the **Enter password** window will appear with a message indicating you took too long to complete the sign in process, so you will be timed-out. If this occurs, you must sign in again with Holly's password of **Pa55w.rd**. Another verification code will be texted to your phone, so enter it in the **Enter code** screen that appears and select **Verify**.

22. The **Office 365 Security and Compliance center** should now be displayed in your browser. You will resume from here in the next task when you launch a spear phishing attack using the Attack Simulator. Leave this tab open in your browser. 

23. You have now configured MFA, you have signed into the **Security and Compliance center** using MFA, and you are ready to run the Attack Simulator. Leave everything as is in your VM and proceed to the next task.


### Task 2: Configure and launch a Spear Phishing attack
Now that Holly has turned on MFA, she is ready to run the Attack Simulator and launch a simulated spear phishing attack. This will provide visibility into how well Adatum is prepared to handle such a security attack. 

1. You should still be on **LON-CL1**, and you should still be logged in as the **Admin** account. If necessary, log in as the **Admin** with a password of **Pa55w.rd**.

2. You should still have the **Office 365 Security and Compliance center** open in in your **Edge** browser from the prior task. If not, enter **https://protection.office.com** in the address bar, and then when you receive the dialog box asking for a second form of authentication, proceed through the verification process. 

3. In the **Office 365 Security and Compliance center**, select **Threat management** in the left-hand navigation pane and then select **Attack simulator**. 

4. On the **Attack Simulator** page, you reviewed the four types of simulated attacks that are available in the prior task. For this simulation, Holly has decided to conduct an account breach in which she will use a URL to try and obtain user names and passwords. This is referred to in the Attack Simulator as a **Spear Phishing (Credentials Harvest)** attack. <br/>

	You can launch this attack either from this page or the **Attack Details** page. Since the **Attack Details** page has additional information on what this attack will do, it is recommended that you launch it from there so that you can learn about the specifics of this type of attack. <br/>
	
	To the right of the **Spear Phishing (Credentials Harvest)** section, select **Attack Details**.

5. On the **Attack details** page, review the specific information related to the **Spear Phishing (Credentials Harvest)** attack type.

6. In the **Launch attack** section for the **Spear Phishing (Credentials Harvest)** attack type, select **Launch attack**.

7. In the **Configure Phishing Attack** page, the steps involved in the simulation are displayed in the left-hand pane. While you can manually create a phishing campaign, it is recommended that you take advantage of the available templates that will prefill most of the information for you. The key to a successful phishing attack is to create a very intriguing, real-world looking email, and the templates provide very creative solutions. <br/>

	On the **Provide a name to the campaign** page, select the **Use Template** button. 

8. Select the **Please select a template in the list** field that appears, and in the drop-down menu, select the template of your choice. Select **Next**.

9. In the next step, you will select the users that will receive the phishing email. You can select users from the company address book (the Active Users), or for large-scale attacks, you can import users from a .csv file. For this simple simulation, you will only send the email to one user, so select **Address Book**. <br/>

	Enter **Lynne** in the **Search for users or groups within your organization** field. In the list of users that appears, select **Lynne Robbins**. Lynne's user account record will display in the list of **Recipients**. Select **Next**. 

10. In the next step, you will configure the email details. Because you chose to use a template, all the fields are prefilled for you. Between this step and the next one, the template provides a very professional touch to make the email appear legitimate. Select **Next**.

11. In the final configuration step, you will configure the email details. Because you chose to use a template, the **Email body** is prefilled for you. Scroll down to see the full body of the text. Select **Next**

12. On the **Confirmation** page, select **Finish**. This will launch the phishing attack!

13. Once the attack is complete, you will be returned to the **Attack simulator** page. 

14. Leave your browser and the Security and Compliance Center open for the next task.


### Task 3: Review the attack simulation results

In this task, you will verify whether Lynne Robbins received the email that you configured in the Attack Simulator, and then you will review the report associated with the Spear Phishing attack that you simulated.

1. Switch to the **LON-CL2** VM and log in as the **Admin** with a password of **Pa55w.rd**.

2. Select the Edge browser icon on taskbar, maximize the window, and then enter the following URL in the address bar: **https://outlook.office.com**.
 
3. In the **Sign in** window, enter **LynnR@xxxxxZZZZZZ.onmicrosoft.com** (where xxxxxZZZZZZ is the tenant prefix ID provided by your lab hosting provider), and then in the **Enter password** window, enter **Pa55w.rd** and select **Sign in**. Select **Yes** on the **Stay signed in?** window.

4. Close the **Welcome** window.

5. In Lynne's Outlook Inbox, you should see the spear phishing email that was sent by the Attack Simulator. Select the email to open it and review the details in the body of the message. 

6. Select the link that is included in the email. Even though you know this is a spear phishing attack, this will enable you to see the effect of doing so in the Attack Simulator report that tracks the results of the spear phishing campaign.

7. Switch back to LON-CL1.

8. In your browser session where you are logged in as Holly Dickson, you should still be on the **Attack simulator** page. In the **Spear Phishing (Credential Harvest)** section, it should display **Attack Completed**. Select **View Report**.

9. On the **Attack details** page, view the report for the phishing campaign that you completed. Note the date and time of the report. If you had run a previous simulation, it sometimes takes a few minutes to update this report information with the details from the current simulation that you just ran. If this occurs, refresh the page after a few minutes. Review the information on the page and note the results after having clicked on the spear phishing URL in the email that was sent to Lynne Robbins earlier in this task.

10. Leave your browser open in LON-CL1 and do not close any of the tabs.
    

# Proceed to Lab 3 - Exercise 2
