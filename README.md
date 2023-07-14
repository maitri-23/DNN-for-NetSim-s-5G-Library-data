# DNN for NetSim's 5G Library data

## Model for predicting received power using Log Distance Pathloss formula

Features: Distance, Transmitted Power
Label: Received Power

## Model for predicting SINR in 7-cell scenario with fixed ISD

Features: Distance, Angle
Label: SINR

## Model for predicting SINR in 7-cell scenario with varying ISD

Features: Distance, Angle, ISD
Label: SINR

To run the files, we can jupyter notebook. The folder 'data' contains the necessary csv files. To run the files, tensorflow, pandas, matplotlib needs to be installed on the system. Google colab can also be used as it already has libraries installed but one needs to add lines of codes for uploading the csv file to drive in order to run the program.

## 7-cell hexagonal scenario in NetSim

Create a standard 7-cell scenario in NetSim. A central gNB is placed at (1500, 1500), surrounded by 6 other gNBs at a fixed distance of known as ISD from the central gNB, and at a distance ISD from each other in a hexagonal structure. The UEs are placed in a circular manner around the central gNB at distances from 30m to ISD/2 at an interval of let's say 10m and at diverse angles from 0 to 360 degrees. Obtain X-Y coordinates using distance and polar angles and place the UEs and gNBs in the workspace with the help of rapid scenario generator. After running the simulation for 3GPP pathloss, SINR values are obtained in a log file

## How to obtain data files from NetSim?

### Model for predicting SINR in 7-cell scenario with fixed ISD

We require a csv file containg SINR values at a fixed ISD say, 1000m for a fixed distance 'd' starting from 30m and angles from 0 to 360 degrees with an increment of 10 degrees and so on for 'd+10' upto ISD/2 for training.  For testing, we can keep the angle at a fixed value and take distance values not in the training to obtain SINR values from NetSim in a csv file.

## Model for predicting SINR in 7-cell scenario with varying ISD

Similar to the previous model, we need a csv file for training data containing SINR values, but we vary the ISD from 1000m to 1500m in order to create 6 different NetSim scenarios with changed placement of gNBs to create a NetSim sceanrio. Then we take two ISDs, not used in training in the given range (say, 1150m and 1250m) to create a NetSim sceanrio and obtain SINR values in a csv file.