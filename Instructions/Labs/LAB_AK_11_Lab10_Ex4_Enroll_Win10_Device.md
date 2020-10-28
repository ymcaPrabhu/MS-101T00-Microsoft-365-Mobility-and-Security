# Module 11 - Lab 10 - Exercise 4 - Enroll a Windows 10 Device

One of Adatum’s goals for their Microsoft 365 deployment is to enroll their Windows 10 devices to Azure AD and Intune so that the devices can be managed by MDM. As part of her pilot project, Holly Dickson wants to enroll the LON-CL1 PC to Intune. In this exercise, you will first verify that the device is not currently enrolled, and having done that, you will enroll the device to Azure AD and Intune and then verify the enrollment. 

During her pilot project, Holly plans to use certificates with Intune to authenticate Adatum’s users to applications and corporate resources through VPN, Wi-Fi, and email profiles. By using certificates to authenticate these connections, Adatum’s end-users won't need to enter usernames and passwords, which helps to make their access seamless. 

### Task 1: Verify the device is not enrolled
You should first verify that the device you want to enroll into Intune is not already enrolled. 

1. You should still be logged into LON-CL1 as the **Admin** and into Microsoft 365 as **Holly Dickson**.
2. In your **Edge** browser, you should have the **Microsoft Endpoint Manger admin center** portal open in a tab that's displaying the **Device configuration | Profiles** window. At the top of the screen is the following navigation thread: **Home > Devices |Configuration Profiles**. <br/>

   In this thread, select **Home**.
3. In the **Microsoft Endpoint Manger admin center** page, in the  navigation pane  select **Devices**.
4. On the **Devices** window, in the left-hand pane under **Manage**, select **All Devices** and verify that LON-CL2 is listed in the details pane. <br/>

   **Note:** LON-CL2 was enrolled into Intune in an earlier lab when you configured integration between Azure AD and Intune. When you joined LON-CL2 to Azure AD, it was automatically enrolled to Intune.  
5. You now want to start the **Certificates** MMC for the local machine. In the Search field on the taskbar, enter **run**, and then on the menu, select **Run**.
6. In the **Run** window, enter **certlm.msc** in the **Open** field and then select **OK**.
7. Maximize the **certlm – [Certificates – Local Computer]** window, and then drag the pane divider to the right so that you can see the entirety of the left-hand pane. 
8. In the left-hand pane, select **Personal** and verify that no certificate is listed in the details pane on the right.
9. Minimize the **certlm – [Certificates – Local Computer]** window as you will use it in a later task.

### Task 2: Enroll the device to Azure AD and Intune

1. In **LON-CL1**, in the Search field on the taskbar enter **access work**, and then in the menu, select **Access work or school**.
2. In the **Settings** app, in the **Access work or school** section, select **+Connect**.
3. In the **Microsoft account** window, on the **Set up a work or school account** page, select **Join this device to Azure Active Directory**.
4. On the **Let's get you signed in** page, in the **Work or school account** text box, enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) and then select **Next**.
5. On the **Enter password** page, enter **Pa55w.rd** in the **Password** field and then select **Sign in**.
6. On the **Make sure this is your organization** dialog box, review the information and if everything looks correct, select **Join**.
7. On the **You're all set!** page, select **Done**.
8. In the **Settings** app, in the **Access work or school** section, verify that the device is connected to Azure AD and then close the **Settings** app by selecting the **X** in the upper right-hand corner.
9. On the **Devices | All devices** page in the Microsoft Endpoint Manger admin center, in the Navigation pane under select **Devices**. You should see both **LON-CL1** and **LON-CL2**.
9. Leave all browser tabs open for the next task.

### Task 3: Verify the device is enrolled to Azure AD and Intune
In an earlier lab you configured integration between Azure AD and Intune. Because of that, any device that is joined to Azure AD is automatically enrolled to Intune. In this task you will join LON-CL2 to Azure AD, which will automatically enroll it into Intune.

1. You should still be logged into **LON-CL1** as the **Admin** account, and you should still be logged into Microsoft 365 as **Holly Dickson**.
2. In **LON-CL1**, select the **certlm – [Certificates – Local Computer]** icon on the taskbar.
3. In the **certlm – [Certificates – Local Computer]** console, in the left-hand navigation pane, the **Personal** folder should already be selected from the prior task. In the menu bar, select **Action** and then select **Refresh**.
4. In the left-hand pane, under the **Personal** folder, select **Certificates**. In the details pane, verify that several certificates are listed.<br/>

    **Note**: Those certificates were added when you joined the LON-CL1 device to Azure AD, which in turn enrolled it to Intune.
5. Close the **certlm – [Certificates – Local Computer]** window. 
6. In your **Edge** browser, in the **Azure portal**, the **Devices | Azure AD devices** window should be displayed from the prior task.
7. In the details pane on the right, both **LON-CL1** and **LON-CL2** are displayed. In the **MDM** column, note that both are enrolled to **Microsoft Intune**.  <br/>

    **Note:** This view lists devices that are joined to Azure AD. Remember that you configured integration between Azure AD and Intune, and because of that, any device that is joined to Azure AD is automatically enrolled to Intune.
8. In the **Devices** window, in the lef-hand pane under **Overview**, select **All devices**.
9. In the **Devices | All devices** window, verify that both devices are listed. Note the value displayed in the **Ownership** column for each device. Since LON-CL1 was enrolled by Holly, an administrator, LON-CL1 is classified as a corporate device. Conversely, since Joni Sherman, a non-admin, enrolled LON-CL2, device ownership is classified as a personal device. <br/>

10. Leave all browser tabs open for the next task.


# Proceed to Lab 4 - Exercise 5
