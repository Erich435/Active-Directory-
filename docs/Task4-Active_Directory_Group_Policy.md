# Task 4 - Configure Active Directory Group Policy:
* Create an OU named **ITOffice**
* Create an OU named **Users (OU)**
* Assign users **ITadmin** and **ServiceDesk** to the **ITOffice** group
* Assign user **John** to the **Users** group
* Create and apply a Group Policy Object to enforce a standardized desktop background

# Steps performed

1. Created two new Organizational Units (OUs) within Active Directory Users and Computers
  * **ITOffice**
  * **Users (OU)**

2. Dragged and dropped users into respective OUs from the **Users** container
   * John: Users (OU)
   * ITadmin: ITOffice
   * ServiceDesk: ITOffice
  
3. Created basic backgrounds using windows paint colour coded for each OU group
   * Red background: ITOffice
   * Blue background: Users (OU)
   * Created a shared network folder with path - \\Dc01\sysvol\lab.local\Resources\GPO-Wallpapers
   * Saved both desktop images as .png files inside this shared network path

  
4. Opened Group Policy Management from Server Manager and created two new GPOs under the lab.local domain
   * ITOffice Desktop GPO
   * Users (OU) GPO

5. Edited both GPOs to enforce desktop background by editing GPOs and using the following path **User Configuration -> Policies -> Administrative Templates: Policy definitions -> Desktop** -> From here the Desktop wallpaper setting was edited and the path to the relevant desktop backgrounds were specified

6. Signed into client machine as ServiceDesk user in order to open up command prompt, on the command prompt page I entered **gpupdate /force** to update group policy on that virtual machine

7. Signed out of client machine after gpupdate had completed and signed back in with user **John** in **Users (OU)** Group and both users **ITadmin** and **ServiceDesk** in group **ITOffice** to validate group policy had been conrrectly configured

 # Problems encountered:
  * During original test of group policies configuration, all users including user **John** had a red desktop background; this proved to me there was an issue with the configured group policy as user **John** had been assigned to **Users (OU)** and should have had a blue background, not red.
  * Upon inspection of Group Policy Management, I noticed that both Group Policy Objects were assigned to the domain itself instead of the respective OUs, upon correction a gpupdate was forced on the client virtual machine and this fixed the issue.

  * # Validation
  * * User John's background is blue as per GPO
    * Users: ITadmin and ServiceDesk backgrounds are red as per GPO

![Active Directory OU Configuration](/docs/images/ADOU.png)
![Blue and red desktops](/docs/images/Desktops.png)
