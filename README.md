# Developing NodeJS applications from Windows deploying to Ubuntu

This is my attempt to do some React development on a low powered Windows PC with up to 14 hours battery life.
Windows shared folders do not work with symlinks so getting code between Windows and the VM is a bit of a pain.
Should be using vagrant


1. Install VirtualBox, git bash
2. Download Ubntu server ISO
3. On Windows run `ssh-keygen`
4. In VirtualBox, create a new virtual machine and attach the ISO as an optical disc
5. Go to settings for created VM and in network, forward ports 3000 to 3000 and 2222 to 22
6. In VirtualBox, Preferences, Network, Create a network
7. Enable [passwordless SSH](https://linuxize.com/post/how-to-setup-passwordless-ssh-login/) by:
8. In `/etc/ssh/sshd_config` ensure these are set

```
PasswordAuthentication no
ChallengeResponseAuthentication no
UsePAM no
AuthorizedKeysFile ssh/authorized_keys .ssh/authorized_keys2
```

9. ssh into server ssh 

