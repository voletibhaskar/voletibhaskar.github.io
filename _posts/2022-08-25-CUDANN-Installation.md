---
layout: post
title: How to install Tensorflow GPU on Windows 11 for VSCode 
subtitle: A detailed step-by-step explanation of the Tensorflow GPU installation process for VSCode. 
gh-repo: voletibhaskar/Telangana-IPass-Data-Analysis
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

## Pre-requisites to this Guide for Windows 11 CUDA, CUDANN Tensorflow installation:
1. Install python 3.9
2. Install pip 
3. Install VSCode and install Virtual Environment venv

#### PART-1: 
 - Install Visual Studio (2019) for Windows 10/11 for CUDA and CUDANN.
  - [Visual Studio 2019 Installation](https://visualstudio.microsoft.com/vs/older-downloads/)
 - After Visual Studio installation install CUDA (11.2) for 2019.
  - [CUDA 11.2 Installation](https://developer.nvidia.com/cuda-11.2.0-download-archive)
  - After CUDA installation install CUDANN (8.2.x) for CUDA.
  - [CUDA 11.2 Installation](https://developer.nvidia.com/rdp/cudnn-archive)

{: .box-warning}
**Warning:** Please make sure you are installing Visual Studio (2019) from older repos and installing them in 'C:'

 {: .box-note}
**Note:** Install CUDA (11.2) for 2019 and CUDANN (8.2.x) version.

#### PART-2:
Paste these folders under the NVIDIA GPU Toolkit -> CUDA 11.2 -> /bin, /lib, /include
  - cudnn64_7.dll -> /bin
  - cudnn.h -> /include
  - cudnn.lib -> /lib/x64

#### PART-3:

 We need to add these paths to the sys path folder.
 Usually you will find the two paths mentioned under the Environment path location. s

 1. On the Windows taskbar, right-click the Windows icon and select System.
 2. In the Settings window, under Related Settings, click Advanced system settings.
 
 ** Control Panel -> System and Security-> System-> Advanced System settings. ** 

 {: .box-note}
 Add the path and save 'C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/bin'

{: .box-note}
Add the path and save 'C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/libmnrv'

#### After installing GPU we need to add the following line to your code in the beginning if using VSCode:
~~~
 - import os 
 - os.add_dll_directory("C:/Program Files/NVIDIA GPU Computing Toolkit/CUDA/v11.2/bin")
~~~ 

#### To run venv we need to initiate the following command

{: .box-note}
Set-ExecutionPolicy Unrestricted -Scope Process

#### Warning

{: .box-warning}
**Warning:** Please ensure you are using the right path for the Testenv in place of 'YourPath'

#### Initializing Virtual Environment Testenv:
You can initiate the Venv using your path to 'Testenv'. Your 'Testenv' python executable with the concerned python file you want to use.

~~~
 - & "YourPath/Testenv/Scripts/Activate.ps1"
 - & "YourPath/Testenv/Scripts/python.exe" "YourPath/Time_Series_Analysis/Time_Series.py"
~~~