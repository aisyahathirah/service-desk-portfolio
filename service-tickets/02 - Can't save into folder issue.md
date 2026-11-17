# INC162164 – Unable to Save or Create Folders in Shared Drive

**Category:** Software / Access Permissions  
**Priority:** Medium  
**Status:** Resolved  
**Reported by:** Tyler Grant  
**Department:** Sales

### 1. Issue Description

The user reported being unable to save new files or create folders in the Reports directory on the D: drive after the folder structure had been reorganized.

The user could still access and open existing reports but received a permission-related error when attempting to save new files or create folders.

Other directories, such as Shared Documents and Templates, were functioning normally. The issue also appeared to affect other members of the Sales department.

**Business Impact:**

The Sales team's pipeline report was stored in the affected directory and accessed by management. Due to the permission issue, the user was unable to update the report, potentially delaying reporting activities.

### 2. Troubleshooting & Investigation

I investigated the issue to determine whether it was related to the user's local computer or the shared folder permissions.

The following steps were taken:

1. **Remote Desktop Connection:** Connected to the user's computer remotely to reproduce and verify the reported issue.
2. **Accessed the File Server:** Navigated to the server room and accessed FILESERVER01, which hosts the shared file directories.
3. **Located the Affected Directory:** Opened File Explorer and navigated to D:\Shares\departments\Sales to locate the shared folders.
4. **Accessed Administrator Credentials:** Referred to the internal documentation to retrieve the authorized administrator username and password required to manage the folder permissions.
5. **Investigated Sharing Permissions:** Opened the affected folder's Properties and navigated to Sharing → Advanced Sharing → Permissions.
6. **Updated Folder Permissions:** Modified the sharing permissions to restore the user's ability to save files and create new folders.

### 3. Resolution

The issue was resolved by correcting the sharing permissions on the affected directory in FILESERVER01.

Actions performed:

1. Accessed the affected folder's Properties.
2. Selected the Sharing tab.
3. Opened Advanced Sharing.
4. Selected Permissions.
5. Updated the necessary permissions to allow the user to access and modify the shared folder.
6. Confirmed the changes.

### 4. Outcome

After updating the sharing permissions, I contacted the user through company chat and requested that they test saving files and creating folders in the affected directory.

The user confirmed that everything was working properly again.

**Final Status:** Resolved – Shared folder permissions successfully updated and user access restored.

### 5. Skills Demonstrated

- Windows Server file-sharing administration
- Shared folder permissions management
- Remote Desktop troubleshooting
- Access control and permission configuration
- Server and directory navigation
- Incident investigation and resolution
- End-user communication and verification
