# MALib-Dataset

## Introduction

MALib is an open-source dataset which contains 56,000+ mobile apps gathered from Google Play and 763 corresponding third-party libraries that have been used by those apps. 

It can be used for investigating the potential relationship between the existing mobile apps and third-party libraries, especially the third-party library use patterns. Besides, it can be used for recommending potential useful third-party libraries for mobile apps underdeveloped.

Please feel free to use this dataset in your research, and it would be appreciated if you could cite the following paper.

>Diversified Third-Party Library Prediction for Mobile App Development. Q. He, B. Li, F. Chen, J. Grundy, X. Xia and Y. Yang. IEEE Transactions on Software Engineering (2020).


## Dataset Overview
Similar to classical recommendation databases, MALib contains three tables/files, namely apk_info.csv, lib_info.csv, and relation.csv respectively.

### lib_info.csv
|Column 1|Column 2
|---|---|
|Library Id|Library Name|

In this file, we provide the exact name of each third-party library. Those names are gathered from [Maven](https://mvnrepository.com/)  and Github.

### app_info.csv
|Column 1|Column 2
|---|---|
|App Id|App Name|

In this file, we provide the exact name of each app as well as its version. This information is gathered from the meta file of their .apk files.

### relation.csv
|Column 1|Column 2
|---|---|
|App Id|Library Id|

As the usage information of third-party libraries is binary attributes, i.e., 1 stand for the corresponding app has used the corresponding library, and 0 otherwise, we only have two columns in this datasheet. The first column is the id of each app and the second column is the id of each library. For example, when we find a tuple <1,2>, it means app 1 has used library 2. In addition, if we cannot find a tuple <1,5> in this datasheet, it means app 1 hasn't used library 5. 

## Dataset Analysis

The following two figures demonstrate the characteristics of MALib. In general, we find that 92.25\% of these collected apps use 5 TPLs or more third-party libraries, with an average of 11.81.

![Usage Distribution](https://github.com/malibdata/MALib-Dataset/blob/master/Analysis01.png)

In addition, the top 1\% most popular libraries were involved in approximately 29.91\% of the app-library usage records in MALib.

![Usage Distribution](https://github.com/malibdata/MALib-Dataset/blob/master/Analysis02.png)

