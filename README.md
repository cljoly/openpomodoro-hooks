# 🪝 Openpomodoro Hooks

Hooks I use with [open-pomodoro cli][cli]. It is mostly oriented toward a sway/i3 desktop environment and text based programs.

## Features

* Silences notifications (do not disturb mode) with [mako][] and [dunst][].
    * Also supports an arbitrary script, to integrate with other notification daemons. If `~/.bin/dnd_toggle` is an executable file, it will be run (passing it `on` or `off`), instead of communicating with mako or dunst.
* Pause and start the current player. If [cmus][] is in use, it will pause and start it instead of any other player.

## Installation

1. Set up the [open-pomodoro cli][install]
2. Drop the [`hooks`][hooks-dir] folder in `~/.pomodoro/hooks/`.

### Optional Dependencies

If the following programs are present, the hook will opportunisticaly start and pause the current music player, mute notifications…

* [playerctl][]
    * if [cmus][] is in use, it will have priority
* [mako][] or [dunst][]

### Automatic Update with Chezmoi (NOT Required)

Chezmoi [external](https://www.chezmoi.io/reference/special-files-and-directories/chezmoiexternal-format/) feature allows you to auto update and manage the hooks, by adding the following to your `~/.local/share/chezmoi/.chezmoiexternal.toml`:

```toml
[".pomodoro/hooks/"]
    type = "archive"
    url = "https://github.com/cljoly/openpomodoro-hooks/archive/refs/heads/main.zip"
    exact = true
    stripComponents = 2
```


[cli]: https://github.com/open-pomodoro/openpomodoro-cli
[mako]: https://wayland.emersion.fr/mako/
[dunst]: https://dunst-project.org/
[cmus]: https://cmus.github.io/
[mynoise]: https://mynoise.net/
[playerctl]: https://github.com/altdesktop/playerctl
[hooks-dir]: https://github.com/cljoly/openpomodoro-hooks/tree/main/hooks
[install]: https://github.com/open-pomodoro/openpomodoro-cli#installation
