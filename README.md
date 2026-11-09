# agri-mark-submetering
Files associated with pre- and post-processing of Agri-Mark PME submetering data

Agri-Mark has a Schneider Power Monitoring Expert (PME) platform installed at their Middlebury creamery. To get the data, a user has to get on the Agri-Mark VPN and use the Reports functionality to download raw data each month. An 'EVT SEM' folder has been setup in the Report Library where a report for each group of data for analysis has been saved: Data Export - Compressed Air, Data Export Refrigeration, Data Export - Wastewater and Data Export - Boiler. The reports have been configured so that all one has to do is hit the 'Generate Report' of the beginning of each month and the prior month's data will be exported in 1-minute intervals.  

This repository is for code written to make engineering analysis easier for the canned reports. 

**data_quality_agrimark.py** -> used to look at all data for a specific month and show data quality statistics and visualize data gaps

**clean_pme_{dataset}_datafile_agrimark.py** -> gives user dropdown with all data files in Data directory to choose which one is cleaned, renames points to more user friendly ones and removes empty columns added by PME for {compressed_air}, {refrigeration} and {wastewater} datasets and saved cleaned data in Data directory in CLeaned_AgriMark {dataset} PME Data Export{month} where month is in _YYYY_MM format. 

**analysis_clean_{dataset}_agrimark.py** -> visualizes cleaned datafiles selected from dropdown menu and saved canned analysis plots in Reports

**The scripts were developed for the following workflow:**

Download files -> rename files replacing the timestamp embedded at end of filename with month (i.e. _2026_10) and save them in Data directory -> run data_quality_agrimark.py script to visualize gaps in data -> run clean_pme_{dataset}_datafile_agrimark.py for compressed_air, refrigeration and wastewater datasets -> run analysis_clean_{dataset}_agrimark.py scripts for visualization -> upload cleaned datasets into Traker in https://veic.sharepoint.com/sites/TrackerEVT/Companies/Forms/AllItems.aspx?id=%2Fsites%2FTrackerEVT%2FCompanies%2F25356%2F%5FSchneider%20PME%20Submetering%20Data&viewid=80b37e57%2De6d7%2D4d7e%2D8ad0%2D5d469fcb14c4 directory
