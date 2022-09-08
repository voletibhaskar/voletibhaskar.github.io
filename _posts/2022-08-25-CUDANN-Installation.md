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
1. Install pip
2. Install python 3.9
3. Install VSCode and install venv

#### PART-1: 
 - Install Visual Studio (2019) for Windows 10/11 for CUDA and CUDANN.
 - After Visual Studio installation install CUDA (11.2) for 2019.
 
{: .box-warning}
**Warning:** Please make sure you are installing Visual Studio (2019) from older repos and installing them in 'C:'

 {: .box-note}
**Note:** Install CUDA (11.2) for 2019 and CUDANN (8.1.x) version.

#### PART-2:
Paste these folders under the NVIDIA GPU Toolkit -> CUDA 11.2 -> /bin, /lib, /include
  - cudnn64_7.dll -> /bin
  - cudnn.h -> /include
  - cudnn.lib -> /lib/x64

#### PART-3:

 We need to add these paths to the sys path folder.
 - Control Panel -> System and Security-> System-> Advanced System settings.

 {: .box-note}
**Note:** Usually you will find the two paths under the Environment path location. 

 Assuming your path location C: -> CUDA.11/ 

 {: .box-note}
**Note:** Add the path of  'C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/bin' folder as a path and save

{: .box-note}
**Note:** Add the path of  'C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/libmnrv' folder as a path and save

#### After installing GPU we need to add the following line to your code in the beginning if using VSCode:
~~~
 - import os 
 - os.add_dll_directory("C:/Program Files/NVIDIA GPU Computing Toolkit/CUDA/v11.2/bin")
~~~ 

#### To run venv we need to initiate the following command

{: .box-note}
**Note:** Set-ExecutionPolicy Unrestricted -Scope Process

#### Warning

{: .box-warning}
**Warning:** Please ensure you are using the right path for the Testenv in place of 'YourPath'

#### Initializing Virtual Environment Testenv:
You can initiate the Venv using your path to 'Testenv'. Your 'Testenv' python executable with the concerned python file you want to use.

~~~
 - & "YourPath/Testenv/Scripts/Activate.ps1"
 - & "YourPath/Testenv/Scripts/python.exe" "YourPath/Time_Series_Analysis/Time_Series.py"
~~~