# INC941968 – Network Drive Access Issue (Network Path Not Found)

**Category:** Network / File Access  
**Priority:** Not specified  
**Status:** Resolved  
**Reported by:** Kevin Zhang  
**Department:** Engineering

### 1. Issue Description

The user reported that their team's shared network drive (D: Engineering) was still visible on their computer but could not be opened. When attempting to access the drive, Windows displayed the following error:

**"Location is not available – The network path was not found."**

The user confirmed that other team members could access the same shared folder from their own computers, suggesting that the issue was related to the network drive configuration on the affected computer rather than a server-wide issue.

**Business Impact:** The user was unable to access the shared departmental files required for daily work, preventing them from accessing important documents and affecting their productivity.

### 2. Troubleshooting & Investigation

I connected to the user's laptop through Remote Desktop to investigate the issue and identify the cause.

The following steps were taken:

1. **Connected to the user's computer:** Established a remote desktop connection to access the user's laptop and perform troubleshooting.
2. **Inspected the existing network drive:** Opened File Explorer and checked the mapped network drive. Attempted to access the drive and identified the "Network path was not found" error.
3. **Removed the old network path:** Deleted the existing mapped drive configuration because the previous network path was no longer accessible.
4. **Retrieved the correct file server path:** Accessed the internal IT documentation under Documentation > File Server to obtain the correct shared folder network path.
5. **Re-mapped the network drive:** Opened File Explorer again and mapped the D: drive using the correct file server path.
6. **Verified drive accessibility:** Checked whether the network drive could be accessed successfully after remapping.

### 3. Resolution

After identifying the incorrect or outdated network drive mapping, I reconfigured the drive using the correct file server path obtained from the internal documentation.

Actions performed:

1. Opened File Explorer on the user's computer.
2. Removed the old network drive mapping.
3. Accessed the internal File Server documentation.
4. Retrieved the correct network folder path (UNC path).
5. Re-mapped the shared network drive using the correct path.
6. Tested the drive to ensure it was accessible.

### 4. Outcome

The network drive was successfully re-mapped, and the user was able to open the shared folder without encountering the previous network path error.

I contacted the user through the company chat to confirm that the drive was working properly. The user replied, **"Yep, I can open it now. Thanks."**, confirming that the issue had been resolved.

**Final Status:** Resolved – Network drive successfully re-mapped using the correct file server path, and access restored after user confirmation.

### 5. Skills Demonstrated

- Remote Desktop Support
- Windows File Explorer Troubleshooting
- Network Drive Mapping and Configuration
- UNC Path Identification
- File Server Navigation
- IT Documentation Reference
- Network Connectivity Troubleshooting
- End-user Communication and Support
- Incident Investigation and Resolution
- Ticket Management and Follow-up
