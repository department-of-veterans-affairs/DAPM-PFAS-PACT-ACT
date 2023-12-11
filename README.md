<h1>Per- and polyfluoroalkyl substances (PFAS) in drinking water on or near military installations, 2017 and 2021-2023</h1>

<img src= 'https://github.com/department-of-veterans-affairs/DAPM-PFAS-PACT-ACT/blob/main/map%202018%20image.JPG'>


This repository contains the Python code that scrapes, cleans, and maps data on the concentrations of per- and polyfluoroalkyl substances (PFAS) collected in drinking water systems on or near military installations. This data is publicly available on the Department of Defense (DOD)'s PFAS website: https://www.acq.osd.mil/eie/eer/ecc/pfas/index.html. There are two sets of data, one dated as of August 31, 2017 and the other dated 2021-2023. The 2021-2023 data was scraped directly from DOD's PFAS website using an API: https://www.acq.osd.mil/eie/eer/ecc/pfas/map/pfasmap.html. The 2017 data was scraped from a PDF file also available on DOD's PFAS website: https://www.denix.osd.mil/derp/denix-files/sites/26/2018/03/FY18-HASC-Brief-on-PFOS-PFOA_Mar2018.pdf. The year "2018" is occassionaly used in reference to the 2017 data because the report the data was scraped from is dated "March 2018." The words military "installation" and "bases" are used interchangeably in the code. 

The PFAS concentrations displayed are either Perfluorooctanoic acid (PFOA) or Perfluorooctane sulfonic acid (PFOS) which are members of the PFAS chemical group. For the 2017 data, the concentrations were reported mostly as a combination of PFOA and PFOS or the analyte was unspecified.

The Environmental Protection Agency (EPA) has presented concentration thresholds to be used for evaluating the risk of PFOA and PFOS in drinking water to human health: 70 parts per trillion (ppt) for either PFOS or PFOA separate or combined and, more recenlty, 4 ppt for either PFOS or PFOA. For the 2021-2023 data, the sample results are compared to both thresholds in separate tables. For the 2017 data, all military installations reported concentrations, specifically a combination of PFOS and PFOA concentrations, in drinking water that were above 70 ppt. 
 
If a cell in the "results" column in a table is blank, no concentrations were detected or reported. 

<b> Folders and files contained in this repository:</b>

<i>1. 2017 PDF scrape:</i> folder that contains code that scrapes the 2017 data from the PDF file. 

<i>2. 2017 spatial:</i> folder that contains code that joins spatial data to the 2017 data, allowing the 2017 concentrations to be mapped. 

<i>3. 2021-2023 webscrape:</i> folder that contains code that scrapes the 2021-2023 from a website using an API and then maps it using geopandas. 

<i>4. compare 2017 and 2021-2023:</i> folder that contains code that identifies military installations reported in both the 2017 and 2021-2023 datasets and compares the sample results. 

<i>5. PFAS PACT Act data dictionary.xlsx:</i> file that contains information on each of the tables generated in the code. There are .csv files that are created throughout the code. The data dictionary defines what is contained in those .csv files and then subsequent tabs define the columns in those .csv tables. 
