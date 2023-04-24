# Install updates/upgrades
```
sudo apt update
sudo apt upgrade
sudo apt autoremove
```
# Upgrade release
```
sudo do-release-upgrade
```
# Check of "Additional drivers" e.g. for NVIDIA

# Install usefull SNAP packages
* GIMP
* Inkscape
* Ghostwriter
* Xournal++
* 

# Download + install packages
## VS code
* Download .deb file: https://code.visualstudio.com/Download
* Right click, Properties, Permissions, tick Allow Execution as Program 

## Add Julia
* Download: https://julialang.org/downloads/, e.g. the latest 64-bit glibc version
* Extract. 
* Then browse into the extracted folder to find the folder containing the content like the bin folder etc. Copy/cut all content and move to a local folder where you want Julia to exist e.g. `/home/kevin/julia/`. Not have the version tag in this folder name, so plain `julia` rather than `julia-1.8.5` means the symbolic links can stay constant when you upgrade julia in the future. 

* Setup julia

```
sudo ln -s /home/kevin/julia/bin/julia /usr/bin/julia
```
Export path
```
export PATH="$PATH:/home/kevin/julia/bin"
```

Julia packages to add: 
* IJulia
```
]add IJulia
```
* Gridap
```
]add Gridap
```
* Makie: https://docs.makie.org/stable/
```
]add GLMakie
```

## Git
* Install
```
sudo apt install git
```
* Configure: https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup
Set user name: 
```
git config --global user.name "Kevin-Mattheus-Moerman"
```
Set user email: 
```
git config --global user.email kevin.moerman@gmail.com
```

## GNU Octave
```
sudo apt install octave
```
 
## Install Conda
* Download the installation `.sh` file: https://www.anaconda.com/download/
* Right click, Properties, Permissions, tick Allow Execution as Program 
* Open a terminal in that folder run equivalent of:
```
./Anaconda3-2023.03-Linux-x86_64.sh
```
Conda packages to add: 
* Jupyter notebooks support
```
conda install jupyter
```
* RISE https://rise.readthedocs.io/en/stable/installation.html
```
conda install -c conda-forge rise
```
* Octave kernel https://pypi.org/project/octave-kernel/
```
conda config --add channels conda-forge
conda install octave_kernel
conda install texinfo # For the inline documentation (shift-tab) to appear
```

## Tex / LATeX (SLOW/LONG!)
```
sudo apt install texlive-full
```

# Get LibreOffice plugins
* TexMaths https://extensions.libreoffice.org/en/extensions/show/texmaths-1, download the OXT file, go to LibreOffice Writer, Tools, Extension Manager, Add, then browse to the OXT file. 

# MATLAB
* Download installer
* Right click, Properties, Permissions, tick Allow Execution as Program 
* Extract
* Browse to folder containing `install`, open a terminal and run: 
```
./install
```
Do not run the install as administrator. You can create symbolic links later

# Install Carbon black
* Extract the archive
* Right click the `install.sh` file, Properties, Permissions, tick Allow Execution as Program 
* Run the installation using
```
sudo ./install.sh
```


# Ubuntu things
* Enable add new empty file on right click e.g. 
```
touch ~/Templates/newTextFile.txt
```

