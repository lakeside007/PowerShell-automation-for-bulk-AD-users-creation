# Using a PowerShell Script to automate the creation of user profiles for 1,000 users in Active Directory.




<h2>Description</h2>
This repository provides a comprehensive guide on using a PowerShell script to automate the creation of 1,000 Active Directory (AD) domain users. This walkthrough is aimed at system administrators and IT professionals who want to streamline user management in an Active Directory environment.
<br />

<h2>Purpose</h2>
Creating multiple user accounts manually can be time-consuming and prone to errors. This guide demonstrates how to efficiently use PowerShell to automate the bulk creation of user accounts, enhancing productivity and ensuring consistency.

<h2>Environments Used </h2>

- <b>VirtualBox</b>
- <b>Windows Server 2019</b>
- <b>PowerShell ISE</b>

<h2>Project walk-through:</h2>

<p align="center">
First step was generating random 1,000 first and last name to use. I also added my own name to show the realism of this lab. <br/>
<img src="https://imgur.com/uqnjGNL.png" height="80%" width="80%" alt="Generating 1,000 user first and last names"/>
<br />
<br />
Click the Windows button, search for PowerShell and ensure to select PowerShell ISE. PowerShell Integrated Scripting Environment (ISE) is a graphical user interface and scripting environment for Windows PowerShell. It provides a user-friendly platform for writing, testing, and debugging PowerShell scripts and commands :  <br/>
<img src="https://imgur.com/H2t4Y2q.png" height="80%" width="80%" alt="Opening up PowerShell ISE to perform scripting"/>
<br />
<br />
If the script has been pre-written in a file, select the file icon as indicated in the screenshot to upload it to PowerShell ISE interface to begin adjusting and running.<br/>
<img src="https://imgur.com/ruTg4sx.png" height="80%" width="80%" alt="Upload the script to PowerShell ISE"/>
<br />
<br />
After observing the script and finally trying to progress to the next stage by running the script, an error code shows which indicates inability to run the script because it is not digitally signed as a sign of safety and securtiy, this is primarily a good security practice because it prevents bad scripts from running without the consent of the user. However, we need a way to run the script regardless.<br/>
<img src="https://imgur.com/qvCnpsq.png" height="80%" width="80%" alt="Inability to run script due to it not being digitally signed"/>
<br />
<br />
The Execution Policy has to be unrestricted for the script to run successfully without hindrance due to no digitally signed signature.  <br/>
<img src="https://imgur.com/YJTAst9.png" height="80%" width="80%" alt="Finish creating the domain controller."/>
<br />
<br />
Select Yes to All to allow any and every script be able to run on PowerShell ISE  <br/>
<img src="https://imgur.com/5tnPCfq.png" height="80%" width="80%" alt="Yes to All"/>
<br />
<br />
Change directory to where the script is located exactly on the computer then use 'ls' to list the content of the directory. Once the file name of the script has been seen, navigate to it by typing the whole directory name and also the file name at the end to indicate the exact file intended to be ran. <br/>
<img src="https://imgur.com/ifcoEoK.png" height="80%" width="80%" alt="Change directory to file location"/>
<br />
<br />
Select Run Once to run the script. Note that the script uses the generated names in the names.txt file to run the domain user creations. <br/>
<img src="https://imgur.com/I2uPOj8.png" height="80%" width="80%" alt="Running the script"/>
<br />
<br />
User creation starts and takes about a minute to complete <br/>
<img src="https://imgur.com/UTgPSPa.png" height="80%" width="80%" alt="User creation kickstarted"/>
<br />
<br />
Opened Active Directory and selected users in the domain to confirm if the script really worked and yes it did, 1,000 domain users + 1 (my name) now successfully created within a couple of minutes, this has saved time, energy and helped avoid mistakes that could happen during bulk user management. <br/>
<img src="https://imgur.com/esugxE6.png" height="80%" width="80%" alt="Confirmation of created users"/>
<br />
<br />
I initially added my name to the list of generated names that was used to create the domain users so it is expected that a domain user account was created for me as well. I right-clicked on USERS then selected Find to search for my name, viola! A domain user account was created for me alongside others. This is confirmation that everything worked according to plan! <br/>
<img src="https://imgur.com/xk9xplG.png" height="80%" width="80%" alt="User creation kickstarted"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
