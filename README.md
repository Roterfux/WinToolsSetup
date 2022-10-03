# Windows Tools Setup Script

Install Scoop Package Manager
```pwsh
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

scoop install firefox python vscode tor-browser winscp git adb windows-terminal pwsh qtorrent discord telegram mpc-hc-fork rufus syncthing syncthingtray pycharm dbeaver 7zip gimp tailscale calibre fzf sharex aimp singal mumble keepass

scoop export  # the exported json file can be used for the next installation as an import file (scoop install)
```
