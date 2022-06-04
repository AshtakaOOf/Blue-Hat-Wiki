# This is how to make dnf (the package manager of fedora) faster.

#### (If you break your system please open a GitHub issue)

### Optimize dnf to make it faster.
Type one of these command in the terminal to begin. (The second one is for other edition of fedora)
```
sudo gnome-text-editor /etc/dnf/dnf.conf
```
```
sudo nano /etc/dnf/dnf.conf
```
Now add this to the end of the text file
```
fastestmirror=true
deltarpm=true
max_parallel_downloads=6
```
Change the number from 2 to 10 (Lower if your internet is slow, Higher if you have a fast internet).
After you finished save and quit.

### Add the rpmfusion repo (This will let you install more apps for fedora). 
Begin by typing these command in the terminal.
```
sudo dnf install https://download1.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm

sudo dnf install https://download1.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
```
##### Now do this, to cache the newly added repo.
```
sudo dnf upgrade --refresh
```
### Add flathub repo (This will let you install even more apps for fedora).
Begin by typing this command in the terminal.
```
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
```

(This is still wip)
