# Volentix Papers

(c) 2019 Volentix, Inc.  All rights reserved

This repository contains the LaTeX source code for the Volentix papers. The
instructions to clone the repository and build the PDF using pandoc are
described below.

# Fast Build

## OSX

* `brew install docker docker-machine`
* `brew tap caskroom/cask`
* `brew cask install virtualbox`
* `docker-machine create --driver virtualbox default`
* `eval $(docker-machine env default)`
* `make`

## Docker Already Installed, Linux

(This is already in the `Makefile`.  Just type `make`.)

* `docker build -t Volentix/papers .`
* `docker run Volentix/papers/vdex-whitepaper/en-US/ > vdex-whitepaper.pdf`

# Manual Build

Currently the manual build instructions are for Ubuntu 16.04 or higher but
may successfully build on other distributions. Pull requests to update the
papers will be gladly accepted and reviewed.

## Install Packages

```bash
sudo apt-get update
sudo apt install -y texlive-xetex pandoc python3-pip graphviz imagemagick
pip3 install matplotlib
```

## Compile Images

There are several image files in the `/img/` directory that are generated using the build file. The first time the build is done, and whenever the figures are updated, the images will need to be compiled.

```bash
./build.sh
```

## Build PDF

Compile using pandoc
```bash
cd ~/papers/vdex-whitepaper/en-US/
pandoc INDEX.md --pdf-engine=xelatex -o vdex-whitepaper.pdf

```

After building, the pdf file will be output to `vdex-whitepaper.pdf`.
