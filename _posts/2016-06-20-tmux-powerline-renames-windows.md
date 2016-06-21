---
layout:     post
title:      Stop powerline from renaming tmux windows
date:       2016-06-20 19:07:48
summary:    Learn how to stop powerline from renaming your tmux windows easily.
categories: powerline tmux hacking
---

I really like [`powerline`](https://github.com/powerline/powerline) and I am
trying to use [`tmux`](https://tmux.github.io/) so that I can switch from
[`screen`](https://www.gnu.org/software/screen/) to `tmux`.
To be frank, I keep trying `tmux` and keep going back to `screen` :)

However one thing that annoys me no end is that every time I rename my windows
based on context, `powerline` comes around and renames them to something
unhelpful.

For example, my typical setup is to rename the first window to `git` since I
use that window primarily for all `git` operations.
The next window is typically called `b/r`, which stands for "build and run".
You get the idea.

So, in order to not let `powerline` update the window name, you need to add the
following lines at the bottom of your .tmux.conf file (typically located at
`"${HOME}/.tmux.conf"`):

```
# Turn off auto-renaming of window panes (by powerline, for example).
set-window-option -g automatic-rename off
set-option -g allow-rename off
```

Have fun tmuxing!
