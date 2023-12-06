<h1>Per- and polyfluoroalkyl substances (PFAS) in drinking water on or near military installations, 2017 and 2021-2023</h1>

<img src= 'https://github.com/department-of-veterans-affairs/DAPM-PFAS-PACT-ACT/blob/main/map%202018%20image.JPG'>


This repository contains the Python code that scrapes, cleans, and maps data on the concentrations of per- and polyfluoroalkyl substances (PFAS) collected in drinking water systems on or near military installations. This data is publicly available on the Department of Defense PFAS website: https://www.acq.osd.mil/eie/eer/ecc/pfas/index.html. DOD collected these samples to identify potential impacts of PFAS resulting from DOD activities. There are two sets of data, one dated as of August 31, 2017 and the other dated 2021 and 2023. The 2021-2023 data was scraped from DOD's public PFAS website: https://www.acq.osd.mil/eie/eer/ecc/pfas/map/pfasmap.html. The 2017 data was scraped from a PDF file also available on DOD's PFAS website: https://www.denix.osd.mil/derp/denix-files/sites/26/2018/03/FY18-HASC-Brief-on-PFOS-PFOA_Mar2018.pdf.

The PFAS concentrations displayed are either Perfluorooctanoic acid (PFOA) or Perfluorooctane sulfonic acid (PFOS) which are members of the PFAS chemical group. For the 2021-2023 data, only one PFOS or PFOA concentration is displayed for each military base, specifically the highest concentration of either PFOS or PFOA that was reported in the dataset. 

For the 2017 data, the concentrations were reported as a combination of PFOA and PFOS or the analyte was unspecified. Only one concentration is reported for each base with the exception that some bases had concentrations reported both on and off the base. In this situation, the highest concentration for both scenarios were reported. 

 EPA has presented to concentration thresholds for PFAS to be used for evaluating the risk of PFOA and PFOS in drinking water to human health: 70 parts per trillion (ppt) and, more recenlty, 4 ppt. For the 2021-2023 data, one table is created that has a Boolean value (True / False) indidcating if the sample results exceeds 70 ppt and another that adjust this threshold to 4 ppt. For the 2017 data, all concentrations were reported above 70 ppt. 
 
If a result cell in the attribute table is blank, no concentrations were detected. 

The "2017 PDF scrape" folder contains code that scrapes the 2017 data from the PDF file. 

The "2017 spatial" contains code that joins this data to spatial data, allowing the data to then be mapped. 

The "2021-2023 webscrape" folder contains code that scrapes the 2021-2023 from a website using an API and then maps it using geopandas. 

The "compare 2017 and 2021-2023" contains code that looks for overlap in military installations in the 2017 and 2021-2023 datasets and compares the sample results. 


The "PFAS PACT Act data dictionary.xlsx" file contains information on each of the tables generated in the code. There are .csv files that are created throughout the code. The data dictionary defines what is contained in those .csv files and then subsequent tabs define the columns in those .csv tables. 
