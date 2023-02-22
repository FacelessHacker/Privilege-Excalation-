# Privilege-Excalation-

Place it in your C:\ drive.
Logon as a standard or admin user and use the following command: cd \. This places you in the root directory of your drive, where psexec is located.
Use the following command: psexec -i -s cmd.exe where -i is for interactive and -s is for system account.
When the command completes, a cmd shell will be launched. Type whoami; it will say 'system"
Open taskmanager. Kill explorer.exe.
