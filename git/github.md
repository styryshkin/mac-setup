# Authenticating with GitHub from Git

## Connecting over SSH

If you clone with SSH, you must generate SSH keys on each computer you use to push or pull from GitHub.

SSH URLs provide access to a Git repository via SSH, a secure protocol. To use these URLs, you must generate an SSH keypair on your computer and add the public key to your GitHub account.

When you `git clone`, `git fetch`, `git pull`, or `git push` to a remote repository using SSH URLs, you'll be prompted for a password and must provide your SSH key passphrase.

### Generating a new SSH key

1. Create a new ssh key, using the provided email as a label.

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
```

2. When you're prompted to "Enter a file in which to save the key," press Enter. This accepts the default file location.

```
Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]
```

3. At the prompt, type a secure passphrase.

```
Enter passphrase (empty for no passphrase): [Type a passphrase]
Enter same passphrase again: [Type passphrase again]
```

### Adding your SSH key to the ssh-agent

When adding your SSH key to the agent, use the default macOS `ssh-add` command, and not an application installed by macports, homebrew, or some other external source.

1. Start the ssh-agent in the background.

```
$ eval "$(ssh-agent -s)"
Agent pid 59566
```

2. If you're using macOS Sierra 10.12.2 or later, you will need to modify your `~/.ssh/config` file to automatically load keys into the ssh-agent and store passphrases in your keychain.

```
Host *
 AddKeysToAgent yes
 UseKeychain yes
 IdentityFile ~/.ssh/id_rsa
```

3. Add your SSH private key to the ssh-agent and store your passphrase in the keychain. If you created your key with a different name, or if you are adding an existing key that has a different name, replace id_rsa in the command with the name of your private key file.

```
ssh-add -K ~/.ssh/id_rsa
```

### Adding a new SSH key to your GitHub account

To configure your GitHub account to use your new (or existing) SSH key, you'll also need to add it to your GitHub account.

1. Copy the SSH key to your clipboard.

```
$ pbcopy < ~/.ssh/id_rsa.pub
# Copies the contents of the id_rsa.pub file to your clipboard
```

2. In the upper-right corner of any page, click your profile photo, then click `Settings`.
3. In the user settings sidebar, click `SSH and GPG keys`.
4. Click `New SSH key` or `Add SSH key`.
5. In the "Title" field, add a descriptive label for the new key. For example, if you're using a personal Mac, you might call this key "Personal MacBook Air".
6. Paste your key into the "Key" field.
7. Click `Add SSH key`.
8. If prompted, confirm your GitHub password.
