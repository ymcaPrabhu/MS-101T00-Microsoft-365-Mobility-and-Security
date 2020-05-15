# Module 11 - Lab 10 - Exercise 5 - Manage and Monitor a Device in Intune

Holly Dickson wants to make managing devices easier, so she has decided to implement Microsoft Intune device categories in her pilot project. Implementing device categories will enable her to automatically add devices to groups based on categories that she defines.

As part of managing devices in Intune, Holly will create dynamic groups in the Azure portal, based on the device category and device category name. After you configure device groups, users who enroll their device will be presented with a list of the categories you configured. After they choose a category and finish enrollment, their device is added to the Active Directory security group that corresponds with the category they chose.

### Task 1: Create device categories
In this task, you're going to create device categories, which will then be assigned to devices in the next task.

1. In the LON-CL1 VM, you should still be logged in as the **Admin** account, and you should still be logged into Microsoft 365 as **Holly Dickson**.
2. In your **Edge** browser, you should have the **Microsoft Azure portal** open and displaying the **Devices | All devices** window. At the top of the screen is the following navigation thread: **All services > Microsoft Intune > Devices | All devices**. <br/>

   In this thread, select **Microsoft Intune**.
3. In the **Microsoft Intune | Overview** page, in the left-hand pane under **Manage,** select **Device enrollment**.
4. In the **Device enrollment** window, in the left-hand pane under **Manage**, select **Device categories.**
5. In the **Device enrollment | Device categories** window, select **+Create device category**.
6. On the **Create device category** window, the top of the page shows the 3 steps involved in creating a device category. In **Step 1 - Basics**, enter **Mobile Device** and then select **Next**.
7. On the **Step 2 - Scope tags** window, you will not define scope tags, so select **Next**. 
8. On the **Step 3 - Review + create** window, select **Create**.
9. Repeat steps 5-8 to create a second device category, this one titled **Desktops**.
10. Leave all browser tabs open for the next task.

### Task 2: Manage the enrolled devices
In this task, you're going to manage the Category property of the two devices that are joined to Azure AD and enrolled in Microsoft Intune. You will also review the properties and discovered apps on each device.

1. In the **Azure portal**, in the navigation thread at the top of the screen (**Home > Microsoft Intune > Device enrollment > Device Categories**), select **Microsoft Intune**.
2. In the **Microsoft Intune | Overview** page, in the left-hand pane under **Manage,** select **Devices**.
3. On the **Devices** window, in the left-hand pane under **Manage**, select **All devices**.
4. On the **Devices | All devices** window, select **LON-CL1**, which is the device that Holly joined to Azure AD, and which was automatically enrolled to Intune.
5. On the **LON-CL1** window, review the device details. Also review the actions available on the menu bar at the top of the page; these are the actions that you can perform against the device.
6. On the **LON-CL1** window, in the left-hand pane under the **Manage** section, select **Properties**. 
7. In the **LON-CL1 | Properties** window, note the current value of the **Device category** field is **Unassigned**. Select the drop-down arrow for this field and in the menu, select **Desktops**, and then on the menu bar at the top of the page, select **Save**.<br/>

    **Note:** For Android or iOS devices, you must select the **Device category** during enrollment.
8. In the **LON-CL1 | Properties** window, in the left-hand pane under the **Monitor** section, select **Hardware.**
9. In the **LON-CL1 | Hardware** window, review the hardware information that synced from the device. Also scroll down review the **Conditional access** section at the bottom of the page.
10. In the left-hand pane under the **Monitor** section, select **Discovered apps** and review the list of apps that were discovered on the device.
11. In the **Lon-CL1 | Discovered apps** window, select **Devices | All devices** in the navigation thread at the top of the page.
12. Repeat steps 4-10, but this time select **LON-CL2**, which is the device that Joni Sherman joined to Azure AD in an earlier lab. Change the **Device category** value to **Mobile Device**.
13. Leave all browser tabs open for the next task.


### Task 3: Create dynamic groups for the device categories

1. In the **Azure portal**, in the navigation thread at the top of the screen (**Home > Microsoft Intune > Devices | all devices > LON-CL2 | Discovered apps**), select **Microsoft Intune**.
2. In the **Microsoft Intune | Overview** page, in the left-hand pane under the **Manage** section, select **Groups**.
3. In the **Groups | All groups** window, select **+New group** on the menu bar.
4. In the **New Group** window, enter the following information:

    - Group type: **Security**
    - Group name: **Mobile Devices**
    - Membership type: **Dynamic Device**

5. Under the **Dynamic device members** section, select **Add dynamic query**.
6. On the **Dynamic membership rules** window, hover your mouse over the row to display the rule fields, and then enter the following values:

    - Property:   **deviceCategory**
    - Operator: **Equals**
    - Value: enter **Mobile Device**

7. Select in the **Rule syntax** field and the query syntax will appear.
8. Select **Save** on the menu bar at the top of the page.
9. On the **New Group** window, select **Create.** The **Mobile Device** group should now appear in the list of groups.
10. Repeat steps 3-9 to create a group for desktop devices. The **Group Name** should be set to **Desktop Devices**, and in the **Dynamic membership rules** window, enter **Desktop Devices** in the **Value** field.
11. Leave all browser tabs open for the next task.


### Task 4: Create a conditional access policy
The modern security perimeter now extends beyond an organization's network to include user and device identity. Organizations can utilize these identity signals as part of their access control decisions.

Conditional Access is the tool used by Azure Active Directory to bring signals together, to make decisions, and enforce organizational policies. Conditional Access is at the heart of the new identity-driven control plane.

In this task, you will create a conditional access policy that Holly plans to implement in her pilot project. 

1. In the **Azure portal**, in the navigation thread at the top of the screen (**Home > Microsoft Intune > Groups | All groups**), select **Microsoft Intune**.
2. In the **Microsoft Intune | Overview** page, in the left-hand pane under the **Manage** section, select **Conditional access**.
3. In the **Conditional Access | Policies** window, select **+New policy** on the menu bar.
4. On the **New** pane, in the **Name** text box, enter **Conditional1** and then select the **Users and groups** section.
5. On the **Users and groups** pane, select the **All users** option and then select **Done**.
6. On the **New** pane, select the **Cloud apps or actions** section.
7. On the **Cloud apps or actions** pane, select the **Select apps** option and then select the **Select** section.
8. In the **Select** pane, select the check box for **Office 365 Exchange Online**, select the **Select** button at the bottom of the page, and then select **Done**.
9. On the **New** pane, select the **Conditions** section.
10. On the **Conditions** pane, select the **Device platforms** section.
11. On the **Device platforms** pane, in the **Configure** field, select **Yes**. In the **Include** tab, select the **Select device platforms** option, select the **Windows** check box, and then select **Done.**
12. On the **Conditions** pane, select **Done**.
13. On the **New** pane, under **Access Controls**, select the **Grant** section.
14.  On the **Grant** pane, select the **Require device to be marked as compliant** check box, and then select the **Select** button.
15. On the **New** pane, under **Access Controls**, select the **Session** section.
16. In the **Session** pane, review the explanation but do not select any option. Select the **X** in upper right corner to close the pane.
17. On the **New** pane, select the **Create** button at the bottom of pane. The **Conditional1** policy now appears in the policy list.<br/>

    **Note:** You created a conditional access policy to become familiar with the available options; however, the policy is not effective because you didn't enable it.
18. To enable the policy, select the **Conditional1** policy in the policy list.  
19. In the **Conditional1** pane, scroll to the bottom, and in the **Enable policy** field, select **On**. Select **Save**.

You have now created a conditional access policy and enabled it for Adatum's pilot project.


# End of Lab 10
