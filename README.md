# Virtual Remote Lab - Light Diffraction Simulator

Simulate light diffraction patterns from anywhere with an Interactive Virtual Remote Lab Experience!

## Overview
The Virtual Remote Lab (VRL) is an interactive simulation tool for studying light diffraction patterns. Developed in 2019 with partner Kelson Reiss as a project for our SLU Madrid CS Software Engineering course, this virtual lab enables students to conduct diffraction experiments without the need for physical lab access.

## Demo
![Light Diffraction Simulation Demo](ScreenRecording2019-06-25at7.gif)

## Project Background
This project was created to accompany an optical physics course, providing a Java/JavaFX-powered virtual GUI for students to input various parameters and visualize the diffraction output dynamically. The development process involved learning and implementing basic optical physics principles, including the computation of intensity patterns and the identification of wavelength minima/maxima in diffraction profiles.

## Features
- Interactive GUI for simulating diffraction through single, double, and circular slits.
- Real-time graphical representation of diffraction intensity patterns.
- Customizable parameters for slit type, light color, slit separation, width, and observation distance.

## Getting Started

### Prerequisites
- Download JDK 17 or later for your operating system. Make sure `JAVA_HOME` is properly set to the JDK installation directory.
- Download JavaFX SDK for your operating system and unzip to a desired location.

## Installation and Running the Application

### Linux / Mac
Navigate to the root directory of the project from the terminal and run the following commands to set the JavaFX path variable and compile:

```bash
export PATH_TO_FX=path/to/javafx-sdk/lib
javac --module-path $PATH_TO_FX --add-modules=javafx.controls,javafx.fxml -cp .:commons-math3-3.6.1.jar -d out $(find src -name "*.java")
```
Replace `path/to/javafx-sdk/lib` with the actual path to your JavaFX SDK's lib directory.

To run the project:

```bash
java --module-path $PATH_TO_FX --add-modules=javafx.controls,javafx.fxml -cp out:src:commons-math3-3.6.1.jar application.Main
```

### Windows

Navigate to the root directory of the project from the Command Prompt and run the following commands to set the JavaFX path variable and compile:

```cmd
set PATH_TO_FX=path	o\javafx-sdk\lib
dir /s /b src\*.java > sources.txt & javac --module-path %PATH_TO_FX% --add-modules=javafx.controls,javafx.fxml -cp .;commons-math3-3.6.1.jar -d out @sources.txt & del sources.txt
```
Replace `path	o\javafx-sdk\lib` with the actual path to your JavaFX SDK's lib directory.

To run the project:

```cmd
java --module-path %PATH_TO_FX% --add-modules=javafx.controls,javafx.fxml -cp out;src;commons-math3-3.6.1.jar application.Main
```

Note: The classpath separator in Windows is `;` (semicolon), whereas in Linux/Mac it is `:` (colon).

## Authors
- Nolan Murphy
- Kelson Reiss