# Module 11 - Lab 10 - Exercise 2 - Configure Azure AD for Intune 

In this exercise you will activate the automatic client enrollment to Intune for Mobile Device Management (MDM). This will allow you to manage mobile device access and set policies for restricting access to devices unless certain actions are adopted, such as strong passwords and screen timeouts.

### Task 1: Integrate Azure AD with Intune

1. You should still be logged into LON-CL1 as the **Admin** and in Microsoft 365 as **Holly Dickson**.
2. In your browser, select the **Microsoft 365 admin center** tab, which should still be open; if not, navigate to **https://admin.microsoft.com.** 
3. In the **Microsoft 365 admin center**, in the left-hand navigation pane, select **Show all** (if necessary), and then under **Admin centers**, select **Azure Active Directory**.
4. In the **Azure Active Directory admin center**, in the left-hand navigation pane, select **Azure Active Directory**.
5. On the **Adatum Corporation | Overview** window, in the middle pane under **Manage,** select **Mobility (MDM and MAM),** and then in the details pane on the right, select **Microsoft Intune**.<br/>

    **Note:** If you see a notification that automatic enrollment is available only for Azure AD Premium, press F5 to refresh the page in your web browser and then select **Microsoft Intune**.

6. On the **Configure** window, in the **MDM user scope** row, select **All**.<br/>

    **Note:** By setting this parameter to **All**, you are allowing all users who join their devices to Azure AD to automatically enroll them to Intune as well.

7. Below the list of MDM-related fields, select **Restore default MDM URLs** to ensure the correct URLs for client enrollment are configured.
8. In the menu bar at the top of the **Configure** window, select **Save**.
9. Leave the Azure portal open for the next task.

You have now configured your tenant so that all users can enroll their Windows 10 clients into Intune as soon they log into their devices with their Azure AD account credentials.


### Task 2: Configure Azure AD join

In this task, you will change the default settings for users to join their devices to Adatum's Azure AD tenant.

1. In the **Azure portal**, in the left-hand navigation pane, select **Azure Active Directory.**
2. In the **Adatum Corporation | Overview** window, in the middle section under **Manage**, select **Devices**.
3. In the **Devices | All devices** window, in the details pane on the right, verify that **LON-CL2** is displayed in the list of devices. Back in Lab 5, you performed a task that configured Mobile Device Management (MDM) auto-enrollment; this was a prerequisite to performing a later Windows Information Protection lab. When you performed this MDM configuration lab, it automatically enrolled the devices belonging to members of the WIP Users group. At the time, Joni Sherman was logged into Microsoft 365 on LON-CL2, and since she was a member of the WIP Users group, LON-CL2 was automatically enrolled into Intune as its MDM authority.
4. In the **Devices | All devices** window, in the middle pane under **Manage** , select **Device settings**.
5. In the details pane that appears on the right, in the **Users may join devices to Azure AD** row, verify that **All** is selected. This means that all Azure AD users can join their devices to Azure Active Directory.
6. The **Additional local administrator on Azure AD joined devices** row is currently set to **None**. Select **Selected**.
7. Below this field, in the **Selected** section (where it displays **No member selected),** hover your mouse over this section and note how it highlights the section. Select this section.
8. In the **Local administrators on devices** window, select **+Add**.
9. In the **Add members** pane on the right, select **Alex Wilber** , select the **Select** buton at the bottom of the screen, and then select **OK**.
10. Back in the **Devices | Device settings** detail pane, scroll down and verify that **Require Multi-Factor Auth to join devices** is set to **No**. The **Maximum number of devices per user** is currently set to **50.** Select this field and in the menu that appears, select **10.**
11. Scroll back to the top of the page, and in the menu bar, select **Save**.
12. Leave the Azure portal open for the next task.

You have changed the default settings for users to join their devices to your Azure AD tenant.


### Task 3: Create dynamic Azure AD device group
In Azure Active Directory, you can use rules to determine group membership based on user or device properties. Dynamic membership is supported for security groups or Office 365 groups. When a group membership rule is applied, user and device attributes are evaluated for matches with the membership rule. When an attribute changes for a user or device, all dynamic group rules in the organization are processed for membership changes. Users and devices are added or removed if they meet the conditions for a group. Devices can only be used in Security groups.

In this task, Holly wants to create a new Security group for enrolled devices within Adatum. This group will support dynamic membership when a device's management type is set to MDM.

1. In the **Azure portal**, in the left-hand navigation pane, select **Azure Active Directory.**
2. In the **Adatum Corporation | Overview** window, in the middle pane under **Manage,** select **Groups**.
3. In the **Groups | All groups** window, in the details pane on the right, select **+New group** on the menu bar.
4. In the **New Group** window, enter the following information:

    - Group type: **Security**
    - Group name: **Enrolled Devices**
    - Membership type: **Dynamic Device**
    - Owner: select **no owners selected**, then in the **Add Owners** window, select **Alex Wilber** and select **Select**
    
5. At the bottom of the **New Group** window, under **Dynamic device members**, select **Add dynamic query**.
6. In the **Dynamic membership rules** window, configure the following fields for this expression:

    - Property: select the drop-down arrow and select **managementType**
    - Operator: select the drop-down arrow and select **Equals**  
    - Value: enter **MDM**

7. Select **+Add expression**. It should display the following in the **Rule syntax** field:<br/>

    **(device.managementType -eq  &quot;MDM&quot;)**

8. Select **Save** in the menu bar at the top of the window.
9. In the **New Group** window, scroll to the bottom of the window and select the **Create** button.
10. In the **Groups | All groups** window, the **Enrolled Devices** group should now appear in the list of groups.
11. Leave the **Azure Active Directory admin center** tab open in your browser for the next task.


# Proceed to Lab 10 -Exercise 3
