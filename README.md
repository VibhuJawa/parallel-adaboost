# Parallelizing AdaBoost on Multi Core Machines using open MP in C++

AdaBoost, short for Adaptive Boosting, is a type of boosting algorithm which combines several weak classifiers to create one strong classifier. AdaBoosts fundamental nature doesn’t allow for parallelizing finding the weak classifiers, we present a way which helps achieve nearly 22.14x times the speedup compared to a serial implementaiton. In this project, we develop a parallel AdaBoost algorithm that exploits the multiple cores in a CPU via light weight threads. We propose different algorithms for different types of datasets and machines.



### Prerequisites

Python3: To generate the data set for experimentation

C++ with OpenMP 
Refer this for learning more about open mp and multi threading with C++.
https://bisqwit.iki.fi/story/howto/openmp/


### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

1. Run c++/create_data.sh to create the data set.

2. import the implimentation you like to use, There are 2 header files which you can use:
  
      1. Parallization to find the best feature threhold parallel- [adaboost.h](c++/adaboost.h)   
      2. Parallization everywhere parallel- [adaboost_best.h](c++/adaboost_best.h)
      
      To import simply type:
      
```
#include "adaboost_best.h"


Fit function: 
clf.fit(X,labels,t);

Predict function: 
vector<int> predictions = clf.predict(X); 

X here is a vector of vectors of dimention n*m, 
where n is number of examples and m is number of dimentions.

```
3. We also time different transposse implimentations in  parallel-adaboost/c++/time_transpose.cpp


### Benchmark of Implimentations:
Project Report [parallelizing-adaboost.pdf](https://github.com/VibhuJawa/parallel-adaboost/blob/master/parallelizing-adaboost.pdf)


## Authors
* **Vibhu Jawa** [Vibhu Jawa](https://github.com/VibhuJawa)
* **Praateek  Mahajan** -[Praateek  Mahajan](https://github.com/praateekmahajan)
