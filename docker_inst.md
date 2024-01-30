---
layout: centered_article
feature_image: assets/images/banner/banner_back.jpg
---

<h4> <a id="win_install" href="#win_install">Docker installation on Windows</a> </h4>

<span id="win_inst_des">

In Windows you will need to install <a href="https://docs.docker.com/desktop/install/windows-install/" target="_blank" rel="noopener noreferrer">Docker Desktop</a> with Windows Subsystem for Linux (WSL) activated. There is a good video <a href="https://www.youtube.com/watch?v=PB7zM3JrgkI" target="_blank" rel="noopener noreferrer">here</a>. Let's start the installation:

1. Install Ubuntu inside WSL. For that open PowerShell or Windows Command Prompt in administrator mode by right-clicking and selecting ``Run as administrator`` and type the following: 

```
wsl --install
```

This command will enable the features necessary to run WSL and install the Ubuntu distribution of Linux. Then restart your machine and you can do it again so you can check that it is already installed. 

Once the installation ends it will ask for a username and a password. This is not necessary, exit the installation by using **Ctrl+C** or by closing the window.

Then you need to make Ubuntu the default Linux distribution. List installed Linux distributions typing:

```
wsl --list -verbose
```

The one with * is the default configuration. So, if it is not Ubuntu, it can be changed by using the command:

```
wsl --set-default Ubuntu
```
2. Install <a href="https://docs.docker.com/desktop/install/windows-install" target="_blank" rel="noopener noreferrer">Docker Desktop</a>. 

Check that everything is correct by opening ``Docker Desktop`` application, going to ``Configuration`` (wheel icon in the right top corner), in ``General`` tab the option ``WSL 2`` should be checked. 

<div class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i> <b>Note:</b> Whenever you want to run BiaPy through Docker you need to start <b>Docker Desktop</b> first</div>

<h4> <a id="mac_install" href="#mac_install">Docker installation on macOS</a> </h4>

Follow Docker's official documentation to install <a href="https://docs.docker.com/desktop/install/mac-install/" target="_blank" rel="noopener noreferrer">Docker Desktop in macOS</a>. 

<div class="alert alert-info" role="alert"><i class="fa fa-info-circle"></i> <b>Note:</b> Whenever you want to run BiaPy through Docker you need to start <b>Docker Desktop</b> first</div>

<h4> <a id="linux_install" href="#linux_install">Docker installation on Linux</a> </h4>

Follow Docker's official documentation to install <a href="https://docs.docker.com/desktop/install/linux-install/" target="_blank" rel="noopener noreferrer">Docker in Linux</a>. 

If you follow the steps and still have problems maybe you need to add your user to docker group:

```
sudo usermod -aG docker $USER
newgrp docker
```
