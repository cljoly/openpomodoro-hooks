# openpomodoro-hooks

Hooks I use with [open-pomodoro cli][cli]. It is mostly oriented toward a sway/i3 desktop environment and text based programs.

## Features

* silences notifications (do not disturb mode) with [mako][] and [dunst][].
    * also supports an arbitrary script, to integrate with other notification daemons. If `~/.bin/dnd_toggle` is an executable file, it will be run, instead of communicating with mako or dunst.
* make [cmus][] play a song for the duration of the pomodoro (I use [mynoise sounds][mynoise])

[cli]: https://github.com/open-pomodoro/openpomodoro-cli
[mako]: https://wayland.emersion.fr/mako/
[dunst]: https://dunst-project.org/
[cmus]: https://cmus.github.io/
[mynoise]: https://mynoise.net/
