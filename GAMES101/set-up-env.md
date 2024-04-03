# Setting Up Programming Environment on Windows
### Steps overview
- On Windows
  - Install Linux with WSL
  - Install VSCode
- On Linux
  - Connect VSCode to Linux
  - Install g++
  - Install CMake
  - Install OpenCV
  - Install Eigen

### Install Linux on Windows with WSL
> [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install) <br>

- Open PowerShell or Windows Command Prompt in administrator mode
- Install Ubuntu
```
wsl --install
```
- Set username and password

### Connect VSCode to Linux
> [GAMES101——Windows下作业环境配置 VSCode + CMake + MinGW](https://www.bilibili.com/video/BV1Mo4y197g4/?spm_id_from=333.337.search-card.all.click&vd_source=da443e71bf5e7fefec997d649b02e803)
> 
> [WSL与VScode的配合 在win下进行linux开发](https://www.bilibili.com/video/BV1QJ411x7Yi/?spm_id_from=333.337.search-card.all.click&vd_source=da443e71bf5e7fefec997d649b02e803) <br>

- On Windows, install VSCode from the official website
- Open Ubuntu command line, `cd` to the working directory
- Run `code .`

### Install g++
> [Install and Use G++ on Ubuntu](https://linuxhint.com/install-and-use-g-on-ubuntu/) <br>

```
sudo apt update
sudo apt install build-essential
g++ --version
```

### Install CMake
> [2.1. CMake Installation](https://cgold.readthedocs.io/en/latest/first-step/installation.html) <br>

- Install CMake
```
sudo apt-get -y install cmake
which cmake
cmake --version
```

- Install CMake GUI
```
sudo apt-get -y install cmake-qt-gui
which cmake-gui
cmake-gui --version
```

### Install OpenCV
> [How to Install opencv in C++ on Linux?](https://www.geeksforgeeks.org/how-to-install-opencv-in-c-on-linux/)
>
> [OpenCV: Installation in Linux](https://docs.opencv.org/4.x/d7/d9f/tutorial_linux_install.html)
>
> [Releases - OpenCV](https://opencv.org/releases/) <br>

```
sudo apt install -y g++ cmake make git libgtk2.0-dev pkg-config
git clone https://github.com/opencv/opencv.git
mkdir -p build && cd build
cmake ../opencv
make -j4
sudo make install
```

### Install Eigen
```
sudo apt install libeigen3-dev
```
