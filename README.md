# i3-dots
list of software:
```
yay -S xorg i3 maim xclip ttf-hack-nerd xborders alacritty rofi rofi-emoji polybar brightnessctl feh picom dunst firefox noto-fonts-cjk noto-fonts-emoji starship blesh-git
```
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
