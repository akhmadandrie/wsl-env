## Steps

#### Open PowerShell as administrator
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
wsl.exe --update
```

#### To set v2 as the default version for future installations
```
wsl.exe --set-default-version 2
```

#### To view a list of available WSL distro
```
wsl.exe --list --online
```

#### Install available WSL distro
```
wsl.exe --install -d DISTRO-NAME
```

#### To upgrade the Linux distro to v2
```
wsl.exe --set-version <DISTRO-NAME> 2
```

#### Verify the version of the distro
```
wsl.exe --list --verbose
```

#### Troubleshooting
```
wsl.exe --unregister DISTRO-NAME
```

For further details, see [here](https://github.com/microsoft/WSL) and [here](https://github.com/MicrosoftDocs/wsl/blob/main/WSL/troubleshooting.md).
