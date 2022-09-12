---
layout: post
title: Exploratory Data Analysis on a Multivariate Dataset 
subtitle: A detailed explanation of the Exploratory Data Analysis on the Telangana IPASS Dataset. 
tags: [Python]
comments: true
---

## Pre-requisites to this Guide for Windows 11 CUDA, CUDANN installation:
1. Install Pandas
2. Install Plotly, Dash, Jupyter-Dash

In this article, we will perform Exploratory Data Analysis on the Telaganana IPASS Dataset. We will clean, prune and visualize the dataset looking at various features of pandas. 

#### PART-1: 
We add the directory to the 'path' and read all the csv files and merge them under a single file 'all_time_data'.

~~~
def main():
    path = "./Telangana_Industries_TS_IPass"
    files = [file for file in os.listdir(path) if not file.startswith('.')] # Ignore hidden files
    all_time_data = pd.DataFrame()
    for file in files:
        current_data = pd.read_csv(path+"/"+file)
        all_time_data = pd.concat([all_time_data, current_data])
    all_time_data.to_csv("all_time_data_copy.csv", index=False)
    return all_time_data
if __name__ == "__main__":
    all_time_data = main()
~~~

'all_time_data' has 17282 rows and 18 columns.
~~~
all_time_data.shape
~~~  

~~~
all_time_data.info()
~~~
![Telangana IPASS Joint Dataset Info](voletibhaskar.github.io\assets\img\telangana_IPass_data_info.PNG)
~~~
all_time_data.isnull( ).sum( )
~~~

{: .box-warning}
**Warning:** Please make sure you are installing Visual Studio (2019) from older repos and installing them in 'C:'

 {: .box-note}
**Note:** Install CUDA (11.2) for 2019 and CUDANN (8.2.x) version.
