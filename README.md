Templates for academic presentations
======================

> Beamer - LaTeX \ XeLaTeX templates for professional presentations

[![Build Status](https://api.travis-ci.org/demanasta/pres-templates.svg)](https://travis-ci.org/demanasta/pres-templates)
[![License MIT](http://img.shields.io/badge/license-MIT-brightgreen.svg)](LICENCE)
[![](https://img.shields.io/github/release/demanasta/pres-templates.svg)](https://github.com/demanasta/pres-templates/releases/latest)
[![](https://img.shields.io/github/tag/demanasta/pres-templates.svg)](https://github.com/demanasta/pres-templates/tags)

[![](https://img.shields.io/github/stars/demanasta/pres-templates.svg)](https://github.com/demanasta/pres-templates/stargazers)
[![](https://img.shields.io/github/forks/demanasta/pres-templates.svg)](https://github.com/demanasta/pres-templates/network)
[![](https://img.shields.io/github/issues/demanasta/pres-templates.svg)](https://github.com/demanasta/pres-templates/issues)


## Author(s)
*   Demitris G. Anastasiou	

--------------------------------------------------------------------------------
## Features

--------------------------------------------------------------------------------

## Building your thesis - XeLaTeX
### Using latexmk (Unix/Linux/Windows)

This template supports `XeLaTeX` compilation chain. To generate  PDF run

    latexmk -xelatex phd_pres.tex
    biber phd_pres.tex
    latexmk -xelatex -g phd_pres.tex
    
### Shell script for XeLaTeX (Unix/Linux) (Recommended)

Usage: `sh ./compile-thesis.sh [OPTIONS] [filename]`

[option]  xelatex: Compile the PhD thesis using xelatex

[option]  xelatexf: Compile xelatex and biber, full copilation

[option]  clean: removes temporary files no filename required

### Using the make file (Unix/Linux)  still some bugs

The template supports PDF, DVI and PS formats. All three formats can be generated
with the provided `Makefile`.

To build the `PDF` version of your thesis, run:

    make


This build procedure uses `latexmk` and will produce `phd_pres.pdf`.

Use `Variables.ini` to change options:

Clean unwanted files

To clean unwanted clutter (all LaTeX auto-generated files), run:

    make clean

__Bug__: You cannot use `printbib` option on Class file!! 

__Note__: the `Makefile` itself is take from and maintained at
[here](http://code.google.com/p/latex-makefile/).
 
-------------------------------------------------------------------------------

## Usage details

Thesis information such as title, author, year, degree, etc., and other meta-data can be modified in `thesis-info.tex`

### Style file
All style files `.sty` placed at `sty` directory.
> Install Beamer custom style:
> 
> * Run: `$ tlmgr conf | grep "TEXMFHOME"
> 
> * Add style file at `${TEXMFHOME}/tex/latex/beamer/themes/`
> 
> * Run: `$ [sudo] texhash`

Otherwise you can place `.sty` file at the same directory with `.tex` file.
 
### Class files

* `beamerPhD`: Class file for thesis presentations

### Class options

* `aspectration=169`: reduce ratio to 16:9

* `draft`: Special draft mode with line numbers, images, and water mark with timestamp and custom text. Position of the text can also be modified.

* `chapter`: This option enables only the specified chapter and it's references. Useful for review and corrections.

* `notes`: Prints frames and notes 

* `notes=only`: Prints only notes of each frame

* `printbib`: Include bibliography at the end of the presentation (__bug__: not working with makefile!)

## Contributing

1. Create an issue and describe your idea
2. [Fork it](https://github.com/demanasta/pres-templates/network#fork-destination-box)
3. Create your feature branch (`git checkout -b my-new-idea`)
4. Commit your changes (`git commit -am 'Add some feature'`)
5. Publish the branch (`git push origin my-new-idea`)
6. Create a new Pull Request
7. Profit! :white_check_mark:

## ChangeLog

The history of releases can be viewed at [ChangeLog](ChangeLog.md)

## Acknowlegments

* Xanthos Papnikolaou [@xanthospap](https://github.com/xanthospap) - Original design idea of presentation style 