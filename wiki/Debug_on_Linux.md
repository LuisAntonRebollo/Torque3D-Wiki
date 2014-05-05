Debug Torque 3D on Linux
=======

When an application grab input, there are only two ways for the release:

* The application explicitly releasing the grab. This is not possible when a crash occurs, debug breakpoint or similar.
* The application closes. This is not very useful for dubug.


**The following solution can enable a security issue. It is IMPORTANT to disable it, at the end the debug session.**

### Required libraries:
You need to install xdotool:
```
sudo apt-get install xdotool
```

### Preparation for debug
* Open a terminal ```ctrl + atl + t```
* write to activate break grabs:

```
setxkbmap -option grab:break_actions
```

* Write to check:

```
setxkbmap -print | grep grab
```

* You will see this:

```
xkb_compat    { include "complete+xfree86(grab_break)"	};
```

### Debug Torque 3D
* Write this command on console for ungrab mouse when necesary

```
xdotool key XF86Ungrab
```

### Restore system:
* When finished you need to disable break grabs. Write in console:

```
setxkbmap -option
```

* Write to check if disabled:

```
setxkbmap -print | grep grab
```

* You should not see any result
