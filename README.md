# bluetooth-profile-switch
Switch audio profile for active bluetooth audio device

## Synopsys
When a Bluetooth audio device is connected, bt-profile-switch can switch between headset/handsfree modes.
For convenience (I often get confudes by the two names), the properties 'talk' and 'music are used here. Where
talk being the two-way (with mic) low-quality audio and music as on-way HiFi.
The default audio output device will be configured. When that default audio output device is not a bluetooth device,
the script will end without action.

## Dependencies
- bash
- libnotify (optional, bundled with Gnome)
- pulseaudio/pipewire-pulse (as long as pactl is installed)
- bluetooth stack
- jq (command-line JSON parser)

## Instructions

Usage: bt-profile-switch [-v] [-m <mode>] [-n] [-h]
  
Parameters:
    -v  Verbose output (shows names and addresses of devices)
    -m  Change mode (profile) to music (a2dp-sink), or talk (headset-head-unit)
    -n  Send notifications to Gnome-Shell, using notify-send
    -h  Show this help and exit immediately
  
  Note: When mode '-m' is omitted, the profile will swich between the two modes
