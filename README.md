# i3-dots
list of software:
```
paru -S xorg i3 maim xclip ttf-hack-nerd xborders alacritty rofi rofi-emoji polybar brightnessctl feh picom dunst firefox noto-fonts-cjk noto-fonts-emoji starship blesh-git
mate-polkit snixembed
```
(for some reason i need `snixembed` to show the discord tray icon)

symlink this folder to `~/.config`

to enable touchpad, make a new file at `/etc/X11/xorg.conf.d/touchpad-tap.conf` and put this:
```
Section "InputClass"
        Identifier "libinput touchpad catchall"
        MatchIsTouchpad "on"
        MatchDevicePath "/dev/input/event*"
        Driver "libinput"
        Option "Tapping" "on"
EndSection
```
audio server: `pulseaudio`

select `xorg` and `intel` in `archinstall`

`discord` and `spotify` work out of the box since it's X :]

`lxappearance-gtk3` for setting gtk2 and gtk3 theme

for display manager i recommend `ly`

gtk theme: [here](https://github.com/Fausto-Korpsvart/Catppuccin-GTK-Theme)

qt theme:
```
paru -S kvantum-theme-catppuccin-git
```

cursors:
```
curl -OL https://github.com/catppuccin/cursors/releases/download/v2.0.0/catppuccin-mocha-maroon-cursors.zip
```
for cursor theme,extract to `~/.icons` and put in `~/.Xresources`:
```
Xcursor.theme = catppuccin-mocha-maroon-cursors
```
and add this to `~/.xinitrc`:
```
xrandr
xrdb -merge ~/.Xresources
exec i3
```
for gtk theme, extract to `~/.themes`

## how to make Persona 4 Golden work
download `klite.verb`
```
curl -OL https://raw.githubusercontent.com/GloriousEggroll/protonfixes/refs/heads/master/verbs/klite.verb
```
then execute this:
```
winetricks dxvk d3dx11_43 d3dcompiler_43 xact klite.verb wmp9 devenum quartz
```
After that persona 4 golden should work
