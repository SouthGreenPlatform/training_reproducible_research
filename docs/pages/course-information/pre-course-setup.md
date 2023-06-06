{% raw %}
# Unix environment

## Setup for Mac / Linux users

You are lucky, using a UNIX based system as always been ideal for bioinformatics.
Open a bash shell terminal and follow the installation instructions.

First, create and move into a directory on your computer where it makes
sense to work during the course e.g. `{{training_path}}`.

```bash
mkdir {{training_path}}
cd {{training_path}}
```

## Setup for Windows users

Using a Windows computer for bioinformatic work has sadly not been ideal most of
the time, but large advanced in recent years have made this quite feasible
through the Windows 10 *Linux subsystem*. This is the only setup for Windows
users that we allow for participants of this course, as all the material has
been created and tested to work on Unix-based systems.

Using the Linux subsystem will give you access to a full command-line bash shell
based on Linux on your Windows 10 PC. For the difference between the Linux Bash
Shell and the PowerShell on Windows 10, see *e.g.* [this article](
https://searchitoperations.techtarget.com/tip/On-Windows-PowerShell-vs-Bash-comparison-gets-interesting).

Install Bash on Windows 10, follow the instructions at *e.g.* one of these
resources:

- [Installing the Windows Subsystem and the Linux Bash](https://docs.microsoft.com/en-us/windows/wsl/install-win10)
- [Installing and using Linux Bash on Windows](https://www.howtogeek.com/249966/how-to-install-and-use-the-linux-bash-shell-on-windows-10/)
- [Installing Linux Bash on Windows](https://itsfoss.com/install-bash-on-windows/)

!!! note

    If you run into error messages when trying to download files through the Linux
    shell (_e.g._ `curl:(6) Could not resolve host`) then try adding the Google
    nameserver to the internet configuration by running `sudo nano /etc/resolv.conf`
    then add `nameserver 8.8.8.8` to the bottom of the file and save it.

Open a bash shell Linux terminal and clone the GitHub repository containing all
files you will need for completing the tutorials as follows. First, create and move into 
a directory on your computer where it makes sense to work during
the course e.g. `{{training_path}}`.

!!! tip

    You can find the directory where the Linux distribution is storing all its
    files by typing `explorer.exe .`. This will launch the Windows File Explorer
    showing the current Linux directory.
    Alternatively, you can find the Windows C drive from within the bash shell
    Linux terminal by navigating to `/mnt/c/`.

```bash
mkdir {{training_path}}
cd {{training_path}}
```

**Whenever a setup instruction specifies Mac or Linux (*i.e.* only those two,
with no alternative for Windows), please follow the Linux instructions.**


# Git

Chances are that you already have git installed on your computer. You can check
by running *e.g.* `git --version`. If you don't have git, install it following
the instructions [here]( https://git-scm.com/book/en/v2/Getting-Started-Installing-Git).
If you have a very old version of git you might want to update to a later version.

Git configutation will be done together during the training.

# Conda

Conda installation and configutation will be done together during the training event.


# Snakemake

Snakemake installation and configutation will be done together during the training event.

# Nextflow

Nextflow installation and configutation will be done together during the training event.

# R Markdown

R Markdown installation and configutation will be done together during the training event.

# Jupyter

Jupyter installation and configutation will be done together during the training event.

# Docker

Installing Docker is quite straightforward on Mac or Windows and a little more
cumbersome on Linux. Note that Docker runs as root, which means that you have to
have `sudo` privileges on your computer in order to install or run Docker. When
you have finished installing docker, regardless of which OS you are on, please
type `docker --version` to verify that the installation was successful!

## macOS intel/M1/M2

Go to [docker.com](https://docs.docker.com/docker-for-mac/install/#download-docker-for-mac)
and select download option that is suitable for your computer's architecture
(*i.e.* if you have an Intel chip or a newer Apple M1 chip). This will download
a `dmg` file - click on it when it's done to start the installation. This will
open up a window where you can drag the Docker.app to Applications. Close the
window and click the Docker app from the Applications menu. Now it's basically
just to click "next" a couple of times and we should be good to go. You can
find the Docker icon in the menu bar in the upper right part of the screen.

## Linux

How to install Docker differs a bit depending on your Linux distribution, but
the steps are the same. Please follow the instructions for your distribution on
[https://docs.docker.com/engine/install/#server](https://docs.docker.com/engine/install/#server).

!!! Tip
    As mentioned before, Docker needs to run as root. You can achieve this by
    prepending all Docker commands with `sudo`. This is the approach that we
    will take in this tutorial, since the set up becomes a little simpler that way.
    If you plan on continuing using Docker you can get rid of this by adding your
    user to the group `docker`. Here are instructions for how to do this:
    [https://docs.docker.com/engine/installation/linux/linux-postinstall/](https://docs.docker.> com/engine/installation/linux/linux-postinstall/).

## Windows

In order to run Docker on Windows your computer must support *Hardware
Virtualization Technology* and virtualization must be enabled. This is
typically done in BIOS. Setting this is outside the scope of this tutorial,
so we'll simply go ahead as if though it's enabled and hope that it works.

On Windows 10 we will install Docker for Windows, which is available at
[docker.com](https://docs.docker.com/docker-for-windows/install/#download-docker-for-windows).
Click the link *Download from Docker Hub*, and select *Get Docker*. Once the
download is complete, execute the file and follow the
[instructions](https://docs.docker.com/docker-for-windows/install/#install-docker-desktop-on-windows).
You can now start Docker from the Start menu. You can search for it if you
cannot find it; the Docker whale icon should appear in the task bar.

You will probably need to enable integration with the Linux subsystem, if you
haven't done so during the installation of Docker Desktop. Right-click on the
Docker whale icon in the task bar and select *Settings*. Choose *Resources* and
select *WPS integration*. Enable integration with the Linux subsystem and click
*Apply & Restart*; also restart the Linux subsystem.

# Singularity

Singularity installation might be tiedous. No worries if you do not succeed the installation. 
We can reiew the installation procedure during the training event.

Installation of Singularity depends, again, on your operating system. When you
have finished, regardless of your OS, please type `singularity --version` to
verify that your installation was successful!

Both Mac and Windows utilise Vagrant, for which the information in the box
below may help you.

> **Vagrant and VirtualBox** <br>
> The Vagrant VirtualBox with Singularity can be started like this:
>
> - Move into the folder `vm-singularity` where you installed Singularity.
> - Type `vagrant up` and once this has finished, verify that the Vagrant
>   VirtualBox is running with `vagrant status`.
> - Now, type `vagrant ssh`, which will open the Vagrant VirtualBox.
> - The first time you open the Vagrant VirtualBox like this, you will have to

## macOS intel

Please follow the Mac-specific instructions at the [Singularity website](https://sylabs.io/guides/latest/admin-guide/installation.html#installation-on-windows-or-mac).
!!! Notes
    the command   
    `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`  
    must be replaced by this one  
    `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`  


## macOS M1/M2

You're out of luck this time, as often with new OS and chip architectures, the tools may not yet be compatible.
The proper way here is to use a linux virtual machine. You will have to download a linux distribution iso image and install it via a virtual machine manager.
Please follow the instruction [here](https://sylabs.io/2023/03/installing-singularityce-on-macos-with-apple-silicon-using-utm-rocky/).

!!! Notes
    You will need a linux iso image ARM architecture compatible.  
    You can find rockylinux iso image at this address: [https://rockylinux.org/download](https://rockylinux.org/download) 
    Or use Ubuntu Server for ARM available here: [https://ubuntu.com/download/server/arm](https://ubuntu.com/download/server/arm)

## Linux

Follow the Linux-specific instruction at the [Singularity website](https://sylabs.io/guides/latest/admin-guide/installation.html#installation-on-linux).

## Windows

Please follow the Windows-specific instructions at the [Singularity website](https://sylabs.io/guides/latest/admin-guide/installation.html#installation-on-windows-or-mac).

!!! Notes
    Last time we checked, the software "Vagrant Manager" was not available for
    download but the installation of Singularity was successful even without it.

    Version 6.1.28 of "Virtual box for Windows" may not work, please install
    Version 6.1.26 from [here](https://www.virtualbox.org/wiki/Download_Old_Builds_6_1)
    in case you encounter problems when trying to start the Vagrant VirtualBox.

{% endraw %}