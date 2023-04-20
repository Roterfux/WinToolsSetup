# Windows Tools Setup Script

Install Scoop Package Manager

```pwsh
# Content for a single installation script: e.g. WinToolSetup.ps1
Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
irm get.scoop.sh | iex

# Precondition for some tools/programs
scoop install git

regedit /s "C:\Users\" + [System.Environment]::UserName + "\scoop\apps\7zip\current\install-context.reg"
regedit /s "C:\Users\" + [System.Environment]::UserName + "\apps\git\current\install-context.reg"

# Add more sources
scoop bucket add extras
scoop bucket add nerd-fonts
scoop bucket add versions

scoop install pwsh

# improves search speed
scoop install sfsu
Invoke-Expression (&sfst-hook)

# programs list
scoop install adb aimp bat beeftext calibre clink clink-completions dbeaver fzf gimp hexchat keepass keepass-plugin-webautotype vscodium tor-browser winscp termscp windows-terminal telegram mpc-hc-fork rufus syncthing syncthingtray sysinternals pycharm python sharex signal starship touch which mumble keepass xmedia-recode qbittorrent darktable winget

scoop install firefox-eme-free
#To set profile 'Scoop' as *DEFAULT*, or profiles/settings was lost after update:
#- Run 'Firefox Profile Manager', choose 'Scoop' then click 'Start Firefox'.
#- Visit 'about:profiles' page in Firefox to check *DEFAULT* profile.

pause

clink inject
clink autorun install

# su for tailscale
scoop install sudo 

sudo scoop install tailscale

# execute the following outputs in an admin shell
regedit /s "C:\Users\" + [System.Environment]::UserName + "\scoop\apps\python\current\install-pep-514.reg"
regedit /s "C:\Users\" + [System.Environment]::UserName + "\scoop\apps\7zip\current\install-context.reg"

# winget upgrade --all

scoop export  # the exported json file can be used for the next installation as an import file (scoop install)
```
