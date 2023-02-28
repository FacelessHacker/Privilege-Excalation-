# READ CONTENT OF SAM FILE USING CMD & PSEXEC

## What is SAM file?

Security Account Manager (SAM) is a database file in Windows 11/10/8/7/XP that stores user passwords in encrypted form. It is usually located in the following directory:
(C:\Windows\system32\config). Sam file cannot be opened, copied or read while windows is running for security reasons. However, to bypass this hinderance using PSEXEC, we will follow the steps below.

### Read Content of SAM File with CMD (Command Prompt)

- Run the command prompt as the system user
- Enter the commnands below

  ```
  reg save hklm\sam C:\samcopy
  ```
  ```
  reg save hklm\system C:\systemcopy
  ```
  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(77).png)
  
  Note that C:\samcopy is the name of the path you want to save the copy of sam file & same goes for the system file
  
 - Check the location you entered, you will see your files there.
 
  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(79).png)
  
 - Right click and open the files with notepad or any available editing App.
 
 - Note that you will be able to open and read the file but, it is still in the encrpted form.
  
### Opening SAM File Through Registry Editor 

- Navigate to  PSTOOLS on your command prompt
- Type the command below to access the registry editor as the system user

  ```
  psexec -i -d -s c:\windows\regedit.exe
  ```
  
  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(80).png)


### Reading SAM File in Plaintext 
- Download Samfile reader to read the content of sam file
- Use John the Ripper to read it.
