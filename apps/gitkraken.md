# GitKraken

Add this to `~/Library/LaunchAgents/com.maxgoedjen.Secretive.SecretAgent.plist`

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <key>Label</key>
  <string>link-ssh-auth-sock</string>
  <key>ProgramArguments</key>
  <array>
	<string>/bin/sh</string>
	<string>-c</string>
	<string>/bin/ln -sf $HOME/Library/Containers/com.maxgoedjen.Secretive.SecretAgent/Data/socket.ssh $SSH_AUTH_SOCK</string>
  </array>
  <key>RunAtLoad</key>
  <true/>
</dict>
</plist>
```

Log out and log in again before launching Gitkraken. Then enable "Use local SSH agent in GitKraken Preferences (Located under Preferences -> SSH)
