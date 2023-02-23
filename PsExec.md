# RUNNING CMD THROUGH PSEXEC

##### Follow the steps below to run cmd.exe using PsExec

- Download PsExec Tools from Microsoft Sysinternals using this link https://learn.microsoft.com/en-us/sysinternals/downloads/psexec

  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(70).png)

- Extract the zip file to a preferable location on your drive

  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(71).png)


- Here, lets place it in the C:\ drive directly.

  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(72).png)


  It's best to place in the C:\drive directly or under C;\Windows\System32
  
- PSTOOLS sitting pretty in C: drive

  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(73).png)

  
- Now, run your Command Prompt as administrator 
- Use the command below to change to the C: drive
  ```
  cd \
  ```

  This places you in the root directory of your drive, where psexec is located.
  
- In this sample, our psexec is under the PSTOOLS so, we can chnage the directory to the location using
  ```
  cd \PSTOOLS
  ```
  

- Use the command below to run cmd using  psexec
  ```
  psexec -sid cmd
  ```
  
- When the command completes, a cmd shell will be launched.

- Type whoami; it will say ' nt authority\system" which means you are running cmd through psexec as the System User.

  ![UI Image](https://github.com/FacelessHacker/Privilege-Excalation-/blob/main/Screenshot%20(75).png)

