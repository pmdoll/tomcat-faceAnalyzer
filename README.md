ToMCAT
======

This is the repository for the ToMCAT (Theory-of-Mind based Cognitive
Architecture for Teams) project at the University of Arizona.

Dependencies
------------

You will need Python 3, and the following

- cmake
- ffmpeg
- swig
- wget
- Java 8
- doxygen 

### MacOS

#### MacPorts

If you have the MacPorts package manager, you can install these with the
following commands.

If you don't have Python 3 already, you can install it with 

```
sudo port install py37-pip
sudo port select --set python python37
sudo port select --set python3 python37
sudo port select --set pip pip37
sudo port select --set pip3 pip37
```

Then install the rest of the dependencies:

```
sudo port install cmake wget openjdk8 swig swig-java ffmpeg doxygen
```


#### Homebrew

If you are using the Homebrew package manager, you can install these with the
following commands (copied from the Project Malmo documentation).

```
brew install python3 # (If you don't have it already)
brew install cmake wget swig ffmpeg doxygen
sudo brew cask install java8
```

Installation
------------

**Note**: If you are an active developer of ToMCAT, it is highly recommended to
create a Python virtual environment for this project and activating it prior to
this step. Also, you can speed up builds by installing Gradle and
adding the line

```
org.gradle.daemon=true
```

to your `~/.gradle/gradle.properties` file. (Source:
https://stackoverflow.com/a/34738800)


To clone the project and install it, do the following:

```
git clone --recursive https://github.com/ml4ai/tomcat
cd tomcat
make install
```

Running the example mission
---------------------------

To run the example mission, do

`make launch_unix`

to launch Minecraft, and then in a separate terminal, do

`make run_example_mission`

This creates an output file `saved_data.tgz`  and an output directory
`mission_records` for further inspection.

