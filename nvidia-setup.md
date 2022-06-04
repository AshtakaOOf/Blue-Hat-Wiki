# This is how to setup the Nvidia Driver on Fedora, and some others nvidia related tweaks.

#### (If you break your system please open a GitHub issue)

## [Please first do this part of the wiki, or this won't work.](dnf-and-repo-tweak.md)

### First Discover what Nvidia GPU you have.
Begin by typing this command in the terminal, to learn what nvidia gpu you have. (You can skip this if you already know)
```
/sbin/lspci | grep -e VGA
```
##### Here an example of what it could look like:
``` 
$ /sbin/lspci | grep -e VGA
01:00.0 VGA compatible controller: NVIDIA Corporation GA104M [GeForce RTX 3070 Mobile / Max-Q] (rev a1)
```
It can also look like this
```
0b:00.0 VGA compatible controller: NVIDIA Corporation GP102 [GeForce GTX 1080 Ti] (rev a1)
```
As you can see i have a RTX 3070, now let's go to the next step.


(This is still wip) [rpmfusion documentation](https://rpmfusion.org/Howto/NVIDIA)
