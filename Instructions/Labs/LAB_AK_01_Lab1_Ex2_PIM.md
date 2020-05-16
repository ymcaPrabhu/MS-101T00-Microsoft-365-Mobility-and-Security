# Module 1 - Lab 1 - Exercise 2 - PIM Resource Workflows

As part of her Microsoft 365 pilot project, Holly Dickson, Adatum's Enterprise Administrator, wants to implement Privileged Identity Management within Azure Active Directory. One of Adatum's pain points in their existing system is they have far too many users with permanent administator roles. This has caused concern among management, who sees this as a threat to Adatum's data security. They feel that too many people were assigned admin roles that shouldn't have been, and as such, they have access to secure information and resources that could potentially compromise the organization. 

Because there is a need to reduce the number of users with permanent administrator roles and yet still provide admin privileges to selected users when business justification warrants it, Holly has been tasked with implementing Azure Active Directory's Privileged Identity Management service. By implementing PIM, Adatum can reduce the number of users with admin roles and yet still be able to assign users with admin rights on an as-needed basis whenever necessary.

In this lab, you will perform the basic steps involved in implementing PIM for a given admin role:

- Configuring the role to require approval
- Assign an eligible user to the role
- Submit a request from the eligible user to be assigned the role
- Approve the request for the role

In this exercise, you will perform these tasks for the Global Administrator role. Holly will take on the role of the approver, and Patti Fernandez will be the user requesting access to the role.

**Note:** In Task 3, Patti Fernandez will submit a request to be assigned the Global Admin role. The activation request process is set up to require Multi-Factor Authentication (MFA). If you do not have a phone to complete this process, notify your instructor. You can still complete Tasks 1 and 2, and you may be able to partner up with another student to watch them complete the remaining tasks.


### Task 1 - Configure the Global Administrator role to require approval
Since the Microsoft 365 Global Administrator role provides a user with basically unlimited access to all Microsoft 365 resources, the number of users assigned to this role should obviously be kept to a bare minimum for security purposes. 

Holly Dickson, Adatum's Enterprise Administrator, wants to limit access to this role using Privileged Identity Management. To do so, she must first configure the role to require approval before it can be assigned as an eligible role for a user, and then she wants to assign herself as the approver whenever an eligible user requests activating the role.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as Holly Dickson.

2. In the **Microsoft 365 admin center**, in the left-hand navigation pane under the **Admin centers** section, select **Azure Active Directory**

3. In the **Azure Active Directory admin center**, in the left-hand navigation pane, select **All services**.

4. In the **All services** window, under the **Identity** section, select **Azure AD Privileged Identity Management**.

5. In the **Privileged Identity Management | Quick start** window, in the middle pane under the **Manage** section, select **Azure AD roles**.

6. In the **Adatum Corporation | Quick start** window, in the middle pane under the **Manage** section, select **Settings**. 

7. In the **Adatum Corporation | Settings** window, select the **Global Administrator** role.

8. In the **Role setting details -  Global Administrator** window, select **Edit** on the menu bar at the top of the page.

9. In the **Edit role setting - Global Administrator** window, select the **Require Approval to activate** check box. 

10. In the **Select approver(s)** section, no specific approver has been selected. Holly wants to assign herself as the approver for this role, so select this section. In the **Select a member** pane that opens on the right, scroll down through the list of users and select **Holly Dickson**, and then select the **Select** button.

11. In the **Edit role setting - Global Administrator** window, select **Update**.

12. Leave all browser tabs open for the next task.


### Task 2 - Assign an eligible user to the Global Admin role
For Adatum's PIM pilot project, Holly has selected Patti Fernandez as the sole user who will be eligible to be assigned the Global admin role. In this task, Holly will enable Patti to be eligible for the Global admin role.

1. You should still be logged into LON-CL1 as the **Admin** account, and you should be logged into Microsoft 365 as Holly Dickson.

2. In your **Edge** browser, you should still have the **Azure Active Directory admin center** open in a tab that's displaying the **Adatum Corporation | Settings** window. In the navigation thread at the top of the page (**All services > Privileged Identity Management > Quick start**), select **Privileged Identity Management**.

3. In the **Privileged Identity Management | Quick start** window, in the middle pane under **Manage**, select **Azure AD roles**.

4. In the **Adatum Corporation | Quick start** window, in the **Privileged Identity Management** pane, under the **Assign** group, select **Assign Eligibility**.

5. In the **Adatum Corporation | Roles** window, scroll down through the list of roles and select **Global Administrator**.

6. In the **Global Administrator | Assignments** window, select **+Add assignments** on the menu bar. 

7. In the **Add assignments** window, the **Membership** tab is displayed by default. Under the **Select member(s)**, select **No member selected**.

8. In the **Select a member** pane that appears on the right, scroll down through the list of users and select **Patti Fernandez**, and then select the **Select** button.

9. In the **Add assignments** window, select **Next** (this does the same thing as selecting the **Settings** tab). 

10. In the **Add assignments** window, under the **Settings** tab, verify the **Assignment type** option is set to **Eligible**, and then select **Assign**. 

11. In the **Global Administrator | Assignments** window, note that Patti Fernandez is now an eligible user who can be assigned the Global Admin role.

12. Leave all browser tabs open for the next task.


### Task 3 - Submit a request for the Global Admin role
Now that Patti Fernandez has been made an eligible user for the Global Admin role, Holly wants to test out the PIM process in her pilot project. In this task, Patti will submit a request to be assigned Global Admin role privileges. In the next task, Holly will review her request and approve it.

**Note:** The activation request process is set up to require Multi-Factor Authentication (MFA). If you do not have a phone to complete this process, notify your instructor. You may be able to partner up with another student to watch them complete the remaining two tasks.

1.  In LON-CL1, right-click on the **Edge** icon on ther taskbar and in the menu that appears, select **New InPrivate window*. 

2. In your InPrivate browser session, enter the following URL in the address bar: **https://portal.azure.com**

3. In the **Sign in** window, enter **PattiF@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is the tenant suffix ID provided by your lab hosting provider) and then select **Next**. In the **Enter password** window, enter **Pa55w.rd** and then select **Sign in**.

4. In the **Welcome to Microsoft Azure** dialog box that appears, select **Maybe later**.

5. In the **Microsoft Azure** portal, scroll down to the **Azure services** section, and then on the right side of the section, select **More services**.

6. In the **All services** window, enter **priv** in the **Search** box at the top of the page. In the list of search results, select **Azure AD Privileged Identity Management**.

7. In the **Privileged Identity Management | Quick start** window, in the navigation pane, select **My Roles**.

8. In the **My roles | Azure AD roles** window, the **Eligible roles** tab is displayed by default. Since Holly assigned Patti as an eligible user for the Global Administator role, this role appears in the list. Under the **Action** column, select **Activate**.

9. In the **Activate** pane, a warning message is displayed at the top of the pane indicating additional verification is required. Select this message.

10. In the **More information required** window that appears, select **Next**. 

11. In the **Additional security verification** window that appears, under **How should we contact you?**, leave the value set to **Authentication phone**. Select your country or region, and then in the field next to it, enter your phone number (xxx-xxx-xxxx). Select **Next**.

12.In the **Additional security verification** window, under **We've sent a text message to your phone**, retrieve the verification code from the text sent to your phone and enter it here, then select **Verify**.

13. Once verification is complete, select **Done**.

14. In the **Activate - Global Administrator** pane that appears, enter **Testing PIM** in the **Reason** field, and then select the **Activate** button at the bottom of the pane.

15. On the **My roles | Azure AD roles** window, select the **Active roles** tab on the menu bar. Note that no roles appear. <br/>

     **Note:** If you recall, back in Task 1 Holly set up the Global Admin role so that activation to a user account will require approval. What Patti just did was request that the Global Admin role be activated for her user account. This will send a request to Holly, who can then either approve or deny Patti's request for role activation. Holly will review this request in the next task.

16. Leave the InPrivate browser session open. You will return to it in the next task once Holly approves Patti's request.


### Task 4 -  Approve the request for the Global Admin role

Back in Task 1, Holly set herself up as the approver for the Global Administrator role. Since Patti has submitted a request to be assigned this role, Holly must review the request and determine whether to accept or deny it. 

1.  In LON-CL1, switch back to the original browser session in which you are signed into **Microsoft 365** as **Holly Dickson**.

2.  In your browser, select the **Azure Active Directory admin center** tab, which should be displaying the **Global Administrator | Assignments** window. In the navigation thread at the top of the page (**All services > Privileged Identity Management > Adatum Corporation | Roles > Global Administrator | Assignments**, select **Privileged Identity Management**.

3. In the **Privileged Identity Management | Quick start** window, in the middle pane under **Tasks**, select **Approve requests**.

4. In the **Approve requests | Azure AD roles** window, in the **Requests for role activations** section, select the request from Patti Fernandez. In the pane that appears on the right that displays the details of Patti's request, select **Approve**.

5.  Enter a reason **Granted for this task** and click **Approve**.

6.  Switch back to the InPrivate browser session where Patti is signed in. In the **My roles |Azure AD roles** window that should still be displayed, the **Eligible roles** tab is currently being displayed. On the menu bar, select the **Active roles** tab. Note how the Global Administrator role is now activated for Patti. 

7. Close the InPrivate browser session.

8. In your Edge browser session, close the **Azure Active Directory** tab. 

9. In your Edge browser, leave the **Microsoft Office Home** tab and the **Microsoft 365 admin center** tab open for the next task.


# End of Lab 1
