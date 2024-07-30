## Setting Up SSH Key for Github

**1. Navigate to your terminal and input the command:**
```sh
ssh-keygen -t ed25519 -C "your_email@example.com"
```

**2. Response will output:**
```
➞  ssh-keygen -t ed25519 -C "your_email@example.com"
Generating public/private ed25519 key pair.
Enter file in which to save the key (/Users/username/.ssh/id_ed25519):
```

**3. Press `Enter` to save in the current directory.**

**4. It will then ask for a passphrase:**
- It is your choice whether or not you want to enter a passphrase.
- If you enter a passphrase, you will have to enter it every time you use your SSH key.

**5. Repeat that step (re-enter passphrase).**

**6. **Your identification has been saved** should come up.**

**7. Enter the command:**
```sh
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

**8. Follow the output, enter the command:**
```sh
pbcopy < ~/.ssh/id_ed25519.pub
```

**9.**
- Go to GitHub and navigate to **Settings > SSH and GPG keys > New SSH key**.
- Paste the key into the “Key” field and give it a recognizable title.

**10. Select **"Add Key"**.**

**11. Test Your SSH Connection to GitHub with the command:**
```sh
ssh -T git@github.com
```

**12. You should get a response similar to:**
```
Hi "username"! You've successfully authenticated, but GitHub does not provide shell access.
```

**13. Complete. You can now start using your git commands.**