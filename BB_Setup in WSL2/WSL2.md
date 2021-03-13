1. INSTALL WSL 2

RUN POWERSHELL as administrator

⚙️ Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

RESTART POWERSHELL and RUN cmd in powershell

⚙️ dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

⚙️ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

RESTART POWERSHELL and RUN cmd in powershell

SET DEFAULT TO WSL 2
⚙️ wsl --set-default-version 2 	(Type this in adminstrator mode powershell)

DOWNLOAD & INSTALL UBANTU 
Download Linux Kernel: https://aka.ms/wsl2kernel​
go to search 
type Ubantu 20.04 Linux & open. it'll take few minutes.
then it'll ask for username & Password.

CHECK VERSION 
⚙️ wsl --list --verbose   (Type this in powershell)
⚙️ cat /etc/os-release	  (Type this in Ubantu)

------------------------------------------
⚙️ sudo apt-get update && sudo apt-get upgrade
⚙️ sudo apt update && sudo apt install git
⚙️ wsl -l -v
⚙️ lsb_release -a        (Type this in Ubantu)
⚙️ exit 			            //to logout

⚙️ wsl --help            //Type this in adminstrator mode powershell
Note: You're installing WSL2 in Powershell not in Ubantu.
-------------------------------------------------
