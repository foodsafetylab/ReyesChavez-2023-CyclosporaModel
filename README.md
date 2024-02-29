# ReyesChavez-2023-CyclosporaModel

## Overview
As of August 2023, the two U.S. Food and Drug Administration (FDA) official detection methods for _C. cayetanensis_ are outlined in the FDA Bacteriological Analytical Manual (BAM) Chapters 19b (produce testing) and 19c (agricultural water testing). These newly developed detection methods have been shown to not always detect contamination when present at low levels. Yet, industry and regulators may choose to use these methods as part of their monitoring and verification activities while detection methods continue to be improved. This study uses simulation to better understand the performance of these methods for various produce and water sampling plans. To do so, we used published FDA test validation data to fit a logistic regression model that predicts the methods’ detection rate given the number of oocysts present in a 10-L agricultural water or 25 g produce sample. By doing so, we were able to determine contamination thresholds at which different numbers of samples (_n_ = 1, 2, 4, 8, 16, and 32) would be adequate for detecting contamination. Furthermore, to evaluate sampling plans in use cases, a simulation was developed to represent _C. cayetanensis_ contamination in agricultural water and on cilantro throughout a 45-day growth cycle. The model included uncertainty around the contamination sources, including scenarios of unintentionally contaminated irrigation water or in-field contamination. The results demonstrate that in cases where irrigation water was the contamination source, frequent water testing proved to be more powerful than produce testing. In scenarios where contamination occurred in-field, conducting frequent produce testing or testing produce toward the end of the season more reliably detected contamination. This study models the power of _C. cayetanensis_ detection methods to understand the sampling plan performance and how these methods can be better used to monitor this emerging food safety hazard.

## Usage
This repo contains the model publshed in Journal of Food Protection

### Data Folder
The datafolder contains the CSV files that resulted from the model. 
You can use these csv files to regenerate the paper figures/ 
Use the file CPS Cilantro Scenario Figures.rmd to generate Figures 4 and 5. 
Use the Cilantro Figures 2 and 3 N sample.rmd to generate Figures 2 and 3. 

## Figures Folder
Contains the Figures generated as part of the analysis

## Files in the Main Folder

Files ending in .sav are the logistic regression fits. these are fits generated with the scikit learn module in python. You can import this into the model (an example of this is in the Cilantro Process Model Updated.py file)

### The Cilantro Process Model Updated.py 
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

## Authors
You can view the list of authors in the [AUTHORS](/AUTHORS) file.

## Contact
Corresponding author: Matthew J. Stasiewicz<br>
103 Agricultural Bioprocess Lab<br>
1302 W. Pennsylvania<br>
Urbana, IL, 1361801<br>
USA<br>
+1-217-265-0963<br>
[mstasie@illinois.edu](mailto:mstasie@illinois.edu)

## Citation
Reyes, G. A., Chavez, R. A., & Stasiewicz, M. J. (2023). Modeling Preharvest Cyclospora cayetanensis Sampling and Testing for Various Water and Produce Sampling Plans. _J Food Prot, 86_(11), 100161. [https://doi.org/10.1016/j.jfp.2023.100161](https://doi.org/10.1016/j.jfp.2023.100161)

## License
This project's code is licensed under the GNU General Public License v3.0 and dataset is licensed the Creative Commons Attribution Share Alike 4.0 International license. Please see the [LICENSE.code](/LICENSE.code) and [LICENSE.dataset](/LICENSE.dataset) files for details.

## Acknowledgements & Funding
Funding for the project was made possible by The Center for Produce Safety project 2021CPS10. Any opinions, findings, conclusions, or recommendations expressed in this publication are those of the authors and do not necessarily reflect the view of The Center for Produce Safety. ([https://www.centerforproducesafety.org/](https://www.centerforproducesafety.org/)).
