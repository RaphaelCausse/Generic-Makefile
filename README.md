[![OS](https://img.shields.io/badge/os-linux-blue.svg)](https://shields.io/)
[![OS](https://img.shields.io/badge/os-windows-blue.svg)](https://shields.io/)
[![Status](https://img.shields.io/badge/status-completed-success.svg)](https://shields.io/)

# MAKEFILE C/C++

Makefile template for small to medium sized C/C++ projects, for Linux and Windows.

You can build the project in two modes : Release or Debug.

By default, the build is in Debug mode.

Declare all the source files you want to compile in the `src/sources.mk`.

Please follow recommended project layout.

<br>

# Table of Contents
 
- [Project Layout](#project-layout)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Author](#author)

<br>

## PROJECT LAYOUT

To use this makefile template properly, please follow the project layout bellow.
```
──┬─[ Project ]
  │
  ├──── Makefile
  ├──── README.md
  ├──── LICENSE.md
  │
  ├──┬─[ src ]
  │  ├──── sources.mk   # Important: declare in that file all the source files to compile
  │  │
  │  ├──── main.c / main.cpp
  │  ├──── *.c / *.cpp
  │  ├──── *.h / *.hpp
  │  │
  │  ├──┬─[ module ]
  │  │  ├──── *.c / *.cpp
  │  │  └──── *.h / *.hpp
  │  └...
  │
  └...
```
<br>

## INSTALLATION

**Clone** this repository :
```
git clone https://github.com/RaphaelCausse/Makefile_C_Cpp.git
```
**Move** to the cloned directory :
```
cd Makefile_C_Cpp
```
**Copy** the Makefile in your project at root level of your project directory.
```
cp Makefile <path_to_your_project>
cd <path_to_your_project>
```
**Initialize** the project layout, in your project directory :
```
make init
```

<br>

## USAGE

**Update** the `src/sources.mk` file with the files to compile.

**Update** the Makefile for compiler and linker options, check the variables in the `#### PATHS ####` and `#### COMPILER ####` sections.

**Build** the project in Release mode :
```
make release
```
**Build** the project in Debug mode :
```
make debug
```
**Run** the program in Release mode (with optional arguments) :
```
make run
make run ARGS="your_arguments"
```
<br>

## FEATURES

**Clean** the project directory by removing `bin` and `build` directories :
```
make clean
```
**Clean** the object files, by removing `build` directory :
```
make cleanobj
```
**Display** info about the project :
```
make info
```
**Display** help message:
```
make help
```
<br>

## AUTHOR

Raphael CAUSSE.
