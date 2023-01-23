<h1>Active Directory Deployment</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
Active Directory is a database and set of services that connect users with the network resources they need to get their work done. The database (or directory) contains critical information about your environment, including what users and computers there are and who's allowed to do what.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell Ise</b> 
- <b>Server Manager</b>
- <b>Microsoft Azure</b>
<h2>Environments Used </h2>

- <b>Windows 10</b> (21H2)
- <b>Remote Desktop</b>

<h2>Program walk-through:</h2>

<p align="center">
Step 1: Creating the Domain and Client through Microsoft Azure: <br/>
<br />
<br />


https://user-images.githubusercontent.com/119460677/213619351-5dde2022-8b5a-4b68-850d-fec003823826.mp4




<br />
<br />
<p align="center">
Step 2: In Azure, Set Domain Controller’s (DC-1) NIC Private IP address to be static:
<br/>


https://user-images.githubusercontent.com/119460677/213609792-7a9cd55c-b7e6-4031-8237-79514d4d58eb.mp4

<br />
<br />
<p align="center">
Step 3: Login to the DC-1 (remote desktop) and enable ICMPv4 Protocols through Windows Firewall: <br/>
<br />

https://user-images.githubusercontent.com/119460677/213612294-610c95ef-d380-4f13-b2c8-b88996f2308a.mp4


<br />
<br />
 
</p>
<br />
<br />
<p align="center">
Step 4: Install Active Directory : Login to DC-1 to install Active Directory Domain Services, it also requested to create a forest called "myteddy.com" shown in the picture example after the video

 <br/>

https://user-images.githubusercontent.com/119460677/213621848-956ab6bb-2e68-445b-a203-094e8e749160.mp4

</p>
<br />
<br />
<p align="center">
Step 4 cont'd: Create forest during active directory installation
<br />
<br />
 <img src="https://i.imgur.com/JusQXiY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

</p>
<br />
<br />
<p align="center">
Step 5 Post AD installation: In Active Directory Users and Computers create an Organizational Unit called “_EMPLOYEES_”
Create a new OU named “_ADMINS_”
<br />
<br />
 
https://user-images.githubusercontent.com/119460677/213623591-ce98c861-3f94-44cd-95ca-37e35889df54.mp4


<br />
<br />
<br/>
<p align="center">
Step 5 Post AD installation: Create a new employee named “Luffy Monkey” (same password) with the username of “Luffy_admin”
 
<br />
<br />


https://user-images.githubusercontent.com/119460677/213626070-d3ef4de0-7696-4940-8257-692d417dd1fb.mp4

</p>
<br />
<br />
  <br/>
<p align="center">
Step 5: set Client-1’s DNS settings to the DC’s Private IP address, restart client 1.
<br />
<br />


https://user-images.githubusercontent.com/119460677/213627540-ebfa1117-f602-40eb-9c1f-0fe5acb08e2d.mp4


</p>
<br />
<br />
<p align="center">
Step 5 cont'd: Restart client 1.  <br/>
 <br />
<br />
<img src="https://i.imgur.com/GWILOLN.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<br />
<br />

</p>
<br />
<br />
<p align="center">
Step 6: Login to Client-1 (Remote Desktop) as the original local admin (labuser) and join it to the domain computer will restart. :  
<br/>
<br />
<br />
 
https://user-images.githubusercontent.com/119460677/213628327-a2a802f5-d735-469e-af4e-60cdeda8b895.mp4


</p>
<br />
<br />
<p align="center">
Step 7: Click “Remote Desktop” Allow “domain users” access to remote desktop. 
 Now we're able to login into Client-1 as a non-administrative user.
<br />
<br />
 
<img src= "https://i.imgur.com/ERlcnvW.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<br />
<br />
 
</p>
<br />
<br />
<p align="center">
Step 8: Login to DC-1 as Luffy_Admin
<br />
<br />
<img src= "https://i.imgur.com/bFI4pnJ.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>


</p>
<br />
<br />

<p align="center">
Step 9: Open PowerShell_ise as an administrator create a new File, paste the contents of the pre made script into the file, run the script and observe the accounts being created. 
 Side note: There were error messages due to my script uploading to "_EMPLOYEES" which was non existent due to changing the file name to “_EMPLOYEES_”. 
 I updated the script and finally the usernames started processing  :  
<br/>
<br /
<br />
 


https://user-images.githubusercontent.com/119460677/214143495-f18be381-8b5c-4b3c-9dda-b39b3166903b.mp4


</p>
<br />
<br />
<p align="center">
Step 8: Employees created from Windows PowerShell Ise into the Active Directory
<br />
<br />
<img src= "https://i.imgur.com/RnMixrr.png" height="60%" width="80%" alt="Disk Sanitization Steps"/>
