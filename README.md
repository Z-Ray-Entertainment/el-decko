# El Decko
El Decko is a collection of user interfaces, backends and other utilities to make use of Elgato Stream Decks on Linux

## Desing Goals
El Decko aims to be operable rootless and on any (or no) display server.  
Additionally El Decko tries to embrace the Unix philosophy "Do one thing and do it well" as good as it can. Which is the main reason why the entire El Decko ecosystem is split among so many different projects.  

With this come new challenges but also advantages.  
The main challenge currently lies in the keystroke backend as someone can not emulate keyboard press with out super user access on Linux unless we would make use of xdotool.  
Which on the other hand would break with the display server agnostic design goal.  
One solution might be to provide some kind of an el-decko-service or trying to send keyboards instructions via dbus.  

The major advantage is that El Decko is very modular and it is relatively easy to supply custom backends.  
In return the install size can also be tailored to ones need.

## Available UIs
### GTK4
The GTK4 user interface is currently under heavy development and not really usable except for launching, stopping and reloading ed-core.  
Repository: https://github.com/Z-Ray-Entertainment/el_decko_ui_gtk4

## Available Backends
### OBS Studio Websocket
Repository: https://github.com/Z-Ray-Entertainment/el_decko_backend_obs_ws

### MPRIS 2 via dbus
Repository: https://github.com/Z-Ray-Entertainment/el_decko_backend_mpris
  
## Planed UIs
### Qt6
The developemtn of the Qt6 user interface has not yet be started but is on our roadmap.  
Repository: https://github.com/Z-Ray-Entertainment/el_decko_ui_qt6

## Planed Backends
#### Keystroke
  - Rootless emulation of keyboard shortcut and button press
  
## Dropped backends / UIs
### TUI (Terminal user interface)
The TUI was originally planed as a standalone terminal based interface but was dropped as the core of El Decko (ed-core) can be run as a standalone application already.  
All configurations are stored as well formed JSON files allowing for easy readability and shouldn't be very difficult to be added by hand.  
As users usually asking for TUIs are also most likely users not wanting too much bloat on their systems they probably won't install an additional interface if they could just use vim and launch ed-core by hand.
