# GradleRIO
GradleRIO is a powerful Gradle Plugin that allows teams competing in the FIRST
robotics competition to produce and build their code without being limited to
the Eclipse IDE.

GradleRIO extracts the WPILib sources from the eclipse plugin and allows you to
use it with Eclipse, IntelliJ IDEA or any IDE of your choice. GradleRIO also allows you to build and
deploy your code to the RoboRIO from the command-line, or through the IDE.

## Basic Commands
- ```gradlew idea``` / ```gradlew eclipse``` will generate all the necessary files for your Development Environment workspace
- ```gradlew build``` will build your Robot Code
- ```gradlew deploy``` will build and deploy your code to the RoboRIO

### Toast-Specific commands
- ```gradlew toastDeploy``` will export Toast to your RoboRIO

## Features
### Dependency Management
GradleRIO manages your Dependencies with ease. Dependencies can be fetched from either Maven or your local system, and can be packaged with your Robot Code into a single, universal JAR. This is done through the ```dependencies { }``` block in your ```build.gradle``` file. 

Other files can be Deployed to your RoboRIO, too! This is done with the ```gradlerio.deployers``` array, which can take files from your FileSystem and deploy them to a target file on your RoboRIO.

Toast Users can enjoy easy dependency management done the modular way. Dependencies can be added to the ```dependencies { }``` block with the configuration ```toastLibrary``` or ```toastModule``` to be deployed to the appropriate folder directly on the RoboRIO, automatically!

### IDE Support
GradleRIO supports a multitude of IDEs, with Eclipse and IntelliJ IDEA being supported by default. It's as simple as running ```gradlew eclipse``` or ```gradlew idea``` to get your Development Environment.

If you're running Toast, we'll even generate Simulation, Verification and Remote-Debug configurations for you!

### Robot Deployment
GradleRIO is flexible with your Robot. When deploying code, GradleRIO will search for your RoboRIO on USB and Network Interfaces. If your RoboRIO is running on a Network that is not your FRC-Provided Radio (perhaps wired ethernet), you can even specify an IP Address to deploy to. 

Because all of the deployment properties are stored in ```build.gradle```, if you decide to change Team Number or Robot Base Class, it's very simple to update this info and have deployment work without a hitch. 

### Extensibility
GradleRIO runs on an underlying Gradle Build System, which is extremely extensible and is used by many professional software companies around the world. Gradle is stable, fast and flexible, with a huge community to back it. You can even write your own Plugins for Gradle if you really want to take control.

IntelliJ IDEA and the latest releases of Eclipse have Gradle support built in, allowing you to run all these commands without leaving your IDE. Alternatively, you can also use the Command Line to build and deploy your code, and is easily automatable.

## Download
To get GradleRIO, head to the [Releases Page](https://github.com/Open-RIO/GradleRIO/releases) and download the zip archive of the latest release. 

*Note: Toast users should follow the guide on the [Toast Wiki](https://github.com/Open-RIO/ToastAPI/wiki) to get the Toasted version*
