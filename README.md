# Windows Tools Setup Script

Install Scoop Package Manager

```pwsh
# Content for a single installation script: e.g. WinToolSetup.ps1
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

scoop install firefox python vscodium tor-browser winscp git adb windows-terminal pwsh qtorrent discord telegram mpc-hc-fork rufus syncthing syncthingtray pycharm dbeaver 7zip gimp tailscale calibre fzf sharex aimp singal mumble keepass fzf dbeaver hexchat openssh

scoop export  # the exported json file can be used for the next installation as an import file (scoop install)
```
