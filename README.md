# AADPendingDevices

Pending devices indicates that the device has been synchronized successfully using Azure AD connect form your on-premise Active Directory and it is ready for device registration, but is not registered to Azure AD yet.

This also means that the device object in Azure AD waits the device registration process to be triggered and complete successfully to get the device connected to Azure AD as hybrid Azure AD joined device as needed. Learn more about Hybrid Azure AD Device Registration procedure.

The device state could be changed from having a registered state to PENDING, if one of the following actions:

- The device deleted from Azure AD, and then synced back form the on-premise Active Directory.
- The device removed from sync scope and added back. 

 

Due to the fact that it is not easy to search for all PENDING devices in Azure AD devices blade. Get-AADPendingDevices PowerShell script gives you the power to accomplish the following:

- Retrieve all pending devices from an Azure AD tenant.
- Manage pending devices by removing them form Azure AD tenant. 

 

# Why is this script useful?
- To check pending devices in Azure AD tenant.
- To generate a powerful Excel report with the pending devices.
- To automate Azure AD pending devices cleanup procedure by running it in a scheduled task.
- To show the result on CSV or/and Grid View or/and Excel, so you can easily search in the result. 

# What does this script do?
- Verifies the pending devices as per the entered threshold days.
- Cleans pending devices from Azure AD.
- Checks if ‘MSOnline‘ module is installed and updated. If not, it takes care of this.
- Checks if ‘ImportExcel‘ module is installed. If not, it installs and imports it. 

# User experience:

- If there is no pending devices in AAD tenant: 

![Alt text](https://github.com/mzmaili/AADPendingDevices/blob/master/Nopending.PNG "PS output")

- CSV file output: 
![Alt text](https://github.com/mzmaili/AADPendingDevices/blob/master/csv.PNG "CSV output")

- Excel output: 
![Alt text](https://github.com/mzmaili/AADPendingDevices/blob/master/Excel.PNG "Excel output")
 

 
