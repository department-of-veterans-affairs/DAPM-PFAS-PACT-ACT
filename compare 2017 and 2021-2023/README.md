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

<b>Outputs:</b> A single dataframe containing joined data for military installations present in both the 2017 and 2021-2023 datasets. 22 installations were present in both. Two of the installations reported concentrations that were higher in 2021-2023 than 2017. The rows for these installations were highlighted. 

<b>Methods:</b>
1. Import stored 2017 and 2021-2023 dataframes.
2. Rename some of the military installations in both dataframes in order to improve the match.
3. Use fuzzy matching to create a dataframe which contains a similarity score for the best match between the two dataframes based on military installation name.
4. Filter the fuzzy dataframe to only keep installations with a similarity score greater than or equal to 87%.
5. Filter the 2017 dataframe to only keep specific columns needed.
6. Join / merge the 2017 dataframe to the fuzzy dataframe.
7. Highlight rows where the concentrations in 2021-2023 was higher than in 2017. 