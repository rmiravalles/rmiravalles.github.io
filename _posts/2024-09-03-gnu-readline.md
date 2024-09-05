---
layout: post
title: "The GNU readline"
---
# Keep your hands on the keyboard at all times!

Hello, and welcome to another micro article. These are bits of useful information I gather here and there.

This one's about the **GNU Readline**.This is a library that, I guess, comes with every Linux distribution.

This library provides powerful in-line editing capabilities when you're in your command line. You've been using it all the time, and maybe wasn't aware of it. I wasn't aware that many of these ubiquitous shortcuts, like the **TAB autocompletion** were part of this library. Bash uses the Readline, but not just it. Other REPLs use it too, like the Python REPL.

Using these handy shortcuts will make you a lot faster. You don't need to go looking for your arrow keys on the keyboard.

If you're feeling audacious, you can create your own keybindings and shortcuts by adding them to the `inputrc` file.Mine is in `/etc/inputrc`. You can find it also in your Home directory, here: `~/.inputrc`. Mine wasn't there.

# Keyboard shortcuts

Some super useful shortcuts. There are many more.

| Keystroke | Action          |
| --------- | --------------- |
| Ctrl+F    | Go forward one character |
| Ctrl+B    | Go backward one character |
| Alt+F     | Go forward one word |
| Alt+B     | Go backward one word |
| Ctrl+A    | Go to the beginning of the current line |
| Ctrl+E    | Go to the end of the current line |
| Ctrl+L    | Clear the screen (the same as typing clear) |
| Ctrl+P    | Move backwards in the command history (the same as the up arrow) |
| Ctrl+N    | Move forward in the command history |
| Ctrl+W    | Delete the word that's behind the cursor |
| Ctrl+U    | Delete the entire line |

If you want to look for more shortcuts, look no further than the command line itself. The `Bash` manual page lists them. Type `man bash` to go the manual page. Once inside, hit the `/` to activate the search function, and type `commands for moving`. While you're in there, it's not a bad idea to read this manual. You'll learn a lot!

# Ctrl+R reverse search

Now this one is awesome!

`Ctrl+R` will let you search for previous commands based on keywords. You type the keyword and it will show you the previous command you ran with that keyword. Hit `Ctrl+R` again and it will show you the previous one. Keep hitting `Ctrl+R` until you find the one you were looking for.

Here, I'm searching for a `kubectl` command I ran in the past.

![Ctrl+R](../assets/images/ctrl-r.png)

# There's more, much more!

There's a lot more that I want to share, but I need to go now. I'll update this article very soon. I want to talk about *killing* and *yanking*! 

Keep using these shortcuts, and they'll become second nature.

See you soon!
