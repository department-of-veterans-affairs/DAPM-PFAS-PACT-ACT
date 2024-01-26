## Webscraping data from a website and mapping it

<img src="https://github.com/department-of-veterans-affairs/DAPM-PFAS-PACT-ACT/blob/main/2021-2023%20webscrape/2021-2023%20map.jpg">
<p>Figure: This map shows the location of military installations with at least one exceedance of the Environmental Protection Agency (EPA)’s proposed standard of 4 parts per trillion (ppt) in the 2021-2023 dataset. The larger the circle, the higher the concentration of PFAS.
   
</p>

The code in this respository scrapes data from a publicly available website and displays key information on a map so it is easier to understand. Specifically, the code scrapes data from a Department of Defense (DOD) website; cleans, filters, and compares the data to proposed environmental standards; and then maps it so the exceedances of these standards can be easily visualized. 


This repository contains one Jupyter notebook:

A. **Creating and cleaning data for mapping - GH.ipynb.** 

*Inputs*: Two urls that are responses from a Department of Defense (DOD) website. One contains metadata, specifically the geospatial locations for military installations in the United States. The other contains per-and polyfluoroalkyl substances (PFAS) concentrations measured at those installations in JSON format.

*Outputs:* 
1) Multiple data tables that could be exported. The most valuable ones are two data tables that report the highest concentration of PFAS for each military installation reported, whether or not that concentration exceeds EPA's proposed standards and guidelines (either 4 ppt or 70 ppt, respectively), and associated geospatial data for each installation.
2) histogram of concentrations and frequency, displaying a right skew and indicating that the median should be used as the measure of central tendency
3) descriptive statistics throughout to summarize the data
4) map of the highest concentrations that exceeds 4 ppt

The code does the following:
   1. Sends API request to a public DOD website and pulls in geospatial locations for military installtions in the United States and PFAS concentrations measured at those installations in JSON format.
   2. Accesses JSON sublists if needed and converts lists to a pandas dataframe.
   3. Cleans the data by removing nan values and then filters the data a variety of ways, such as by only selecting PFOA and PFOS (forms of PFAS that the EPA has proposed standards for).
   4. Compares the concentrations of PFOA and PFOS to EPA's proposed standard of 4 ppt and identifies samples that exceed this by marking it with a True statement in a column.
   5. Filters the data again in a variety of ways (i.e. selecting only installations that exceed this standard, determining the number of installations with exceedances, determining the number of installations with exceedances and no treatment system).
   6. Filtes the data so only the highest concentration of PFOA or PFOS is selected for each military installation. This allows for easy viewing on a map.
   7. Merges the geospatial locations (i.e. latitude and longitudes) and highest concentration of PFAS for each military installation to allow for mapping. Maps the highest concentrations that exceeds 4 ppt (see figure above)
   8. Reapeats step 4-7 using 70 ppt instead of 4 ppt. 70 ppt is an older guidance threshold for PFAS EPA had published previously.
   9. Cleaning and sorting date fields to determine the span of dates the PFAS samples were collected.
