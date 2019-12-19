# lattepanda
The strongest single board computer

# Install OpenSSH server

## download package
https://github.com/PowerShell/Win32-OpenSSH/releases/download/v8.1.0.0p1-Beta/OpenSSH-Win64.zip

## unzip paccage
c:\tools\OpenSSH-Win64

## add path to environment
PATH
;C:\tools\OpenSSH-Win64

## install ssh service with powershell
- Open PowerShell command prompt by administrator
- cd c:\tools\OpenSSH-Win64
- install.pl

# change the setting
c:\ProgramData\ssh\sshd_config
RSAAuthentication yes
PubkeyAuthentication yes
AuthorizedKeysFile .ssh/authorized_keys

# auto start service
