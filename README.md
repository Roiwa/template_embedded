# Embedded Project Template

Project
|_ build
    |_ bin
    |_ obj
|_ docs
|_ external
|_ src
    |_ app
    |_ common
    |_ drivers
    |_ test
    |_ main.c
|_ tools
|_ Makefile
|_ README.md

## build Folder
This folder holds all final files to run the project in the MCU. The bin folder will have the executable file of the MCU, and the obj folder all the .o files. The objective of the last folder is to hold all .o, so that if we need to compile again the project, only files we have currently changed are compiled, reducing the compiling time (completely necessary in big projects).


## docs Folder
In this folder, we put all the information of the project. A good practice is to create subfolder which hold only pictures, only texts, etc. Another recommendation is to place the main information in the README file linking the sources to the docs folder.

## external Folder
The external folder will hold any external code (which does not run inside the MCU) needed for the project. For example, a GUI made in Python which receives the information from the MCU. The best way to use this folder is to use a **git submodule** to update this code independently from the rest.

## src Folder
This folder contains all the source files, implementation and headers files. Inside it has different folders depending on their purpose

### app Folder
The app folder holds all source files of the app layer. The app layer means the main functionality of your embedded system, such as driving a drone

### common Folder
The common folder should have all files shared by the app and drivers folder

### drivers Folder
The driver folder holds all source files of the driver layer. This files are those that control electronics which the MCU interacts with and also its peripherals (IOs, timers, interrupts, etc.)

### test Folder
This folder should have the test files of the project, such as unit tests.

### main.c
It will hold the main program of your embedded system

## tools Folder
## Makefile
This file allows to compile the whole project without writing by hand all the dependencies of files in the project, only typing "make" in the command line.

## README.md
It has all the needed information to understand what is the purpose of the project, how to run it, and (if needed) how to develop it.