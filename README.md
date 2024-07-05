# AUR packages I install
### Use one at a time, dont be a hero who runs all and ruin everything.

```
mkdir installers
cd installers
```

# basic installations
```
sudo pacman -Sy git base-devel cmake firefox alsa-utils net-tools networkmanager devtools htop less terminus-fonts flameshot xorg-xkill
sudo pacman -Sy pcmanfm evince gcc make autoconf txt2man automake unzip texlive texlive-mathscience texlive-bibtexextra texlive-lang transmission 
sudo pacman -Sy man sshfs nitrogen gcc-fortran ttf-font-awesome inxi feh
```
[comment]: (inxi to check if picom is running)
```
sudo systemctl enable NetworkManager
sudo systemctl start NetworkManager
```

# i3 installation
```
sudo pacman -Sy i3 xorg-xinit
```

# Terminal and editor
```
sudo pacman -Sy terminator vim emacs
git clone https://aur.archlinux.org/visual-studio-code-bin.git code
cd code && makepkg -si 
cd ..
```
## powerlevel10k
- Requirments
```
git clone https://aur.archlinux.org/ttf-meslo-nerd-font-powerlevel10k.git fontpower
cd fontpower && makepkg -si && cd ..
```
- powerlevel10k
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```
- change fonts for vscode and i3config and terminator

## LAMMPS
### mpich
```
git clone https://aur.archlinux.org/mpich installers/mpich
cd mpich && makepkg -si
cd ..
```
### lammps github
```
git clone https://github.com/lammps/lammps.git
cd lammps && git checkout origin/stable && mkdir build
cd build && cmake -C ../cmake/presets/most.cmake  -D BUILD_MPI=yes -D LAMMPS_MACHINE=mpi ../cmake
make -j${nprocs}
cd ../../
```
- add directory to path in .zshrc

## Ulancher
```
git clone https://aur.archlinux.org/ulauncher.git
cd ulauncher && makepkg -si
cd ..
```
- add extensions for calculations etc.

## autotiling for i3
```
git clone https://aur.archlinux.org/autotiling.git
cd autotiling && makepkg -si
cd ..
```

## picom best
```
git clone https://aur.archlinux.org/picom-ftlabs-git.git picom
cd picom && makepkg -si
```

## i3 swallow
```
git clone https://aur.archlinux.org/i3-swallow-git
cd i3-swallow-git && makepkg -si
```
[.config/picom.conf](.config/picom.conf)

## ovito download from website, do not build it. It will try to install openmpi otherwise

# Install Nvidia drivers if required
```
sudo pacman -Sy nvidia
sudo pacman -Sy lib32-nvidia-utils
sudo pacman -Sy nvidia-utils
sudo pacman -Sy nvidia-settings
```

- Install Matlab
- ![wallpaper](https://github.com/tolovegrover/mydotfiles/assets/59788502/25848dea-26bb-4c87-b81d-6209618bf2ec)






