<!--
===============================================
Raspberry Pi Toolchains(raspberry-pi-cross-compilers): This project 
provides latest automated GCC Cross Compiler & Native (ARM & ARM64) 
build-scripts and precompiled standalone toolchains for Raspberry Pi.


Copyright (C) 2020 Abhishek Thakur(@abhiTronix) <abhi.una12@gmail.com>


This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
===============================================
-->


<table align="center"><tr><td align="center">
<img alt="Raspberry Pi Toolchains Logo" src="https://raw.githubusercontent.com/abhiTronix/Imbakup/master/Images/gcc/GCC.png">

<a align="center"> **Latest CI maintained Precompiled Standalone ARM & ARM64 Toolchains for Raspberry Pi SBCs**</a>

![CI Builder Pi[0-1]](https://github.com/abhiTronix/raspberry-pi-cross-compilers/workflows/CI%20Builder%20Pi%5B0-1%5D/badge.svg)
![CI Builder Pi[2-3]](https://github.com/abhiTronix/raspberry-pi-cross-compilers/workflows/CI%20Builder%20Pi%5B2-3%5D/badge.svg)
![CI Builder Pi[3+]](https://github.com/abhiTronix/raspberry-pi-cross-compilers/workflows/CI%20Builder%20Pi%5B3+%5D/badge.svg)
![CI Builder Pi[64]](https://github.com/abhiTronix/raspberry-pi-cross-compilers/workflows/CI%20Builder%20Pi%5B64%5D/badge.svg)
![CI Builder Pi[Desktop]](https://github.com/abhiTronix/raspberry-pi-cross-compilers/workflows/CI%20Builder%20Pi%5BDesktop%5D/badge.svg)

[![ko-fi][kofi-badge]][kofi]

[![License][license-badge]][license]
![GitHub release (latest by date)](https://img.shields.io/github/v/release/abhiTronix/raspberry-pi-cross-compilers?logo=github)
[![Downloads][downloads-badge]][downloads]



</td></tr></table>

&nbsp;

## Table of Contents

* [**TL'DR**](#tldr)
* [**New v3.0+ Release SneekPeak**](#new-release-sneekpeak-v30)
* [**Precompiled Toolchains: Easy-to-Use**](#precompiled-toolchains-easy-to-use)
  * [**A. Automated Toolchain Builder Workflow**](#a-automated-toolchain-builder-workflow)
  * [**B. Toolchain Binaries description table**](#b-toolchain-binaries-description-table)
  * [**C. Identifying Toolchain Binaries by Name**](#c-identifying-toolchain-binaries-by-name)
  * [**D. Toolchain Binaries Downloads**](#d-toolchain-binaries-downloads)
  * [**E. Toolchain Setup Documentation**](#e-toolchain-setup-documentation)
  * [**F. Supported Toolchains Programming Languages**](#f-supported-toolchains-programming-languages)
* [**Build-Script for Developers**](#build-script-for-developers-do-it-yourself-muscle)
* [**Supporting this Project :heart:**](#supporting-this-project)
* [**Additional Information**](#additional-information)
  * [**Supported ARM Devices**](#supported-arm-devices)
  * [**Optimization Flags Involved**](#optimization-flags-involved)
* [**Citing**](#citing)
* [**Copyright License**](#copyright-license)
* [**Acknowledgments**](#acknowledgments)

&nbsp;

&nbsp;


### TL'DR

**What is this project?**

> _This project provides the Latest, CI maintained, Precompiled [**Raspberry Pi CPU optimized**](#optimization-flags-involved) GCC Cross & Native (ARM & ARM64) Compressed Standalone Toolchains, that is [**fastest to setup**](#e-toolchain-setup-documentation) and saves you tons of time and helps you to get quickly started with software development on Pi._

**Who will benefit from the project?**

> _This project benefits everyone, from Professional Devs to a college research Student, looking for latest easy-to-use precompiled GCC toolchains for their Hobby Raspberry Pi project(s)._ 


&nbsp;

&nbsp; 

### New v3.0+ Release SneekPeak

- *Automated CI maintained GCC standalone ARM & ARM64 toolchains.*
- *Latest [**GCC 10.2.0**](https://gcc.gnu.org/gcc-10/) toolchains available.*
- *Hardcoded paths free both Cross & Native **Raspbian Buster (Debian 10)** toolchains available.*
- *Separate binaries for each Raspberry Pi variant (including latest Compute modules and Raspberry Pi 4).*
- *PIGZ-TAR Compressed Binaries avaliable with maximum possible compression.*
- *Exclusive **ARM64|AARCH64** Binaries for Raspberry Pi 64-Bit kernel OS flavors.*
- *Open-sourced Toolchains build-scripts are also available.*
- *Latest [**GDB Debugger v9.2**](https://www.gnu.org/software/gdb/download/ANNOUNCEMENT) included in all binaries.*


&nbsp;

&nbsp;



# Precompiled Toolchains: Easy-to-Use

This project now utilizes powerful [**Github Actions**][git-action] CI(Continuous Integration) to auto-compile Compressed GCC Cross & Native ARM & ARM64 Toolchain binaries and thereby auto-deploy them to SourceForge repository.


### A. Automated Toolchain Builder Workflow:

<h3 align=center><img alt="Workflow" title="Toolchain Builder Workflow" src="https://raw.githubusercontent.com/abhiTronix/Imbakup/master/Images/gcc/workflow.png"></h3>


&nbsp;

### B. Toolchain Binaries description table:

Here's a reference table for various CI generated OS targetted precompiled Toolchain Binaries available with this project:

<br>

**References:**
* **Host OS:** on which the toolchain is executed/used.
* **Target OS:** for which the toolchain generates code.


| Toolchains | Host OS | Target OS | Current Status | Precompiled GCC versions available |
| :---------- | :--------: | :-------: | :--------: | :------------------------: |
| **Raspberry Pi GCC Cross-Compiler Toolchains(Stretch)** | any x64/x86 Linux machine | Raspbian Stretch OS (Debian Version 9) only | Stable/Production | 6.3.0,  9.3.0, 10.2.0 |
| **Raspberry Pi GCC Cross-Compiler Toolchains(Buster)** | any x64/x86 Linux machine | Raspbian Buster OS (Debian Version 10) only | Stable/Production | 8.3.0, 9.3.0, 10.2.0 |
| **Raspberry Pi GCC Native-Compiler Toolchains(Stretch)** | Raspbian Stretch OS (Debian Version 9) only | Raspbian Stretch OS (Debian Version 9) only | Stable/Production | 9.3.0, 10.2.0 |
| **Raspberry Pi GCC Native-Compiler Toolchains(Buster)** | Raspbian Buster OS (Debian Version 10) only | Raspbian Buster OS (Debian Version 10) only | Stable/Production | 9.3.0, 10.2.0 |
| **Raspberry Pi GCC 64-Bit Cross-Compiler Toolchains** | any x64/x86 Linux machine | any x64 Raspberry Pi OS(like Pi64) | Stable/Production | 6.3.0, 8.3.0, 9.3.0, 10.2.0 |
| **Raspberry Pi GCC 64-Bit Native-Compiler Toolchains** | any x64 Raspberry Pi OS(like Pi64) | any x64 Raspbian OS(like Pi64) | Stable/Production | 8.3.0, 9.3.0, 10.2.0 |
| **Exclusive/Experimental Toolchains** |  x86/x86_64 Pi Desktop | x86/x86_64 Pi Desktop | Beta/Experimental | 10.2.0 | 


&nbsp;

### C. Identifying Toolchain Binaries by Name:

You can easily identify each pre-compiled toolchain binary by its name as follows:

<h3 align=center><img alt="Binary Description" title="Toolchain Binaries Description" src="https://raw.githubusercontent.com/abhiTronix/Imbakup/master/Images/gcc/gcc-large.png"></h3>


### D. Toolchain Binaries Downloads:


**[TAR][tar]-[PIGZ][pigz] Compressed** pre-compiled GCC Toolchain binaries can be easily be downloaded from the project's [**SourceForge Repository**](https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/) or by clicking links given in the following table:

| Toolchains Binaries | Status | GCC versions |
| ---------- | -------- | :------: |
| **Raspberry Pi GCC Cross-Compiler Toolchains(Stretch)**  | Stable/Production | [6.3.0][cc-stretch-630], [9.3.0][cc-stretch-930], [10.2.0][cc-stretch-1020] |
| **Raspberry Pi GCC Cross-Compiler Toolchains(Buster)** | Stable/Production | [8.3.0][cc-buster-830], [9.3.0][cc-buster-930], [10.2.0][cc-buster-1020] |
| **Raspberry Pi GCC Native-Compiler Toolchains(Stretch)** | Stable/Production | [9.3.0][nc-stretch-930], [10.2.0][nc-stretch-1020] |
| **Raspberry Pi GCC Native-Compiler Toolchains(Buster)** | Stable/Production | [9.3.0][nc-buster-930], [10.2.0][nc-buster-1020] |
| **Raspberry Pi GCC 64-Bit Cross-Compiler Toolchains** | Stable/Production | [6.3.0][cc-64-630], [8.3.0][cc-64-830], [9.3.0][cc-64-930], [10.2.0][cc-64-1020]|
| **Raspberry Pi GCC 64-Bit Native-Compiler Toolchains** | Stable/Production | [8.3.0][nc-64-830], [9.3.0][nc-64-930], [10.2.0][nc-64-1020] |
| **Exclusive/Experimental Toolchains** |  Beta/Experimental | [10.2.0 (x86)][dc-x86-1020], [10.2.0 (x86_64)][dc-x86_64-1020] |  


**Tip::bulb:** _To get the location of each Binary of this project on SourceForge, you can also check out [this Reference Tree](https://github.com/abhiTronix/raspberry-pi-cross-compilers/wiki/Toolchain-Binaries-Reference-Tree#toolchain-binaries-reference-tree)._


&nbsp;


### E. Toolchain Setup Documentation:

These precompiled toolchains setup requires just three easy steps - **Downloading, Extracting and Linking**:

* #### [WIKI-Documentation (en-English)](https://github.com/abhiTronix/raspberry-pi-cross-compilers/wiki)

&nbsp;

### F. Supported Toolchains Programming Languages:
- C++
- Fortran
- C
- Any other language support can be easily [compiled](#build-script-for-developers-do-it-yourself-muscle).
 
&nbsp;

&nbsp;


# Build-Script for Developers: Do It Yourself :muscle:

Open-Source is awesome :heart:

- This project now provides user-friendly open-sourced bash build-scripts that auto-generates Compressed Cross & Native GCC ARM & ARM64 Toolchain binaries targeting Raspberry Pi 32-bit & 64-bit OSes.

- If you need additional language support or need to compile another suitable GCC version toolchains for your Raspberry Pi, then you can use these scripts to manually compile any GCC toolchains by running suitable build-scripts yourself through your system terminal.

- **You can find complete information about these build-scripts [here](/build-scripts)**


&nbsp;

&nbsp;


# Supporting this Project

**If these binaries helped you big time, please consider supporting it through any size donations.:heart:.**

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg?logo=paypal&style=for-the-badge)](https://paypal.me/AbhiTronix)

[![ko-fi][kofi-badge]][kofi]

***Also please share your [**thoughts**](https://sourceforge.net/projects/raspberry-pi-cross-compilers/reviews) or just drop a [star :star:](https://github.com/abhiTronix/raspberry-pi-cross-compilers/stargazers).***

&nbsp;

&nbsp;

# Additional Information

### A. Supported Devices:

- All Raspberry Pi hardware/versions/models are currently supported. 
- Any other ARM & ARM64 Device _(such as Android, other SBCs, IoT etc.)_ with similar or compatible Hardware architecture(see [Optimization Flags](#optimization-flags-involved)), should also work.

### B. Optimization Flags Involved:

These toolchains are built with these following system-specific LTO _(Link Time Optimization)_ flags, therefore you can easily take advantage of your Raspberry Pi's CPU specific features with these Toolchains while compiling your programs:


| Raspberry Pi Board | Link Time Optimization Flags |
|---|---|
| Raspberry Pi - *Zero/W/WH & 1 Model A/B/A+/B+* | `-march=armv6 -mfloat-abi=hard -mfpu=vfp` |
| Raspberry Pi - *2 & 3 Model A/B* | `-march=armv7-a -mfloat-abi=hard -mfpu=neon-vfpv4` |
| Raspberry Pi - *3 & 4 Model A+/B+ & Compute 3/3-lite/3+ (32-Bit)* | `-march=armv8-a -mfloat-abi=hard -mfpu=neon-fp-armv8` |
| Raspberry Pi - *3 & 4 Model A+/B+ & Compute 3/3-lite/3+ (64-Bit)* | `-march=armv8-a+fp+simd` |


**Raspberry Pi 4+:** _The latest Raspberry Pi 4 uses a Broadcom BCM2711 SoC with a 1.5 GHz 64-bit quad-core ARM Cortex-A72 processor, that also have armv8-a architecture similar to Raspberry Pi 3B+, therefore it is also officially supported!_

&nbsp; 

&nbsp;

# Citing

**Here is a Bibtex entry you can use to cite this project in a publication:**

```BibTeX
@misc{raspberry-pi-cross-compilers,
    Title = {Raspberry Pi Toolchains},
    Author = {Abhishek Thakur},
    howpublished = {\url{https://github.com/abhiTronix/raspberry-pi-cross-compilers}},
    year = {2020}  
  }
```


&nbsp; 

&nbsp;


# Copyright License

**Copyright © 2020 abhiTronix**

This Project source-code and its precompiled binaries are licensed under the [**GPLv3**][license] license.

&nbsp;

&nbsp; 
 

# Acknowledgments

Thank you,

- [GNU project][gnu] for providing the latest source code.   
- [Raspberry Pi project][pi-project] for providing the latest kernel and docs.  
- [GitHub Actions][git-action] for making it easier to automate Toolchain Builder workflows.
- [Sourceforge project][sf-project]  for allowing me to publish these binaries.


[downloads-badge]:https://img.shields.io/sourceforge/dm/raspberry-pi-cross-compilers.svg?style=flat&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAALQAAAC0CAMAAAAKE/YAAAAAYFBMVEVHcEz/OwDzfCD0fCDzfCDzfR/zfCD9fiHzfCD0fCDzfCD0fSDzeyDzfB/zfCDzfCDzfCD/WgPzfCDxfx7wfCH0fCDzfCDzfCDzfB/zfCDzfCD0fCDzfCDyfCD1fCDzfCAr6LXeAAAAH3RSTlMAAXuI/oNpCPhIlYq2oYC37wN2IRDO5sI926lfUycyJgWG0gAABKZJREFUeAHt3P9Os0gUxvEzOhZobUvL71r73P9dbkzfJcW3wPCcnRzN8v1b48cjhWEmUdbW1tbW1tbWPrr8WVUrP7cXjJSXv88MZL/Q7IvfZ8aL/MzOGG+3mlfzal7N/0vzpq43Yt5hkfkN8Dj8OvNXh19mJtTmZnM1YTZXE2ZzNWE2VxNmczVhNlcTZls1YT4Tr2HWZpfDUk2Yp9E4/FDz9De8/FCzuK2BmjBbqgmzvZow26t5M6+2N9ur3wgzobYw82p7860g1MbmA9JMvneaVJubpUKvNpr1tPlVntQBSFti1kbmHo2cuK4NzVIDgK+Sv9X7KbWpucS9vRBqI7Nrcc9fCbWFeXBAV5eE2sbsKvzJb4VQW5jlhj7fEmoLszyYfOUItYH50+Ohq8RX683yjscqF1+tN18xLBOlOr75VNYY1ohOHd8s7h3fu8nTTryaN4ceLPqtqNTxzZnHX+WJRh3fXOR40lV4dXxzUuFZF6HV8c1ywbN8mtDq+OYzRroKqY5vbj1G2gqrjm0uaozVCa2Oa3ZHjPfJq2Oa5YyJNsKrI875M8V4fi/R1LxZXIOpOtGoI5nlA5P5sv/COluq9i9xzGWO6Vr50wbdiZs1b57eMwj4JLbAh3Cz5s3EoAePl9Kjc/rrWm+WM2byzePe5FXUs9abXYe5avm3I9Do7yF6c4vZfPKwKeILRn2WQa+0uXfMVjz+sIOo1TvludUpx3yt3HMbAJ3Tqs8YrzrJfDcE1N/nNv2voFFPzelN5nMvmM+fB8/OnSjVuXY52yCgtwG6EqX6gPEaJ/PVCGg7QPtSRnMharenFsJ9JUK6DK5pZKKc9dQ5mZ9XtwjpOFymHGQiF1/9gZCa4Q32ImI66/MitLvcDwhkMne6YLyNXv2GkHpl169FJitrjPehVbvdInTi8VUqc+0Cll+8eo+Qum8f25PmvSIVQs2je0spMx0nb/qEmkDncq8JnPQV470nolXvMN3gL1p4fOVTmS5LQ8y8+oCgisHVUevMjJp4uPhMRFxS416jN6vULYLaDd6R9nqzSl16hFSXj8dIZ71Zp64QVJMdeg1atXnYUrXbYnFpojPrZ33F4t6VZv2skxxL+9Ca9bPeY2FpqTXrZ33DwrZ6s37WDRblP/Vm/awzLOoSwUzM+ogFpZ+sWT/ribOt6XZRzMSsXxBcl0QxE7M+NQgsvfHmoF7D1UWNsDaMOZb6lvMXNG/WqtsQ9dYRZmP1jjHHVRdVwM46YY6qduUeE3UtY46o7gk1RvK7hDTHVyebp2x/4Z7d0dU9u8K36h27rouv7vvcvPfzzqvXNhHSHF89rLxl12vWFk793s33NqkmIswGasJspObNdmrebKfmzXZq3myn5s02at58JM282tbMq+3NvJo326l5s52aN9upebOdmjdbqlmzrZozG6uvjNla3RFmc3XqCLO1emttJv7JUZMQZiM1b7ZT82Z7dVMSZiM1b7ZR25uJzuirCLOVmjdbqlmzrZozW6tTHI3NRGUp1mYi5+zNfKt5Na9m+/g9c8tcmVubiTJzM1HhKbP9QuRZfm9vnqgsnvUfk9fW1tbW1tb+AZhQydEXZaX4AAAAAElFTkSuQmCC
[license-badge]:https://img.shields.io/github/license/abhiTronix/raspberry-pi-cross-compilers.svg?style=flat&logo=gnu
[kofi-badge]:https://www.ko-fi.com/img/githubbutton_sm.svg

[downloads]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files
[license]:https://github.com/abhiTronix/raspberry-pi-cross-compilers/blob/master/LICENSE
[kofi]:https://ko-fi.com/W7W8WTYO
[gnu]:https://gcc.gnu.org/
[pi-project]:https://www.raspberrypi.org/
[sf-project]:https://sourceforge.net
[git-action]:https://github.com/features/actions
[tar]:https://www.gnu.org/software/tar/
[pigz]:https://zlib.net/pigz/

[cc-stretch-630]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Cross-Compiler%20Toolchains/Stretch/GCC%206.3.0/

[cc-stretch-930]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Cross-Compiler%20Toolchains/Stretch/GCC%209.3.0/
[cc-stretch-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Cross-Compiler%20Toolchains/Stretch/GCC%2010.2.0/
[cc-buster-830]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Cross-Compiler%20Toolchains/Buster/GCC%208.3.0/

[cc-buster-930]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Cross-Compiler%20Toolchains/Buster/GCC%209.3.0/
[cc-buster-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Cross-Compiler%20Toolchains/Buster/GCC%2010.2.0/
[nc-stretch-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Native-Compiler%20Toolchains/Stretch/GCC%2010.2.0/
[nc-buster-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Native-Compiler%20Toolchains/Buster/GCC%2010.2.0/
[nc-stretch-930]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Native-Compiler%20Toolchains/Stretch/GCC%209.3.0/
[nc-buster-930]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Raspberry%20Pi%20GCC%20Native-Compiler%20Toolchains/Buster/GCC%209.3.0/
[cc-64-630]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Cross-Compiler%20Toolchains/GCC%206.3.0/
[cc-64-830]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Cross-Compiler%20Toolchains/GCC%208.3.0/
[cc-64-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Cross-Compiler%20Toolchains/GCC%2010.2.0/
[cc-64-930]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Cross-Compiler%20Toolchains/GCC%209.3.0/
[nc-64-830]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Native-Compiler%20Toolchains/GCC%208.3.0/
[nc-64-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Native-Compiler%20Toolchains/GCC%2010.2.0/
[nc-64-930]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Bonus%20Raspberry%20Pi%20GCC%2064-Bit%20Toolchains/Raspberry%20Pi%20GCC%2064-Bit%20Native-Compiler%20Toolchains/GCC%209.3.0/
[dc-x86-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Exclusive-Experimental%20Toolchains/Desktop/x86/GCC%2010.2.0/
[dc-x86_64-1020]:https://sourceforge.net/projects/raspberry-pi-cross-compilers/files/Exclusive-Experimental%20Toolchains/Desktop/x86_64/GCC%2010.2.0/