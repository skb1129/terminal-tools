# Setting up multiple Github accounts

## SSH Keys
Create two SSH RSA keys using:
```bash
ssh-keygen -t rsa -b 4096 -C “your_email@example.com”
```
Then move these keys to **~/.ssh/**.

## Add SSH Keys in Github
Copy the contents of the generated `.pub` (public key) file and paste it in the Github [account settings](https://help.github.com/en/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account).

## Add SSH Configuration
Open **~/.ssh/config** file (Create if doesn't exist) and add the following configuration.
```
# Work Account
Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/work-github
# Personal account
Host me.github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/me-github
```

## Cloning Github Repositories

Now, while cloning new repositories from Github, change the SSH cloning URL respective to the account.
```bash
git clone git@me.github.com:skb1129/terminal-tools.git
```

## Post Cloning

After cloning, you need to set the user yourself in any of the git repositories you clone or create.
```bash
git config user.name "Surya Kant Bansal" && git config user.email suryakantbansal97@gmail.com
```
For easy use, you can create a `alias` for this command in your **~/.bash_profile**