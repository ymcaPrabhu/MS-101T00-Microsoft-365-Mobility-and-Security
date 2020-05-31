# Module 2 - Lab 2 - Exercise 1 - Implement a Safe Attachments policy 

You now have a Global Admin account set up for Holly Dickson, and you&#39;re signed into Microsoft 365 as Holly. In this first phase of your pilot project for Adatum, you want to create a Safe Attachments policy and turn on Advanced Threat Protection for SharePoint, OneDrive, and Microsoft Teams. 

**Note:** You will not be able to validate the Safe Attachments policy. To do so would require that you attach a virus or malware-infected file to an email, which is something that Microsoft does not recommend.

### Task 1 – Create a Safe Attachment policy and turn on ATP for SharePoint, OneDrive, and Microsoft Teams

In this task, you will turn on ATP for SharePoint, OneDrive, and Microsoft Teams, and you&#39;ll create an ATP Safe Attachments policy that will test email attachments for malware that are sent to recipients within the M365xZZZZZZ.on microsoft.com domain. You will configure the policy so that if an attachment is blocked, it will be removed from the email that is sent to the recipient, and a copy of the email will be redirected to Joni Sherman for additional review.

1. Switch back to your Client 1 VM (LON-CL1). You should still be logged into your Client 1 VM as the **Admin** account, and you should be logged into Microsoft 365 as **Holly Dickson**.
2. After finishing the previous task, you should still be in the **Office 365 Security &amp; Compliance center**. If not, in your browser, enter **https://protection.office.com.**
3. In the **Office 365 Security &amp; Compliance center**, in the left-hand navigation pane select **Threat Management** and then select **Policy**.
4. In the **Policy** window, select the **ATP Safe Attachments** tile.
5. In the **Safe attachments** window, at the top of the page under the **Protect files in SharePoint, OneDrive, and Microsoft Teams** section, select the **Turn on ATP for SharePoint, OneDrive and Microsoft Teams** check box.
6. Under the **Protect email attachments** section, select the **plus (+) sign** on the menu bar to add a new Safe Attachments policy.
7. In the **new safe attachments policy** window, enter **AttachmentPolicy1** in the **Name** field.
8. Under the **Safe attachments unknown malware response** section, select the **Dynamic Delivery** option. This option will still send the email but will hold the attachment until it has been scanned and marked acceptable.
9. Under the **Redirect attachment on detection** section, select the **Enable redirect** check box.
10. In the **Send the attachment to the following email address** field, enter **JoniS@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your unique tenant ID provided by your lab hosting provider).
11. Under the **Applied To** section, under **If** (the first condition), select the drop-down arrow and select **The recipient domain is...**
12. In the **NAME** dialog box, select the **M365xZZZZZZ.onmicrosoft** domain (where ZZZZZZ is your tenant ID provided by your lab hosting provider), select **add->**, and then select **OK**.
13. On the **new safe attachments policy** window, select **Save**.
14. Two warning messages will be displayed regarding the **Dynamic Delivery** and **Enable redirect** options that were selected. Select **OK** for each.
15. It may take a minute or so to update the organization settings. You may experience a UI issue where the list of policies that displays at the bottom of the screen can be hard to see, but it should display a message below the list indicating **1 selected of 1 total**.
16. Leave the Client 1 VM and the Security &amp; Compliance Center tab open for the next lab.

**NOTE:** Unfortunately, we are unable to create a training lab in which you can validate the ATP Safe Attachments policy that you just created. To do so, you must send an email that contains a malicious attachment. There are some common test viruses that are available, such as the EICAR test virus; however, with well-known test viruses such as EICAR, the messages in which they are attached get quarantined before they can be processed by Office 365 ATP. Since the ATP Safe Attachments functionality is meant to protect against unknown and zero-day viruses and malware, it is very difficult, and not recommended, to create such an attachment.

That being said, after you have defined ATP Safe Attachment policies in your real-world environment, one good way to see how the service is working is by viewing Advanced Threat Protection reports. For more information on using ATP reporting to validate your Safe Links and Safe Attachment policies, see [View reports for Office 365 Advanced Threat Protection](https://docs.microsoft.com/en-us/office365/securitycompliance/view-reports-for-atp).


# Proceed to Lab 2 - Exercise 2

