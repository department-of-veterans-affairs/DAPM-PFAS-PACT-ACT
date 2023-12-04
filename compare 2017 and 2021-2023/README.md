<h1> Comparing Per- and Polyfluoroalkyl Substances (PFAS) concentrations collected in 2017 v. 2021-2023. </h1>

This code compare PFAS concentrations collected in drinking water on or near military installations in 2017 v. 2021-2023. 22 military installations were in both datasets. The report that presented the 2017 concentrations was dated March 2018, which is why 2018 is used in the code. 

All data was scraped from the Department of Defense's publicly available PFAS website: https://www.acq.osd.mil/eie/eer/ecc/pfas/map/pfasmap.html. 

<b>Highlighted Capabilities:</b>
<i>1. Automating some of the matching process using fuzzy matching.</i>

<i>2. Joining data from one dataframe to another. </i>

<i>3. Highlighting rows if the concentrations in 2018 were lower than concentrations in 2021-2023.</i> Note the highlighting does not appear on GitHub. 

<b>Inputs:</b>

<i>1. 2017 PFAS dataframe. Dataframe that contains PFAS concentrations in drinking water on or near military installations collected as of 2017.</i> Please see the "DAPM-PFAS-2017-PDF-scrape" folder in this repository for the code that scrapes a PDF file for the 2017 data. 

<i>2. 2021-2023 PFAS dataframe. Dataframe that contains PFAS concentrations in drinking water on military installations collected in 2021-203.</i> Please see the "DAPM-PFAS-2021_2023_webscrape" folder in this repository for the code that webscrapes the 2021-2023 data. 
