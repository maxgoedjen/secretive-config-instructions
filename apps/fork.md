# Fork

Add this to your `~/.ssh/config` (the path should match the socket path from the setup flow).

```
Host *
	IdentityAgent /Users/$YOUR_USERNAME/Library/Containers/com.maxgoedjen.Secretive.SecretAgent/Data/socket.ssh
```