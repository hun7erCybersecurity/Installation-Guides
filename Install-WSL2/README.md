[<img src='https://cdn.pixabay.com/photo/2011/08/14/18/08/penguin-8640__340.png' alt='LinuxLogo' height='120'>](https://github.com/hun7erCybersecurity)




# Install-WSL 2
## Here you will find how you install WSL2 on a Windows operating system.

###  My Source

* [Lern Mircrosoft (Install Manual)](https://learn.microsoft.com/en-us/windows/wsl/install-manual)
* [Lern Mircrosoft (Basic Commands)](https://learn.microsoft.com/en-us/windows/wsl/basic-commands#install-a-specific-linux-distribution)
* [Freecodecamp](https://www.freecodecamp.org/news/how-to-install-wsl2-windows-subsystem-for-linux-2-on-windows-10/)



## Install WSL 2 with Powershell step by step:
* Enable Windows features for WSL 
* Check requirements for running WSL 2
* Download and Install the Linux kernel update package
* Set WSL 2 as your default version
* Install your Linux distribution of choice
* Set Username and Password of the machine


## Enable Windows features for WSL:

1. Start your Powershell as Administrator.

<br />

2. Copy, insert and Execute these commands line by line:

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux, VirtualMachinePlatform -All -NoRestart

Restart-Computer

```
<br />

3. After the reboot of your system, check with these commands if the state of the Optional features are "Enabled":

```powershell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux | Select-Object State

Get-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform | Select-Object State
```
<br />

## Check requirements for running WSL 2:

1. To update to WSL 2, you must be running Windows 10

   * For x64 systems: Version 1903 or later, with Build 18362 or later.
   * For ARM64 systems: Version 2004 or later, with Build 19041 or later.
   
<br/>

2. Copy and execute this command to check your Version of the running Opertatingsystem

```powershell   
Get-WmiObject Win32_OperatingSystem | Select PSComputerName, Caption, OSArchitecture, Version, BuildNumber | FL
```
<br/>

## Download and Install the Linux kernel update package:
1. Download the latest package:

    * [WSL2 Linux kernel update package for x64 machines](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)

<br/>
 
2. Install the Linux kernel update package:

    * follow the installation wizard

<br/>

## Set WSL 2 as your default version

1. Start your Powershell as Administrator.

<br />

2. Copy, insert and Execute these commands line by line:

```powershell
wsl --set-default-version 2
```
<br/>

## Find and Install your Linux distribution of choice

1. Start your Powershell as Administrator.

<br/>

2. Find your Linux Distribution with this command:
```powershell
wsl -l -o
```
<br/>

3. Install your Distribution of choice:

```powershell
wsl --install -d <Distribution-NAME>
```
<br/>

## Set Username and Password of the machine

1. Choice a username for your machine, if you see the folloing text:

```notepad
Installing, this may take a few minutes...
Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: 
```
<br/>

2. Choice a password for your machine, if you see the folloing text:
```notepad
Installing, this may take a few minutes...
Please create a default UNIX user account. The username does not need to match your Windows username.
For more information visit: https://aka.ms/wslusers
Enter new UNIX username: <your username>
New password:
```
<br/>

3. Retype your password.

# Done


