# git

## Communicationw with git servers over SSH

Follow the instructions in either [ssh](/apps/ssh.md) or your shell in [shells](/shells).

## Signing Commits

### Required: 

```
git config --global commit.gpgsign true
git config --global user.signingkey $PATH_TO_YOUR_PUBLIC_KEY
git config --global gpg.format ssh
```

### Recommended:

#### Creating and adding to allowed_signers

```
touch ~/.gitallowedsigners
echo $PATH_TO_YOUR_PUBLIC_KEY > ~/.gitallowedsigners
git config --global git config gpg.ssh.allowedSignersFile ~/.gitallowedsigners
```

#### Showing signatures in logs

```
git config --global log.showSignature true
```
