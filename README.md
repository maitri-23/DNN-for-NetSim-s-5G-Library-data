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

To run the files, we can either use jupyter notebook or Google Colab. The folder data contains the necessary csv files. To run the files, tensorflow, pandas, matplotlib needs to be installed on the system and set the path of csv files accordingly. The Google colab already has libraries installed and one needs to upload the csv file to drive to run the program