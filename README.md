# Overview: Lab 3 Creating Help Desk Accounts in Active Directory and Using CMD Commands

Overview: Lab 3 Creating Help Desk Accounts in Active Directory and Using CMD Commands
This section of my home lab documentation demonstrates the creation of a dedicated Help Desk account in Active Directory (AD) and managing it using command-line tools (CMD). This task highlights the practical steps involved in provisioning accounts for IT support personnel, ensuring proper permissions, and configurations, and automating the process to streamline account management. Additionally, this project focuses on the administrative tasks that a Help Desk account might handle, such as password resets and user account modifications.

## Objectives
- Create a specialized Help Desk account in Active Directory.
- Use CMD commands to verify account creation and configuration.
- Assign appropriate permissions to the Help Desk account for administrative tasks.
- Enable the Recycle Bin through Active Directory Administrative Center to enhance account recovery processes.
## Documentation
For this home lab, we will create a Help Desk account with the appropriate permissions for administrative tasks through Active Directory. We will also enable certain features in our Active Directory settings and use specific CMD lines to automate and verify account creation and configuration.

1. Before creating the Help Desk account, let's begin by enabling the Recycle Bin to restore deleted items if needed. To do this, search for "Active Directory Administrative Center" in the search bar at the bottom left and open it.

![68747470733a2f2f692e696d6775722e636f6d2f316255305733742e706e67206865696768743d](https://github.com/user-attachments/assets/418cd4f2-207c-493f-aa6e-2572baad1ff6)

<br>
2. In the Active Directory Administrative Center, select "SimoTech.com (local)," then click on "Enable Recycle Bin." Click "OK" to confirm and enable the Recycle Bin feature.

<br>

<img width="542" alt="Screenshot 2025-02-14 at 12 18 06 AM" src="https://github.com/user-attachments/assets/f04c64bd-aee7-4805-a629-e835198b1ab5" />

<br> 

3. Once you enable the Recycle Bin, the "Enable Recycle Bin" option should be grayed out, and you should now see "Deleted Objects" listed under your local domain in the Active Directory Administrative Center. This confirms that the Recycle Bin feature has been successfully enabled.

<br> 

<img width="985" alt="Screenshot 2025-02-17 at 2 08 20 AM" src="https://github.com/user-attachments/assets/40c25a99-ba9f-43a0-a15a-1d6a39bcfa2b" />

<br> 


4. Now lets open up Server Manager by searching it in our search bar on the bottom left.

<br>


<img width="985" alt="Screenshot 2025-02-17 at 2 12 18 AM" src="https://github.com/user-attachments/assets/9d445b80-d3d7-45b7-aac3-004cef5a9d9c" />

<br>

5. With Server Manager open, on the top right, select “Tools” then “Active Directory Users and Computers”. 
<br>


<img width="985" alt="Screenshot 2025-02-17 at 2 13 51 AM" src="https://github.com/user-attachments/assets/79251df4-5ccf-47ef-8719-b10bb67d33fd" />

<br>

6. Lets also pin Server Manager and Active Directory Users and Computers to our task bar by right clicking the icons on the bottom and select “Pin to task bar”.

<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 13 51 AM" src="https://github.com/user-attachments/assets/be02a051-3e94-4e04-88a0-a992a7855708" />

<br>
7. Now, open "Active Directory Users and Computers," click on "View" at the top, and then select "Advanced Features" to enable advanced options in the interface.

<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 19 59 AM" src="https://github.com/user-attachments/assets/114fae78-aaa4-4821-9c7d-8dbc4c3b2380" />

<br>

8. In the "tobifash.com" domain, select "Users," then right-click on the "Administrator" account and choose "Copy." This will replicate the appropriate permissions from the Administrator account to the new Help Desk account, ensuring it has the necessary administrative permissions for tasks.

<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 23 38 AM" src="https://github.com/user-attachments/assets/b54ce737-bccc-42c5-b819-576cd764ac70" />

<br>

9. For the new Help Desk account, use "Helpdesk" as both the first name and last name, and set the same for the User logon name (Helpdesk). This will help maintain consistency and clarity for the account.

<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 27 57 AM" src="https://github.com/user-attachments/assets/e8629129-243b-4255-93e4-6312d62c8ce0" />

<br>

10. Create a password for our helpdesk account. Then select “finish”.

<br>

<img width="542" alt="Screenshot 2025-02-14 at 12 25 40 AM" src="https://github.com/user-attachments/assets/7682ee0e-8d79-4e1d-a79f-f3125453571b" />

<br>

11. Now we can see that our Helpdesk account is part of the same groups as our Administrator account.

<br> 

<img width="985" alt="Screenshot 2025-02-17 at 2 32 09 AM" src="https://github.com/user-attachments/assets/bb62f6ca-f961-4d37-93b6-1b5d00e51529" />

<br>

12. Now, let's focus on important CMD lines for admins and the helpdesk. First, open the Command Prompt by searching for "Command Prompt" in the search bar at the bottom left and selecting it from the results.

<br> 

<img width="985" alt="Screenshot 2025-02-17 at 2 33 09 AM" src="https://github.com/user-attachments/assets/8aa4ae12-8d9e-4cc0-b9e8-834dd129a582" />

<br>

13. For our first command, type ipconfig and press Enter. This command will display details about your computer's network setup, including your IPv4 address, subnet mask, and other network configuration information.
    
<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 34 54 AM" src="https://github.com/user-attachments/assets/4ed3c19b-6ed0-497e-8e0b-3a510fba6f8e" />

<br>


14. We can also type “ipconfig /all” which will display our computer's entire network configuration. It displays all network adapters, our settings, and additional information not shown by the basic ipconfig command such as the DHCP server, DHCP enabled, Lease Obtained and Lease Expires.

<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 36 21 AM" src="https://github.com/user-attachments/assets/fc2e00e9-f7dd-44da-85fc-a98700b9d547" />

<br>

15. Another useful command is net use. This command is used for managing, connecting, and disconnecting network resources, such as printers, shared disks, and other devices. Although we don’t have any resources mapped yet, it will allow us to view existing connections to shared resources or map shared network resources to a drive letter.
<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 37 52 AM" src="https://github.com/user-attachments/assets/91708a4c-abc8-40d8-96c4-3adb02d2325f" />

<br>

16. The next command is net user helpdesk /domain. This command provides comprehensive details about the "helpdesk" user account, including group memberships, password restrictions, and login configurations. It’s especially useful when managing domain user accounts on a computer that is part of a domain, allowing you to view attributes and settings related to the designated account.

<br>

<img width="985" alt="Screenshot 2025-02-17 at 2 39 14 AM" src="https://github.com/user-attachments/assets/f9bbae25-4f74-4a8b-adf3-f359252d53a5" />

<br>

Congratulations! We have successfully created the Helpdesk account using Active Directory Users and Computers and executed essential command-line tasks that are crucial in a Helpdesk environment. Great work!

👉 Next Lab 4 : [Windows 10, Join PC to Domain (Helpdesk), RSAT Tool, Server Manager](https://github.com/tobifash0/Windows-10-Join-PC-to-Domain-Helpdesk-RSAT-Tool-Server-Manager)





