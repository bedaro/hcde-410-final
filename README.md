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
