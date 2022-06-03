# This is how to setup the Nvidia Driver on Fedora, and some others nvidia related tweaks.

### (If you break your system please open a GitHub issue)

#### First setup the rpmfusion repo, by typing these command in the terminal.
```
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```

### Now do this, to cache the newly added repo.
```
sudo dnf upgrade --refresh
```

### Now type this command to know what nvidia gpu you have. (You can skip this if you already know)
```
/sbin/lspci | grep -e VGA
```
#### Here an example of what it could look like:
``` 
$ /sbin/lspci | grep -e VGA
01:00.0 VGA compatible controller: NVIDIA Corporation GA104M [GeForce RTX 3070 Mobile / Max-Q] (rev a1)
06:00.0 VGA compatible controller: Advanced Micro Devices, Inc. [AMD/ATI] Cezanne (rev c5)
```
As you can see i have a RTX 3070, now to the next step.

(This is still wip)
