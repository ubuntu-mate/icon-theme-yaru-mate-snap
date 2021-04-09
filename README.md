# Yaru MATE icon theme snap

[![icon-theme-yaru-mate](https://snapcraft.io/icon-theme-yaru-mate/badge.svg)](https://snapcraft.io/icon-theme-yaru-mate)
[![icon-theme-yaru-mate](https://snapcraft.io/icon-theme-yaru-mate/trending.svg?name=0)](https://snapcraft.io/icon-theme-yaru-mate)

[Yaru MATE](https://github.com/ubuntu/yaru) is the default GTK theme for Ubuntu MATE 21.04 and newer.

## Install

[![Get it from the Snap Store](https://snapcraft.io/static/images/badges/en/snap-store-black.svg)](https://snapcraft.io/icon-theme-yaru-mate)

```
snap install gtk-theme-yaru-mate
snap install icon-theme-yaru-mate
```

To connect the theme to a snapped application, you can run:

```
sudo snap connect [other snap]:gtk-3-themes gtk-theme-yaru-mate:gtk-3-themes
sudo snap connect [other snap]:gtk-2-themes gtk-theme-yaru-mate:gtk-2-themes
sudo snap connect [other snap]:icon-themes icon-theme-yaru-mate:icon-themes
```

Or, you can connect the Yaru MATE snapped theme to all snapped apps that support theme plugs:

```
for PLUG in $(snap connections | grep gtk-common-themes:gtk-3-themes | awk '{print $2}'); do sudo snap connect ${PLUG} gtk-theme-yaru-mate:gtk-3-themes; done
for PLUG in $(snap connections | grep gtk-common-themes:gtk-2-themes | awk '{print $2}'); do sudo snap connect ${PLUG} gtk-theme-yaru-mate:gtk-2-themes; done
for PLUG in $(snap connections | grep gtk-common-themes:icon-themes | awk '{print $2}'); do sudo snap connect ${PLUG} icon-theme-yaru-mate:icon-themes; done
```

An official snap built with ❤︎ by the Ubuntu MATE team using configuration at
<https://github.com/ubuntu-mate/gtk-theme-yaru-mate-snap> and the Yaru theme from the upstream project source <https://github.com/ubuntu/yaru>.
