---
layout:     post
title:      Jump over words in tmux using Ctrl+Left/Right
date:       2016-06-20 19:07:48
summary:    Learn how to enable (or disable) jumping over words using Ctrl+Left/Right when using tmux.
categories: tmux productivity shortcuts
---

TL;DR: Add this to your `"${HOME}/.tmux.conf"`:

```
# Bind Ctrl+Left and Ctrl+Right in tmux
set-window-option -g xterm-keys on
```

Long version:

As I mentioned in my previous post, I have been trying to use `tmux` instead of
`screen`.

I routinely use really long command lines, mostly recalled from history. I also
tend to chain multiple commands into one long input string, connected by `&&` or
`;`. I often find myself trying to edit a long command in the middle. Doing this
in `screen` is easy using the `Ctrl+Left`/`Ctrl+Right` key combination because
it is enabled by default.

To enable that with `tmux`, you need to add the following lines at the bottom of
your .tmux.conf file (typically located at `"${HOME}/.tmux.conf"`):

```
# Bind Ctrl+Left and Ctrl+Right in tmux
set-window-option -g xterm-keys on
```

Have fun tmuxing!
