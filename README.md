# agri-mark-submetering
Files associated with pre- and post-processing of Agri-Mark PME submetering data

Agri-Mark has a Schneider Power Monitoring Expert (PME) platform installed at their Middlebury creamery. To get the data, a user has to get on the Agri-Mark VPN and use the Reports functionality to download raw data each month. An 'EVT SEM' folder has been setup in the Report Library where a report for each group of data for analysis has been saved: Data Export - Compressed Air, Data Export Refrigeration, Data Export - Wastewater and Data Export - Boiler. The reports have been configured so that all one has to do is hit the 'Generate Report' of the beginning of each month and the prior month's data will be exported in 1-minute intervals.  

This repository is for code written to make engineering analysis easier for the canned reports. 
data_quality_agrimark.py -> used to look at all 
