- INSTALL WSL 2

- RUN POWERSHELL as administrator

⚙️ Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux

- RESTART POWERSHELL and RUN cmd in powershell

⚙️ dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart

⚙️ dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart

- RESTART POWERSHELL and RUN cmd in powershell

- SET DEFAULT TO WSL 2
⚙️ wsl --set-default-version 2 	(Type this in adminstrator mode powershell)

- DOWNLOAD & INSTALL UBANTU 
Download Linux Kernel: https://aka.ms/wsl2kernel​
go to search 
type Ubantu 20.04 Linux & open. it'll take few minutes.
then it'll ask for username & Password.

- CHECK VERSION 
⚙️ wsl --list --verbose   (Type this in powershell)
⚙️ cat /etc/os-release	  (Type this in Ubantu)

------------------------------------------
⚙️ sudo apt-get update && sudo apt-get upgrade
⚙️ sudo apt update && sudo apt install git
⚙️ wsl -l -v
⚙️ lsb_release -a        (Type this in Ubantu)
⚙️ exit 			            //to logout

⚙️ wsl --help            //Type this in adminstrator mode powershell

- Note: 
- 1. You're installing WSL2 in Powershell not in Ubantu.
- 2. Type "cd /mnt" t get access to Window system and cd to go back to UBANTU
-------------------------------------------------

- Ubantu GUI (Ref: https://www.youtube.com/watch?v=IL7Jd9rjgrM)

Open Remote Desktop Connection(RDC)
Enter 	localhost:3390

Username :	 --------
password :	 --------

-------------------------------------------------
-  REF:
Video 1 - Install Windows Subsystem for Linux, Ubuntu 20.04 LTS and Python using ASDF https://youtu.be/CLPwhoTITow​
Video 2 - Using VSCode with Ubuntu https://www.youtube.com/watch?v=CTlTB...​ 
Video 3 (this) - Using Windows Terminal//

- To INSTALL Python, pip, and venv in UBANTU you need to isntall ASDF
⚙️ git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.8.0
⚙️ nano ~/.bashrc
⚙️ asdf plugin-add python
⚙️ asdf      // Type asdf to verify Installation
 
⚙️ sudo apt-get update; sudo apt-get install --no-install-recommends make build-essential libssl-dev zlib1g-dev libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-devsudo
 
⚙️ asdf install python latest or python -v       //To  verify Installation
⚙️  asdf global python 3.9.2                     //Set python as global variable

⚙️ python3 --version       //To check python installations
⚙️ sudo apt update && sudo apt upgrade, then update Python using 
⚙️ sudo apt upgrade python3.
⚙️ sudo apt install python3-pip
⚙️ sudo apt install python3-venv

- Note:
1. Install virtual stdio code
//VS Code is also available for Linux, but Windows Subsystem for Linux does not support GUI apps, so we need to install it on Windows. Not to worry, you'll still be able to integrate with your Linux command line and tools using the Remote - WSL Extension.//
2. Add WSL extention
Close it.

Now open UBANTU 20.4 terminal and make a directory 📂
⚙️ mkdir Project1
⚙️ cd Project1
//open downloaded or saved project from this file//
code .

Inside Visual stdio code open new terminal(ctrl + shift + `) and type  
⚙️ python3 -m venv .venv
⚙️ source .venv/bin/activate

#Open a WSL - Remote window
Open your project folder in VS Code from your Ubuntu terminal by entering: 
⚙️ code .             (the "." tells VS Code to open the current folder).

//After finish your work in Virtual Stdio Code Type "deactivate" to deactivate .venv. 

//An important thing to remember when using Windows Subsystem for Linux (WSL) is that you are now working between two different file systems: 
1) your Windows file system, (/mnt/c/)
and 2) your Linux file system (WSL), which is Ubuntu.(~)//


In case you need help with PIP(Just follow video1,2,3 and you'll be fine)
How to install pip in WSL ? Intall pip - Command 'pip' not found in WSL
Ref: https://www.youtube.com/watch?v=mfIRe_NMHsY

