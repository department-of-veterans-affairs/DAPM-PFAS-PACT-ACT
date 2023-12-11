<h1>Adding spatial data to the 2017 PFAS data</h1>


<img src="https://github.com/department-of-veterans-affairs/DAPM-PFAS-PACT-ACT/blob/main/2017%20spatial/map%202018%20image.JPG">



The code in this repository adds spatial data from one dataframe to another using fuzzy matching. It specifically finds matches between military installation names present in both a dataframe that contains spatial data and another dataframe that contains hazardous waste, specifically Per- and polyfluoroalkyl substances (PFAS), concentrations in drinking water. 

All data was scraped from the Department of Defense's publicly available PFAS website: https://www.acq.osd.mil/eie/eer/ecc/pfas/map/pfasmap.html

<b>Highlighted capabilities:</b>

<i>1. Add spatial data to a dataframe that previously did not have spatial data.</i> This allowed for the data to be mapped. 

<i>2. Automating some of the matching process using fuzzy matching.</i>

<i>3. Joining data from one dataframe to another.</i>

<b>Inputs:</b>

<i>1. Spatial dataframe.</i> Dataframe containing 703 military installations and their latitude and longitude coordinates. Please see the "2021-2023 webscrape" folder for the code that webscrapes the spatial data. 

<i>2. 2017 PFAS dataframe. </i> Dataframe that contains hazardous waste, specifically PFAS concentrations in drinking water collected as of 2017. Please see the "2017 PDF scrape" folder for the code that scrapes a PDF file for the PFAS data. 

<b>Output:</b> A single dataframe that has the 2017 PFAS data with spatial data attached. Spatial data was found and joined for 48 out 55 unique installations. 

<b>Methods</b>
1. Import stored spatial and PFAS dataframes.
2. Rename some of the military installations in the spatial dataframe in order to improve the match.
3. Use fuzzy matching to create a dataframe which contains a similarity score for the best match between the two dataframes based on military installation name.
4. Filter the fuzzy dataframe to only keep installations with a similarity score greater than or equal to 87%. 
5. Filter the spatial dataframe to only keep specific columns needed.
6. Join / merge the spatial dataframe to the fuzzy dataframe.
7. Filter the merged dataframe to only keep specific columns.
8. Calculate the number of unique military installations by name.
9. Export merged and filtered dataframe to .csv for use in a mapping application. 
