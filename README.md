# Active-Directory-Account-Creation-CMD-Commands

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

