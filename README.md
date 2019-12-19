# lattepanda
The strongest single board computer

# Install OpenSSH server

## download package
https://github.com/PowerShell/Win32-OpenSSH/releases/download/v8.1.0.0p1-Beta/OpenSSH-Win64.zip

## unzip package
c:\tools\OpenSSH-Win64

## add path to environment
PATH
;C:\tools\OpenSSH-Win64

## install ssh service with powershell
- Open PowerShell command prompt by administrator
- cd c:\tools\OpenSSH-Win64
- sshd install

# change the setting
- c:\ProgramData\ssh\sshd_config
- RSAAuthentication yes
- PubkeyAuthentication yes
- AuthorizedKeysFile .ssh/authorized_keys

# auto start service

PowerShell
- Set-Service -Name sshd -StartupType 'Automatic'

# change firewall
PowerShell
- New-NetFirewallRule -Name sshd -DisplayName 'OpenSSH Server (sshd)' -Enabled True -Direction Inbound -Protocol TCP -Action Allow -LocalPort 22

or 
- netsh advfirewall firewall add rule name="sshd" dir=in action=allow protocol=TCP localport=22


