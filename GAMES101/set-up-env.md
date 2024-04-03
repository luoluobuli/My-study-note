# Setting Up Programming Environment on Windows
### Process
- On Windows
  - Install Linux with WSL
  - Install VSCode
- On Linux
  - Connect VSCode to Linux and install extensions

### Install Linux on Windows with WSL
> [Install WSL](https://learn.microsoft.com/en-us/windows/wsl/install)
- Open PowerShell or Windows Command Prompt in administrator mode
- Install Ubuntu 18.04
  ```
  wsl --list --online
  wsl --install -d Ubuntu-18.04
  ```

### Connect VSCode to Linux
> [GAMES101——Windows下作业环境配置 VSCode + CMake + MinGW](https://www.bilibili.com/video/BV1Mo4y197g4/?spm_id_from=333.337.search-card.all.click&vd_source=da443e71bf5e7fefec997d649b02e803)
- On Windows, install VSCode from the official website
- Open Ubuntu command line, `cd` to the working directory
- Run `code .`
- Install VSCode extensions: C/C++, C/C++ Extensions, CMake, CMake Tools

### Install
