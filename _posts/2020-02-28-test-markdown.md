---
layout: post
title: How to install Tensorflow GPU on Windows 11 for VSCode 
subtitle: A detailed step-by-step explanation of the Tensorflow GPU installation process for VSCode. 
gh-repo: voletibhaskar/Telangana-IPass-Data-Analysis
gh-badge: [star, fork, follow]
tags: [test]
comments: true
---

# Installation Guide for Windows 11:
1. Install pip
2. Install python 3.9
3. Install VSCode and install venv

### To run venv we need to initiate the following command:
Set-ExecutionPolicy Unrestricted -Scope Process

### Enter the following code to initialize the Virtual Environment Testenv:
 - & "d:/Linkedin Learning/PythonTraining/Testenv/Scripts/Activate.ps1"
 - & "d:/Linkedin Learning/PythonTraining/Testenv/Scripts/python.exe" "d:/Linkedin Learning/PythonTraining/Time_Series_Analysis/Time_Series.py"

#### If we have to install GPU we need to follow the following: 
 - Install Visual Studio (2019) for Windows 10/11 for CUDA and CUDANN
 - After Visual Studio installation install CUDA (11.2) for 2019 as we can't install any other version as they are not compatible
 - Download CUDANN and extract the 3 files /bin, /lib, /include and copy them and replace them with the folders of CUDA GPU Toolkit
 - C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/ 
 - Add the path of  C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/bin folder as a path and save
 - Add the path of  C:Users/Program Files/NVIDIA GPU Toolkit /CUDA.11/libmnrv folder as a path and save

#### After installing GPU we need to add the following line to your code in the beginning if using VSCode:
 - import os 
 - os.add_dll_directory("C:/Program Files/NVIDIA GPU Computing Toolkit/CUDA/v11.2/bin")


This is a demo post to show you how to write blog posts with markdown.  I strongly encourage you to [take 5 minutes to learn how to write in markdown](https://markdowntutorial.com/) - it'll teach you how to transform regular text into bold/italics/headings/tables/etc.

**Here is some bold text**

## Here is a secondary heading

Here's a useless table:

| Number | Next number | Previous number |
| :------ |:--- | :--- |
| Five | Six | Four |
| Ten | Eleven | Nine |
| Seven | Eight | Six |
| Two | Three | One |


How about a yummy crepe?

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg)

It can also be centered!

![Crepe](https://s3-media3.fl.yelpcdn.com/bphoto/cQ1Yoa75m2yUFFbY2xwuqw/348s.jpg){: .mx-auto.d-block :}

Here's a code chunk:

~~~
var foo = function(x) {
  return(x + 5);
}
foo(3)
~~~

And here is the same code with syntax highlighting:

```javascript
var foo = function(x) {
  return(x + 5);
}
foo(3)
```

And here is the same code yet again but with line numbers:

{% highlight javascript linenos %}
var foo = function(x) {
  return(x + 5);
}
foo(3)
{% endhighlight %}

## Boxes
You can add notification, warning and error boxes like this:

### Notification

{: .box-note}
**Note:** This is a notification box.

### Warning

{: .box-warning}
**Warning:** This is a warning box.

### Error

{: .box-error}
**Error:** This is an error box.