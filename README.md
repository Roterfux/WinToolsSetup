# Windows Tools Setup Script

Install Scoop Package Manager

```pwsh
# Content for a single installation script: e.g. WinToolSetup.ps1
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

scoop bucket add extras
scoop bucket add nerd-fonts
scoop bucket add versions

scoop install 7zip adb aimp calibre dbeaver discord firefox fzf gimp git hexchat python vscodium tor-browser winscp windows-terminal pwsh qtorrent telegram mpc-hc-fork rufus syncthing syncthingtray pycharm tailscale sharex singal sysinternals mumble keepass penssh xmedia-recode quicklook qbittorrent

scoop export  # the exported json file can be used for the next installation as an import file (scoop install)
```
