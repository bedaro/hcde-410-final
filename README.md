# hcde-410-final

This is the final project for HCDE 410. I have examined wind data
around Puget Sound from NOAA's National Centers for Environmental Information
to assess the range of winds that should be considered in Puget Sound water
quality models, and how the limitations and uncertainties in this data might
contribute to model uncertainty.

# Data Sources

Hourly wind speed and direction: ISD-Lite https://www.ncdc.noaa.gov/isd

Direct downloads from this FTP site: ftp://ftp.ncei.noaa.gov/pub/data/noaa/isd-lite

ENSO history: https://origin.cpc.ncep.noaa.gov/products/analysis_monitoring/ensostuff/ONI_v5.php

ENSO data was manually copied/pasted into a CSV, ending in 2020. For each
month of each year, the Oceanic Nino Index (ONI) is given as a three-month
smoothed average.

PDO history: https://www.ncdc.noaa.gov/teleconnections/pdo/

PDO data was downloaded from the above website. For each month and year from
1854 through early 2021, the PDO index is given.

## Licensing of Data

All of the above data is from NOAA/National Weather Service. The following
(disclaimer)[https://www.weather.gov/disclaimer] is attached:

> The information on National Weather Service (NWS) Web pages are in the
> public domain, unless specifically noted otherwise, and may be used without
> charge for any lawful purpose so long as you do not: 1) claim it is your
> own (e.g., by claiming copyright for NWS information -- see below), 2) use
> it in a manner that implies an endorsement or affiliation with NOAA/NWS, or
> 3) modify its content and then present it as official government material.
> You also cannot present information of your own in a way that makes it
> appear to be official government information.
> 
> Use of the NWS name ("National Weather Service") and/or visual identifier
> are protected under trademark law and may not be used without permission
> from the NWS. Use of the NWS name and/ or visual identifier to identify
> unaltered NWS content or links to NWS web sites are allowable uses.
> Permission may be requested for this use at
> https://www.weather.gov/logorequest. Permission is not required to display
> unaltered NWS products which include the NWS name or NWS/NOAA visual
> identifier as part of the original product. Neither the name nor visual
> identifier may be used, however, in a manner that implies an endorsement or
> affiliation with NOAA/NWS.
> 
> Before using information obtained from any NWS Web page special attention
> should be given to the date and time of the data and products being
> displayed.
> 
> The user assumes the entire risk related to its use of information on NWS
> Web pages. NWS is provides such information "as is," and NWS disclaims any
> and all warranties, whether express or implied, including (without
> limitation) any implied warranties of merchantability or fitness for a
> particular purpose. In no event will NWS be liable to you or to any third
> party for any direct, indirect, incidental, consequential, special or
> exemplary damages or lost profit resulting from any use or misuse of this
> data.
> 
> As required by 17 U.S.C. § 403, third parties producing copyrighted works
> consisting predominantly of the material appearing in NWS Web pages must
> provide notice with such work(s) identifying the NWS material incorporated
> and stating that such material is not subject to copyright protection.

# Using the Notebooks

* **FetchClimateData.ipynb** downloads the raw climate data files from NOAA
  for each collection of stations and years, cleans up the data, does some
  preliminary analysis on data availability to identify the stations and
  years of interest, then saves the observations for each dataset to separate
  files.
* **DatasetAnalysis.ipynb** is the full writeup and analysis of the datasets.
