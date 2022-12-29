# 🪝 Openpomodoro Hooks

Hooks I use with [open-pomodoro cli][cli]. It is mostly oriented toward a sway/i3 desktop environment and text based programs.

## Optional Dependencies

If the following programs are present, the hook will opportunisticaly start and pause the current music player, mute notifications…

* [playerctl][]
    * if [cmus][] is in use, it will have priority
* [mako][] or [dunst][]

## Features

* silences notifications (do not disturb mode) with [mako][] and [dunst][].
    * also supports an arbitrary script, to integrate with other notification daemons. If `~/.bin/dnd_toggle` is an executable file, it will be run, instead of communicating with mako or dunst.
* make [cmus][] play a song for the duration of the pomodoro (I use [mynoise sounds][mynoise]). If thi

[cli]: https://github.com/open-pomodoro/openpomodoro-cli
[mako]: https://wayland.emersion.fr/mako/
[dunst]: https://dunst-project.org/
[cmus]: https://cmus.github.io/
[mynoise]: https://mynoise.net/
[playerctl]: https://github.com/altdesktop/playerctl
