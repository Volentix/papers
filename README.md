# volentix-papers

[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

> This repository contains the LaTeX source code for the Volentix papers.

This repository is to host the files for the translation of the vaious papers into languages other than english. It is bound to the bounty platform hosted by [![Crowdin](https://d322cqt584bo4o.cloudfront.net/volentix-papers/localized.svg)](https://crowdin.com/project/volentix-papers) and follows its conventions.

If you want to add new language, review/update existing translation or help to finish specific translations, you can join and do that by following link:
https://crowdin.com/project/volentix-papers

Note that this repo is ephemeral and will be moved to the [documentation](https://github.com/volentix/documentation) repo once it is complete.

## Table of Contents

* [Install](#install)
    + [OSX](#osx)
    + [Docker Already Installed, Linux](#docker-already-installed-linux)
    + [Manual Build](#manual-build)
  * [Usage](#usage)
    + [Compile Images](#compile-images)
    + [Build PDF](#build-pdf)
  * [Maintainers](#maintainers)
  * [Contribute](#contribute)
  * [License](#license)

## Install

The following are the installation instructions for the various platforms available.

### OSX

* `brew install docker docker-machine`
* `brew tap caskroom/cask`
* `brew cask install virtualbox`
* `docker-machine create --driver virtualbox default`
* `eval $(docker-machine env default)`
* `make`

### Docker Already Installed, Linux

(This is already in the `Makefile`.  Just type `make`.)

* `docker build -t Volentix/papers .`
* `docker run Volentix/papers/vdex-whitepaper/en-US/ > vdex-whitepaper.pdf`

### Manual Build

Currently the manual build instructions are for Ubuntu 16.04 or higher but
may successfully build on other distributions. Pull requests to update the
papers will be gladly accepted and reviewed.

```bash
sudo apt-get update
sudo apt install -y texlive-xetex pandoc python3-pip graphviz imagemagick
pip3 install matplotlib
```

## Usage

### Compile Images

There are several image files in the `/img/` directory that are generated using the build file. The first time the build is done, and whenever the figures are updated, the images will need to be compiled.

```bash
./build.sh
```

### Build PDF

Compile using pandoc
```bash
git clone https://github.com/Volentix/papers.git
cd papers/vdex-whitepaper/en-US
pandoc README.md --pdf-engine=xelatex -o vdex-whitepaper.pdf

```

After building, the pdf file will be output to `vdex-whitepaper.pdf`.

## Maintainers

[@gregory.luneau@gmail.com](https://github.com/gregory.luneau@gmail.com)

## Contribute

See [the contribute file](.github/CONTRIBUTING.md)!

PRs accepted.

Small note: If editing the README, please conform to the [standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## License

MIT © 2019 Volentix Labs Inc.
