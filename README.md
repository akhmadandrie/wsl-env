## Steps

### Open PowerShell as administrator
```
Start-Process powershell -Verb RunAs
```

#### Enable WSL
```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

#### Enable VM Platform
```
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

#### Update WSL Kernel 
```
wsl --update
```

#### Enable WSL2 & apply the update
```
https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi
```

#### To set v2 as the default version for future installations
```
wsl.exe --set-default-version 2
```

#### To check the WSL mode
```
wsl.exe --list --verbose
```

#### To view a list of available WSL distro
```
wsl.exe --list --online
```

#### To upgrade the Linux distro to v2
```
wsl.exe --set-version <distro name> 2
```

#### Verify the version of the distro
```
wsl.exe --list --verbose
```
