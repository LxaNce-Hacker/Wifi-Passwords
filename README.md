# LxaNce👸🤴
# Pc Wifi-Passwords 
![encryption](https://user-images.githubusercontent.com/96795383/152695189-06253f4a-a95d-42f8-8c6b-152ae1448ada.gif)
# Copy and Run this 👇 script in Powershell as Administrator
# ```(netsh wlan show profiles) | Select-String “\:(.+)$” | %{$name=$_.Matches.Groups[1].Value.Trim(); $_} | %{(netsh wlan show profile name=”$name” key=clear)} | Select-String “Key Content\W+\:(.+)$” | %{$pass=$_.Matches.Groups[1].Value.Trim(); $_} | %{[PSCustomObject]@{ PROFILE_NAME=$name;PASSWORD=$pass }} | Format-Table -AutoSize | Out-File $env:USERPROFILE\Desktop\Log.txt```
