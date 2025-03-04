# dotFiles


## Additional setup to be made for sway / wayland to work

### 1. Setup correctly /etc/environment

To work with display managers such as lemurs the shell used by lemurs or in this
case global environment shall be setup to setup correct env var for wayland to
work.

Note: tested with GDK_BACKEND=x11 and sway run but waybar and wofi won't.

Current setup : 

```
GDK_BACKEND=wayland
QT_QPA_PLATFORM=wayland-egl
CLUTTER_BACKEND=wayland
SDL_VIDEODRIVER=wayland
ECORE_EVAS_ENGINE=wayland_egl
ELM_ENGINE=wayland_egl
ELM_DISPLAY=wl
ELM_ACCES=gl # or gl for hardware accelarated

_JAVA_AWT_WM_NONREPARENTING=1
```

