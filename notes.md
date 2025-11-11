---
generator: CherryTree
title: Startup-Folder
---

<div class="page">

# Startup-Folder

  

# Startup-Folder

- This is whereby an attacker implants a malicious exeutable in the
  startup folder, thereby ensuring that the malware trojan is launched
  by default as the logon on user upon every boot
- The location of the startup folder is usually as shown below on most
  Windows OS
  - - <span style="color:#071ba3;">"%APPDATA%\Microsoft\Windows\Start
      Menu\Programs\Startup"</span>
    - By default this folder is accessible and can be written to by any
      user including non admins

### Abuse

- To set this persistence we simply need only copy our malicious binary
  to the Startup folder using the command below from either a medium or
  high integrity terminal process
  - - <span style="color:#071ba3;">copy C:\Path\To\Malware.exe
      "%APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup"</span> →
      Setup
    - <span style="color:#071ba3;">del
      "%APPDATA%\Microsoft\Windows\Start
      Menu\Programs\Startup\Malware.exe"</span> → Removal

![](images/4-1.png)

</div>
