# i3-dots
list of software:
```
yay -S xorg i3 maim xclip ttf-hack-nerd xborders alacritty rofi rofi-emoji polybar brightnessctl feh picom dunst firefox noto-fonts-cjk noto-fonts-emoji starship blesh-git
mate-polkit snixembed
```
(for some reason i need snixembed to show the discord tray icon)

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

cursor theme and gtk theme included

for cursor theme,extract to `~/.icons` and put in `~/.Xresources`:
```
Xcursor.theme = everforest-cursors
```
and add this to `~/.xinitrc`:
```
xrdb ~/.Xresources
```
for gtk theme, extract to `~/.themes` and apply from `lxappearance`
