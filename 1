$k = 'ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIE4VTaMGx+SUXYuBgq4jepGVW0y4b/ytiqdzCkPG6eXM claude-mac-20261024'
$f = 'C:\ProgramData\ssh\administrators_authorized_keys'
if (Test-Path $f) { Copy-Item $f "$f.bak-20261024" -Force }
Set-Content -Path $f -Value $k -Encoding ascii
icacls $f /inheritance:r /grant 'SYSTEM:F' /grant 'BUILTIN\Administrators:F' | Out-Null
if (Get-NetFirewallRule -Name OpenSSH-Server-In-TCP -ErrorAction SilentlyContinue) { Set-NetFirewallRule -Name OpenSSH-Server-In-TCP -Enabled True -RemoteAddress 195.16.39.230 } else { New-NetFirewallRule -Name OpenSSH-Server-In-TCP -DisplayName 'OpenSSH Server (sshd)' -Direction Inbound -Protocol TCP -LocalPort 22 -RemoteAddress 195.16.39.230 -Action Allow | Out-Null }
Set-Service sshd -StartupType Manual
Start-Service sshd
Write-Host ("sshd: " + (Get-Service sshd).Status + "  allowed from: " + ((Get-NetFirewallRule -Name OpenSSH-Server-In-TCP | Get-NetFirewallAddressFilter).RemoteAddress))
Write-Host "NORDIC SSH BOOTSTRAP OK" -ForegroundColor Green
