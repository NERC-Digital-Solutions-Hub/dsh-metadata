# Datafiles

## Overview
- A directory listing of datafiles with descriptions and time periods, plus three supporting documents: Datafiles.rft (file overview and time period), Study Sites.rtf (information on the three study sites), and Methods.rtf (brief methods used to collect data and contents of datafiles).
- Data files are primarily in CSV format; metadata and context are provided in the accompanying RTF documents.

## Data files by study site

- Semi-mature forest site
  - Forest_Rainfall_raw.csv — raw rainfall data; time period 03-10-2014 to 30-09-2015
  - Forest_Rainfall_processed.csv — 5-minute rainfall data; time period 01-10-2014 to 30-09-2015
  - Forest_micrometeorology.csv — 10-minute weather data; time period 15-10-2014 to 30-09-2015
  - Forest_Throughfall_automatic.csv — 5-minute throughfall data (gutters); time period 01-10-2014 to 30-09-2015
  - Forest_Throughfall_manual.csv — throughfall data from manual gauges; time period 01-10-2014 to 30-09-2015
  - Forest_Stemflow_raw.csv — raw stemflow data; time period 16-2-2015 to 30-09-2015
  - Forest_Stemflow_processed.csv — processed stemflow data; time period 16-2-2015 to 30-09-2015
  - Forest_Sapflow_raw.csv — temperature data used to estimate sap flux density; time period 01-10-2014 to 01-10-2015
  - Forest_Sapflow_processed.csv — sap flux density and sap flow data; time period 01-10-2014 to 01-10-2015
  - Forest_Soilmoisture_raw.csv — raw soil moisture data; time period 15-10-2014 to 01-10-2015
  - Forest_Soilmoisture_processed.csv — processed soil moisture data; time period 15-10-2014 to 01-10-2015
  - Forest_Overlandflow.csv — daily runoff data (overland flow) for the semi-mature site; time period partially shown as 01-10-2014 to (incomplete in listing)

- Young forest site (ReforestedTF)
  - ReforestedTF_Rainfall_raw.csv — raw rainfall data; time period 02-10-2014 to 28-09-2015 (note formatting variations)
  - ReforestedTF_Rainfall_processed.csv — 5-minute rainfall data; time period 01-10-2014 to 30-09-2015
  - ReforestedTF_micrometeorology.csv — 10-minute weather data; time period 15-10-2014 to 30-09-2015
  - ReforestedTF_Throughfall_automatic.csv — 5-minute throughfall data for gutters; time period 01-10-2014 to 30-09-2015
  - ReforestedTF_Throughfall_manual.csv — manual gauges throughfall data; time period 01-10-2014 to 30-09-2015
  - ReforestedTF_Stemflow_raw.csv — raw stemflow data; time period 17-02-2015 to 30-09-2015
  - ReforestedTF_Stemflow_processed.csv — processed stemflow data; time period 17-02-2015 to 30-09-2015
  - ReforestedTF_Sapflow_raw.csv — temperature data for sap flux estimation; time period 01-10-2014 to 30-09-2015
  - ReforestedTF_Sapflow_processed.csv — sap flux density and sap flow data; time period 01-10-2014 to 01-10-2015
  - ReforestedTF_Soilmoisture_raw.csv — raw soil moisture data; time period 01-10-2014 to 10-10-2015
  - ReforestedTF_Soilmoisture_processed.csv — processed soil moisture data; time period 01-10-2014 to 01-10-2015
  - ReforestedTF_Overlandflow.csv — daily runoff data for the reforested (young forest) site; time period 01-10-2014 to 30-09-2015

- Degraded grassland site
  - Degradedland_Rainfall_raw.csv — raw rainfall data; time period around 02-10-2014 to 29-09-2015 (formatted as “30-09-2015 = …”)
  - Degradedland_Rainfall_processed.csv — 5-minute rainfall data; time period 01-10-2014 to 30-09-2015
  - Degradedland_micrometeorology.csv — 10-minute weather data; time period 01-10-2014 to 01-10-2015
  - Degradedland_Soilmoisture_raw.csv — raw soil moisture data; time period around 15-10-2014 to 01-10-2015
  - Degradedland_Soilmoisture_processed.csv — processed soil moisture data; time period around 15-10-2014 to 01-10-2015
  - Degradedland_Overlandflow.csv — daily runoff data; time period 01-10-2014 to 30-09-2015
  - Degradedland_Soil_Heat_flux.csv — soil heat flux data; time period 01-10-2014 to 30-09-2015

## Formats and documentation
- Primary data formats: CSV for numerical/time-series data; RTF for metadata and site/method descriptions.
- Related documentation files: Datafiles.rft (overview of files and time periods), Study Sites.rtf (site descriptions), Methods.rtf (data collection methods and contents).

## How this supports GIS work
- Provides multi-variable, time-stamped environmental datasets suitable for map-based analysis and visualization.
- Enables cross-site comparisons (semi-mature forest, young forest, degraded grassland) and integration of rainfall, micrometeorology, hydrological responses (throughfall, stemflow, sapflow, soil moisture, overlandflow) into GIS data layers.
- Data are available in both raw and processed forms, allowing for custom cleaning, standardization, and spatial-temporal analyses across different resolutions.