# Minimum setup

1. Install VS code

Just two commands and ready to go!

```bash
sudo apt update
sudo apt install code

```

2. Configure git

```bash
# ssh keygen
ssh-keygen -t ed25519 -C "your_email@example.com"

# Start ssh agent in the background
eval "$(ssh-agent -s)"

# Create config file
cd ~/.ssh
touch config
```

Create config in ~/.ssh/config

```
Host github.com
  AddKeysToAgent yes
  IdentityFile ~/.ssh/id_ed25519
```

If a passphrase is set

```
Host github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519
```

3. Add public key to Git

Settings -> SSH and GPG keys -> Then add the key by copy & pasting the content in id_ed25519.pub.