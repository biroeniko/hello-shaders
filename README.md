# Hello-shaders
My first attempt with shaders, textures, etc.
This project is initially made following the tutorial on https://learnopengl.com/, during my learning process.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

The basic requirements for building the executable are:

* CMake 2.8+
* a c++ compiler
* make
* OpenGL 3.3+
* GLFW 3.3+ (OpenGL FrameWork)
* GLAD

#### Installation on Ubuntu

```
sudo apt-get install build-essentials cmake
sudo apt-get install libglu1-mesa-dev freeglut3-dev mesa-common-dev
sudo apt-get install libglfw3-dev libglfw3
git clone https://github.com/Dav1dde/glad.git
cd glad
cmake ./
make
sudo cp -a include /usr/local/
```

* If you encounter any problems with setting up the OpenGL environment on Ubuntu, please read the following guide:
[How to install a OpenGL environment on Ubuntu](https://medium.com/@Plimsky/how-to-install-a-opengl-environment-on-ubuntu-e3918cf5ab6c)

### Installing

This program have been tested on Ubuntu 16.04 but should work under any systems that fulfills the aforementioned requirements.

#### Installation on Ubuntu

If you succesfully cloned the source files and you are currently in the project directory, you can generate the Makefile using the following command:

```
mkdir build
cd build/
cmake ..
```
Now you can build the binary by running:
```
make
```
Som example images which will welcome you in the programs:
![](https://github.com/biroeniko/hello-shaders/blob/master/images/00.png)
![](https://github.com/biroeniko/hello-shaders/blob/master/images/01.png)
![](https://github.com/biroeniko/hello-shaders/blob/master/images/03.png)
![](https://github.com/biroeniko/hello-shaders/blob/master/images/04.gif)
![](https://github.com/biroeniko/hello-shaders/blob/master/images/13.gif)
## Built With

* [OpenGL](https://www.opengl.org/)
* [OpenMP](http://www.glfw.org/)
* [GLAD](https://github.com/Dav1dde/glad)

## Authors

* **Biró Enikő** - [BiroEniko](https://github.com/biroeniko)
