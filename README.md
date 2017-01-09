### fpo-kinit

1. Copy these fines in `~/.config/systemd/user/`
+ Change the `user` (before the @) in `kinit-fedora.service`
+ `sudo dnf install kwalletcli`
+ `kwalletcli -f Passwords -e <user>@FEDORAPROJECT.ORG -p '<password>'`
+ `systemctl --user daemon-reload`
+ `systemctl --user enable --now kinit-fedora.timer kinit-refresh.timer`

Note: You can add the password separately to kwallet, or make sure to clear your bash history, as the password will be stored in `~/.bash_history` if you're not careful.
