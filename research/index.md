---
layout: page
title: Primary Research Projects
image:
  feature: kandersteg2.jpg
comments: false
modified: 2018-01-27
---

### More detail to come...

## Optimization for railroad dispatching

I have written a mixed integer linear optimization model that dispatches trains according to signaling constraints on single track railway lines with passing sidings and does so optimally according to the minimization of a weighted delay measure.

This concept is similar to that used in commercial computer-aided dispatching systems, but those systems have the notable shortcoming of being overridden often in areas with complex dispatching situations. That is, they do not match the behavior of human dispatchers well. I propose to remedy this problem by performing inverse optimization according to known historical data for single track rail lines.

Specifically, the forward optimization problem (dispatching trains) can be tuned to match historical dispatching behavior as closely as possible. The resulting dispatching model is a useful simulation tool that could be used for prediction of train arrivals, assessment of dispatching performance, investigation of track infrastructure layout, and schedule optimization.

Tools:
* Python 2 (with parallel processing)
* AMPL mathematical programming language
* CPLEX optimization solver
* Plotly enhanced visualization
* FFMPEG multimedia processing library
* PostgreSQL database

## Estimating arrival times on freight railroads using machine learning

Numerous methods exist by which to estimate the arrival times (ETAs) of freight trains. Many have been applied to passenger rail, particularly in Europe. But few have investigated the predictability of freight railroads in the United States with large amounts of historical data. Using a dataset from CSX Transportation, I applied machine learning regression techniques on a rich feature set. The features mined from historical railroad operational data included train characteristics, crew information, and network state information.

The dynamics of train operations across route segments is very complex and varied due to numerous factors including topography, locations of passing sidings, and locations of intermediate yards. For this reason, independent regression models were built for a series of discrete points across each route segment. The intuition behind this modeling decision is that the factors contributing to ETA prediction change as the train completes its route. This hypothesis is supported if significant changes are observed in regression feature weights between independent models.

The methodology was tested on sections of the railroad with notoriously varied and unpredictable behavior. ETA predictive performance was compared to that of simple statisitcal methods, which are used in some prediction systems on the railroad. Results showed a consistent 20-30% improvement in prediction accuracy (mean average error) at the beginning of route segments.

Feature weights did indeed change significantly between various regression models on the same route segment. In fact, difficult topographical areas were even identifiable by increased feature weight observed for train tonnage and length.

[Preprint of the journal article.](https://www.dropbox.com/s/ojet2nbntvfeo54/Barbouretal2017.pdf?dl=0)

Tools:
* Python 2
* scikit-learn machine learning library
* pandas data analysis library
* PostgreSQL database with PostGIS spatial extension
* QGIS geographic information system application

## Electric motor failure classification

Predictive maintenance of machinery has recently become a higher-performance methodology compared to traditional condition-based maintenance. This is due to improved sensing capabilities through the internet of things (IoT) and renewed interest in machine learning methods that perform diagnosis well. Fault states as well as machine health values can be predicted in some cases.

We are interested in classifying electric motor failure conditions using accelerometer data, with specific application for traction motors on railroad locomotives. Thus far, machine learning classifiers have been trained and tested on motor data from a test bench with various healthy and failure conditions.

Tools:
* Python 3
* scikit-learn machine learning library
* SciPy scientific computing library
* MATLAB

## Campus mobility mapping and routing

Commercial mapping platforms are excellent at giving directions on public roadways and even for pedestrians and cyclists with consideration for accessibility by these travel modes. However, they are not very capable for pedestrian-focused areas with non-rectilinearity such as a college campus. Nor is good information typically available on these platforms for building names and points of interest.

For these reasons, Vanderbilt University is intersted in developing a campus mobility platform with enhanced functionality for students, staff, faculty, and visitors. Many of the advanced routing techniques used by large-scale mapping systems such as caching, precomputation, and optimized algorithms are not necessary. But campus-specific features such as bike rack locations, building name matching, points of interest, accessible paths, and turn-by-turn directions on unnamed irregular pedestrian ways are more important.

We are developing a prototype backend and frontend for the campus mobility platform that will eventually be integrated as a campus-supported mobile application.

Tools:
* Python 3
* Shapely Python spatial processing
* PostgreSQL database with PostGIS spatial extension
* QGIS geographic information system application

