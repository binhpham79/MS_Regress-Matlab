# MS_Regress-Matlab

This repository provides functions (and examples scripts) for the estimation, simulation and forecasting of a general Markov Regime Switching Regression in Matlab. 

Before using the package, make sure you read the pdf file (About the MS_Regress_Package.pdf) in the downloaded zip file. A copy of this paper can be found in [SSRN](https://ssrn.com/abstract=1714016).

## Instalation

First, clone this repository or download it as a zip file (see download choice in right side button of the webpage). 
 
Matlab works by reading files in the search path. In order to use the functions of MS_Regress, all you need to do is to tell matlab to look for the files in the m_Files folder (e.g. addpath('m_Files') of the zip file.  After that, all functions will be available to the user.

The easiest way to get started is to run the example scripts provided in the root folder. They should work **as is**, without any modification. You can modify the examples for you own dataset and custom model. 

I also wrote a R version of the package (fMarkovSwitching). It is public available in the R Metrics project and in R Code section of my [website](https://sites.google.com/site/marceloperlin/). Please be aware that the R version in no longer being maintained so it is actually an older version of the matlab package with only the basic features.   

## Features of the package: 

- Support for univariate and multivariate models;
- Support of any number of states and any number of explanatory variables;
- Estimation, by maximum likelihood, of any type of switching setup for the model. This means that you can choose which coefficients in the model, including distribution parameters, are switching states over time;
- A wrapper function for the estimation of regime switching autoregressive models, including multivariate case (MS-VAR) is included in the package;
- The values of parameter's standard errors can be calculated with 2 different methods;
- Includes a C version of hamilton’s filter that may be used for speeding up the estimation function (see pdf for details);
- Possibility of three distinct distribution assumptions for residual vector (Normal, t or GED);
- The user can choose the optimizing function to be used in the estimation of the model (fminsearch, fmincon or fminunc);
- Support for reduced/constrained estimation (see pdf document for details);
- Several example scripts that show how to use the code;

## Limitations of the package (so far): 

- The EM algorithm is not implemented (all models are estimated by direct maximization of log likelihood function);
- It does not support state space models with markov switching effects;
- It cannot estimate a model with time varying transition probabilities (TVPT). But, Zhuanxin Ding has developed a matlab package for TVTP models based on MS_Regress. You can access it here;
- It does not support models with garch type of filters for conditional volatility;

 

## Required Products:  

Optimization, Statistics

## References:
    
Alexander, C. (2008) ‘Market Risk Analysis: Practical Financial Econometrics’ Wiley. 

Brooks, C. (2002) ‘Introduction to Econometrics’ Cambridge University Press. 

Hamilton, J., D. (2005) Regime Switching Models. Palgrave Dictionary of Economics, (available at http://dss.ucsd.edu/~jhamilto/palgrav1.pdf ) 

Hamilton , J., D. (1994) ‘Time Series Analysis’ Princeton University Press. 

Kim, C., J., Nelson, C., R. (1999) State Space Model with Regime Switching: Classical and Gibbs-Sampling Approaches with Applications. The MIT press. 
 