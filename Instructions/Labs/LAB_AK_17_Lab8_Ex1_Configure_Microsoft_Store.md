# Module 17 - Lab 8 - Exercise 1 - Configure the Microsoft Store for Business


You are the system administrator for Adatum Corporation, and you have Microsoft 365 deployed in a virtualized lab environment. In this lab, you will work with Microsoft Store for Business. 

**Note:** Company employees can use the Microsoft Store app for accessing Microsoft Store for Business. However, because it can take up to 36 hours for newly added apps to propagate to the private store and be visible in the Microsoft Store app, this lab used a web browser to access the Microsoft Store for Business and configure Adatum’s private store. 

### Task 1: Sign up for Microsoft Store for Business and perform initial configuration 

In this task, you will install the Microsoft Store for Business and then you’ll configure it so that apps from the Microsoft Store for Business will be allowed to run on devices that Windows Defender Device Guard is protecting.

1. You should still be logged into your Client 1 VM (LON-CL1) as the **Adatum administrator** and into Microsoft 365 as Holly Dickson (**holly@M365xZZZZZZ.onmicrosoft.com)** with a password of **Pa55w.rd**. 

2. In your Edge browser, enter the following URL in the address bar: **https://www.microsoft.com/business-store** 

3. This opens the **Microsoft Store for Business**. In the top-right corner, select **Sign in**. 

4. If you are not signed in automatically, enter **Holly@M365xZZZZZZ.onmicrosoft.com** (where ZZZZZZ is your tenant ID provided by your lab hosting provider) in the **Sign in** window and then select **Next.**

5. On the **Microsoft Store for Business** page, in the menu bar at the top of the page, select **Shop for my group**. 

6. Scroll down to the **Made by Microsoft** section and select **Show all.**

7. In the **Made by Microsoft** page, select **Microsoft Remote Desktop.**

8. On the **Microsoft Remote Desktop** page, select **Get the app**. 

9. On the **Microsoft Store for Business and Education Services Agreement** page, scroll to the bottom of the page, select the **I accept this agreement and certify that I have the authority to bind myself (and my organization, if applicable) to its terms** check box, and then select **Accept.** 

10. In the **Thanks for your order** window, select **Close**. 

11. On the **Microsoft Store for Business** page, on the menu bar at the top of the page, select **Manage**. 

12. In the left-hand navigation pane, select **Products &amp; services**. 

13. In the **Products and Services** detail pane, scroll down and verify that the **Excel Mobile**, **Microsoft Remote Desktop**, **OneNote**, **PowerPoint Mobile**, **Sway**, and **Word Mobile** apps are listed. 

14. In the left-hand navigation pane, select **Settings**. 

15. In the **Settings** pane, on the **Shop** tab, scroll down to the **Shopping experience** section and select the **Show offline apps** switch to turn it **On**. 

16. In the **Microsoft 365 admin center**, on the menu bar at the top of the page, select **Adatum Corporation**. This is Adatum’s private store. 

17. As part of your pilot project, you want to change the name of your store to **Adatum private store**. On the **Adatum Corporation** private store page, select the **ellipsis (…)** icon to the right of **Adatum Corporation**, and in the menu that appears, select **Edit collection**. 

18. On the **Edit collection** page, to the right of **Adatum Corporation**, select **Rename private store**.

19. On the **Settings** page, under the **Private store** section, to the right of **Your private store name: Adatum Corporation**, select **Change**.

20. In the **Private store** dialog box, enter **Adatum private store** and then select **Save**. <br/>

    Note the change to your private store name on the menu bar at the top of the page.

21. On the menu bar, select **Adatum private store**.

22. On the **Adatum private store** page, verify that it displays the **Sway**, **OneNote**, **PowerPoint Mobile**, **Excel Mobile**, and **Word Mobile** apps.  <br/>

    ‎**Note:** Earlier when you viewed **Products and Services**, it included this list of client apps, along with Microsoft Remote Desktop app. You do not see the Microsoft Remote Desktop app in your private store because you already got the app at the start of this task.

23. Leave the **Microsoft Store for Business** tab open in your Edge browser. You will use this in the next exercise. 

 
# Proceed to Exercise 2
