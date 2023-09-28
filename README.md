# Reyes Chavez Cyclospora Model
## This folder contains the model publshed in Journal of Food Protection

### Data Folder
The datafolder contains the CSV files that resulted from the model. 
You can use these csv files to regenerate the paper figures/ 
Use the file CPS Cilantro Scenario Figures.rmd to generate Figures 4 and 5. 
Use the Cilantro Figures 2 and 3 N sample.rmd to generate Figures 2 and 3. 

## Figures Folder
Contains the Figures generated as part of the analysis

## Files in the Main Folder

Files ending in .sav are the logistic regression fits. these are fits generated with the scikit learn module in python. You can import this into the model (an example of this is in the Cilantro Process Model Updated.py file)

###The Cilantro Process Model Updated.py 
Is the model used to generate Figures 4 and 5. This file contains the process model and all the calculations. The scenarios for Figure 4 start in line 433, as labeled. 
Each scenario of 10,000 iterations will take approximately 1.5 hrs to run. So you can run a lower number of iterations. The results may change slightly from what is reported in the publication due to normal model variability. However, the trends should be the same. 
B1 = refers to daily contamination
B2 - refers to contamination once per season
The Scenarios for figure 5 start in line 1998 as indicated. There are 8 total scenario, 1 per panel of Figure 5

### Product Testinng Analysis.py and Water Testing Analysis.py

These files are used to create the CSV files figures 2 and 3.
The output CSV file from this document is used in the Cilantro Figures 2 and 3 N sample.rmd

### PCR Logisitic Reg Fit

This files was the one used to create the logistc regression fits for the model 
eq 1 and eq2. These fits were achieved with the sklearn module in Python. 
