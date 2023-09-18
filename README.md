# Windows post installation applications/settings

### This repository I made for myself, but maybe you can find something new for yourself

> ## Download apps using **winget**
>> ```ps1
>>winget install --id=Nvidia.GeForceExperience -s winget ; winget install --id=Nvidia.Broadcast -s winget ; winget install --id=Rainmeter.Rainmeter -s winget ; winget install --id=Valve.Steam -s winget ; winget install --id=EpicGames.EpicGamesLauncher -s winget ; winget install --id=Discord.Discord -s winget ; winget install --id=Telegram.TelegramDesktop -s winget ; winget install --id=Skillbrains.Lightshot -s winget ; winget install --id=JetBrains.Toolbox -s winget ; winget install --id=Git.Git -s winget ; winget install --id=GitHub.GitHubDesktop -s winget ; winget install --id=JanDeDobbeleer.OhMyPosh -s winget ; winget install --id=Spotify.Spotify -s winget ; winget install --id=Logitech.GHUB -s winget ; winget install --id=OBSProject.OBSStudio -s winget ; winget install --id=Microsoft.VisualStudioCode -s winget ; winget install --id=Python.Python.3.12 -s winget ; winget install --id=Oracle.JDK.17 -s winget ; winget install --id=9PF4KZ2VN4W9 -s msstore ; winget install --id=9MTFTXSJ9M7F -s msstore
>> ```
>> If you have errors during installation, check the region settings. Applications may not be installed if, for example, the "World" region is set.

> ## Apps to be installed:
>> **NVIDIA GeForce Experience, NVIDIA Broadcast, Rainmeter, Steam, Epic Games Launcher, Discord, Telegram, Lightshot, JetBrains Toolbox, Git, GitHub Desktop,  OhMyPosh, Spotify, Logitech GHUB, OBS, VSCode, Python 3.12, JDK 17, TranslucentTB, RoundedTB**

> ## Desktop
>> ### Hide desktop icons - ✅
>> ### RoundedTB
>>> * **My settings**  
>>> ![image](https://github.com/magicman517/windows-post-installation/assets/64162075/d3ba8c25-05c0-488b-9eaf-81f5a602f775)
>> ### Rainmeter
>>> * Unload default skins
>>> * Download archive from the [**Releases**](https://github.com/magicman517/windows-post-installation/releases) section
>>> * Install fonts
>>> * Copy **Date** folder to **/Documents/Rainmeter/Skins/**
>>> * In **Rainmeter** refresh all skins
>>> * Load **Date skin.ini**
>>> * Set position to **On desktop**
> ## My result
> ##### [Wallpaper from this screenshot](https://steamcommunity.com/sharedfiles/filedetails/?id=2483685763)  
> ![image](https://github.com/magicman517/windows-post-installation/assets/64162075/b868684c-41e1-42e9-b877-e3a8cf1722f8)

> ## Debloat
>> I always use [ShutUp10](https://www.oo-software.com/en/shutup10)
>> You can install it using **winget**
>> ```ps1
>> winget install OO-Software.ShutUp10 -s winget
>> ```

> ## Disable UAC, Firewall
> ## Do this only if you understand the risks. You are liable for the outcome!
>> ### Disable **UAC**
>> ### Run the **Terminal (PowerShell)** with administrator privileges.
>> ### Run this command  
>> ```ps1
>> Set-ItemProperty -Path "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System" -Name "ConsentPromptBehaviorAdmin" -Value 0
>> ```
>>
>> ### Disable **Windows Firewall**
>> ### Run the **Terminal (PowerShell)** with administrator privileges
>> ### Run this command
>> ```ps1
>> Set-NetFirewallProfile -All -Enabled False
>> ```

> ## Perfomance
>> ### Disable **background apps**
>> ### Run the **Terminal (PowerShell)** with administrator privileges
>> ### Run this command  
>> ```ps1
>> Reg Add HKCU\Software\Microsoft\Windows\CurrentVersion\BackgroundAccessApplications /v GlobalUserDisabled /t REG_DWORD /d 1 /f
>> ```
>>
>> ### NVIDIA Control Panel
>> #### Configure the following in the **3D Settings -> Manage 3D Settings** page:
>> * Anisotropic filtering - Off
>> * Antialiasing - Gamma Correction - Off
>> * Low Latency Mode - On (this setting limits pre-rendered frames to 1)
>> * Power management mode - Prefer maximum perfomance
>> * Shader Cache Size - Unlimited
>> * Texture filtering - Quality - High perfomance
>> * Threaded Optimization - If you are CPU bottlenecked, choose the **Off** option
>> * Vertical sync - Off
>> 
>> #### Configure **explorer** and **dwm**
>> #### Go to **Manage 3D settings -> Program Settings -> Add -> Browse**
>> #### **Open the local disk on which Windows is installed/Windows/explorer**  
>> ![image](https://github.com/magicman517/windows-post-installation/assets/64162075/3aff284f-47b3-4f93-8ba9-53cc71daa190)
>> #### Set **Power management mode** - Prefer maximum perfomance
>>
>> #### Again click **Add -> Browse**
>> #### **Open the local disk on which Windows is installed/Windows/System32/dwm.exe**  
>> ![image](https://github.com/magicman517/windows-post-installation/assets/64162075/182dbfd4-78c2-4e9d-9a47-a142baa38180)
>> #### Set **Power management mode** - Prefer maximum perfomance
