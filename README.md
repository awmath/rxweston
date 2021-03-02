# rxweston
rxweston is a simple bash script to run any application under a rootful Xwayland session.
This is useful for applications which otherwise aren't able to correctly capture the screen content.

# explanation
This script first starts a blank weston display server, either as a nested instance inside another wayland/X11 session or as a seperate wayland session when running from an empty VT. Afterwards it starts a fullscreen rootful Xwayland server inside which the choosen application is started.

All weston command line parameters are supported. For example to run a specific resolution for an application:
```
rxweston --width=1280 --height=800 -- xeyes
```


# "roadmap"
- switch to the weston kiosk shell as soon as it is supported (aka as soon as weston 9.0.0 hits fedora)
- enable headless hardware accelerated mode

# Examples
## Steam Remote Play ##
`rxweston -- steam`
