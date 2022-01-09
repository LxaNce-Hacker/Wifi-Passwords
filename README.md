# LxaNce👸🤴
# Pc Wifi-Passwords 

# Copy and Run this 👇 script in Powershell as Administrator
# ```(netsh wlan show profiles) | Select-String “\:(.+)$” | %{$name=$_.Matches.Groups[1].Value.Trim(); $_} | %{(netsh wlan show profile name=”$name” key=clear)} | Select-String “Key Content\W+\:(.+)$” | %{$pass=$_.Matches.Groups[1].Value.Trim(); $_} | %{[PSCustomObject]@{ PROFILE_NAME=$name;PASSWORD=$pass }} | Format-Table -AutoSize | Out-File $env:USERPROFILE\Desktop\Log.txt```
