# Module 1 - Lab 1 - Exercise 2 - PIM Resource Workflows

As part of her Microsoft 365 pilot project, Holly Dickson, Adatum's Enterprise Administrator, wants to implement Privileged Identity Management within Azure Active Directory. One of Adatum's pain points in their existing system is that they have far too many users with administator privileges, and this has caused concern among management who sees this as a threat to their data security. They feel that too many people have been assigned admin roles that shouldn't have been, and as such, they have access to secure information and resources that they otherwise shouldn't have. There is a need for oversight for what those users are doing with their administrator privileges. By implementing PIM, Adatum can reduce the number of users with admin privileges and yet still be able to assign users with admin rights on an as-needed basis whenever necessary.

In this lab, you will perform the basic steps involved in implementing PIM for a given role - Configuring the role to require approval, assign an eligible user to the role, submit a request from the eligible user to be assigned the role, and approve the request for the role. In this exercise, you will perform these tasks for the Global Admin role, and Patti Fernandez will be the user in this scenario.


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


### Task 2: Assign an eligible user to the Global Admin role
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


### Task 3: Submit a request for the Global Admin role
Now that Patti Fernandez has been made an eligible user for the Global Admin role, Holly wants to test out the PIM process in her pilot project. In this task, Patti will submit a request to be assigned Global Admin role privileges. In the next task, Holly will review her request and approve it.

1.  Open an in Private Browsing session and login to https://portal.azure.com as Patti Fernandez.

1.  Open **Azure AD Privileged Identity Management**.

1.  Select **My Roles**.

     ![Screenshot](../Media/e84f0715-c71e-4b1c-87ed-4e5c0c38d501.png)

1.  **Activate** the Global Administrator Role.

     ![Screenshot](../Media/55eb14b5-540a-4d26-aed7-0b96d162fb31.png)

1.  Verify Patti's identity using the wizard.

1.  Return back to **My Roles** in **Azure AD Privileged Identity Management**.

1.  **Activate** the Global Administrator Role.

1.  Click **Activate**.

1.  Enter the justification **I need to carry out some administrative tasks** and click **Acitvate**.


### Task 3: Approve or deny requests for Azure resource roles in PIM


With Azure AD Privileged Identity Management (PIM), you can configure roles to require approval for activation, and choose one or multiple users or groups as delegated approvers. Follow the steps in this article to approve or deny requests for Azure resource roles.


###### View pending requests


As a delegated approver, you will receive an email notification when an Azure resource role request is pending your approval. You can view these pending requests in PIM.


1.  Switch back to the browser you are signed in with your Global Administrative account Holly Dickson.

1.  Open **Azure AD Privileged Identity Management**.

1.  Click **Approve requests**.

     ![Screenshot](../Media/fbc2f18d-f5a2-4139-b92d-7c19311aec1c.png)

1.  Select the request from Patti and click **Approve**.

1.  Enter a reason **Granted for this task** and click **Approve**.

1.  A notification appears with your approval.

1.  Switch back to the In Private Browsing session where Patti is signed in and click **My Roles** and then select **Active roles** note the status is now activated for Global Administrator.

     ![Screenshot](../Media/fe734263-57c8-4cc9-b79f-848d7d4f9488.png)


# continue to exercise 6
