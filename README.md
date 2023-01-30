# Windows Tools Setup Script

Install Scoop Package Manager

```pwsh
# Content for a single installation script: e.g. WinToolSetup.ps1
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

scoop install git

scoop bucket add extras
scoop bucket add nerd-fonts
scoop bucket add versions

scoop install sfsu
Invoke-Expression (&sfst-hook)

scoop install 7zip adb aimp beeftext calibre clink clink-completions dbeaver discord firefox fzf gimp hexchat python vscodium tor-browser winscp windows-terminal pwsh telegram mpc-hc-fork rufus syncthing syncthingtray pycharm sharex signal mumble keepass xmedia-recode quicklook qbittorrent librehardwaremonitor darktable winget  

scoop install sudo 

sudo scoop install tailscale

# execute the following output
"C:\Users\" + [System.Environment]::UserName + "\scoop\apps\python\current\install-pep-514.reg"

#winget upgrade --all

scoop export  # the exported json file can be used for the next installation as an import file (scoop install)
```
