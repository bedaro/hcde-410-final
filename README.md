# hcde-410-final

This is the final project for HCDE 410. I am proposing to examine wind data around
Puget Sound from NOAA's National Centers for Environmental Information to assess the
range of winds that should be considered in Puget Sound water quality models, and how
the limitations and uncertainties in this data might contribute to model uncertainty.

# Data Sources

Hourly wind speed and direction: ISD-Lite https://www.ncdc.noaa.gov/isd

Direct downloads from this FTP site: ftp://ftp.ncei.noaa.gov/pub/data/noaa/isd-lite

ENSO history: https://origin.cpc.ncep.noaa.gov/products/analysis_monitoring/ensostuff/ONI_v5.php

ENSO data was manually copied/pasted into a CSV, ending in 2020. For each
month of each year, the Oceanic Nino Index (ONI) is given as a three-month
smoothed average.

[TODO license, etc]

PDO history: https://www.ncdc.noaa.gov/teleconnections/pdo/

PDO data was downloaded from the above website. For each month and year from
1854 through early 2021, the PDO index is given.

# Using the Notebooks

The notebooks were developed iteratively to work on one data set at a time,
but each can still be run all at once as long as they are run in the correct
order, as listed below:

* **FetchClimateData.ipynb** downloads the raw climate data files from NOAA
  for each collection of stations and years.
* **ProcessClimateData.ipynb** reads all of the raw ISD-Lite climate data files
  and builds a Pandas DataFrame, saved to a compressed HDF file, for each
  station/year collection.
* **AnalyzeAllStationsSince1980.ipynb** examines the complete data set of all
  available climate stations since 1980, determining which stations have data
  available for which years. The findings here were then used to design the
  other data sets.
