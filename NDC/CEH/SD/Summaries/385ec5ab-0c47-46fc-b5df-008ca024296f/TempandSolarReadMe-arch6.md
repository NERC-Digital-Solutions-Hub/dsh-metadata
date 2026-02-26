# TempandSolar.csv

## Overview
- Dataset contains temperature and solar radiation measurements for four urine collection trials with Welsh Mountain ewes, conducted in 2016.
- Part of the Uplands-N2O project (Grant NE/M015351/1).
- Weather data sourced from a meteorological station at the sites (Skye Instrument, Llandrindod Wells, UK).

## Data scope and structure
- Trials/sites/seasons:
  - 1) Spring semi-improved
  - 2) Summer semi-improved
  - 3) Autumn semi-improved
  - 4) Autumn improved
- TimeDate field provides date and time in dd/mm/yyyy hh:mm format.
- Measurement intervals:
  - Half-hourly data for semi-improved sites
  - Hourly data for the autumn improved site

## Variables and data types
- Site: Semi-improved or Improved
- Season: Spring, Summer, Autumn (for semi-improved); Autumn (for improved)
- TimeDate: Date and time (dd/mm/yyyy hh:mm)
- SolarRadiation: Incoming solar radiation (W m-2)
- AirTemp: Air temperature (°C)

## Data provenance and authorship
- Authors: Karina A Marsden, Lucy Lush, Jon A Holmberg, Mick J Whelan, Andrew J King, Rory P Wilson, Alice F Charteris, Laura M Cardenas, Davey L Jones, Dave R Chadwick
- Data source: Meteorological station at the study sites (Skye Instrument, Llandrindod Wells, UK)
- Reuse note: If data are reused please ensure it is fully cited

## Usage and considerations
- Potential use: Explore relationships between environmental conditions (temperature and solar radiation) and urine collection trial outcomes; combine with other datasets to create self-serve data products or support analysis related to N2O flux or related studies.
- Considerations:
  - Check data quality and completeness, given multiple sites and differing sampling intervals.
  - Ensure consistent units (SolarRadiation in W/m2; AirTemp in °C) and correct TimeDate parsing, including timezone if relevant.
  - Properly cite the dataset when reusing.