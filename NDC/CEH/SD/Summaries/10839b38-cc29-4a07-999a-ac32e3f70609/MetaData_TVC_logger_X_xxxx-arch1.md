# Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Overview
- A dataset consisting of 5 CSV files, each corresponding to a single logger located within different vegetation types at SikSik Creek, Trail Valley Creek, NWT, Canada.
- Logs cover the period from 2013 to 2015 with 10-minute interval measurements.
- Variables measured include soil temperature, soil volumetric water content, air temperature, relative humidity, and surface wetness (at one location).

## Data contents and structure
- Files and vegetation types:
  - TVC_logger 1_sedge.csv
  - TVC_logger 2_riparian.csv
  - TVC_logger 3_betula.csv
  - TVC_logger 4_alder.csv
  - TVC_logger 5_lichen heath.csv
- Each file contains records from a single logger; data are recorded every 10 minutes and are continuous with no gap-filling.
- Record structure:
  - Record number
  - Date and Time (DateTime, format: dd/mm/yyyy HH:MM:SS)

## Measurements and sensors
- Soil temperature (Tsoil.C) at 5 cm depth using Onset 12-bit Temperature Smart sensors.
- Air temperature (Tair.C) measured approximately 0.5 m above ground; shielded from radiation.
- Relative humidity (RH.percent) measured with Onset 12-bit Temperature/Relative Humidity Smart sensors (where applicable).
- Soil volumetric water content (VWC.m3.per.m3) measured at 5 cm depth with ECH2O EC-5 sensors (calibrated where possible; measurements for hummock and inter-hummock positions as applicable).
- Surface wetness (Wetness.percent) measured at the lichen heath location using an Onset Leaf Wetness sensor (only present in Logger 5).
- Not all variables are captured at every location:
  - Logger 1: Tsoil.C, Tair.C, RH, VWC
  - Logger 2: Tsoil.C, Tair.C, RH, VWC (Sphagnum moss) and VWC (under willow shrub)
  - Logger 3: Tsoil.C (hummock), Tair.C, RH, VWC (hummock), VWC (interhummock)
  - Logger 4: Tsoil.C (hummock), Tair.C, RH, VWC (hummock), VWC (interhummock)
  - Logger 5: Tsoil.C (hummock), Wetness.percent, VWC (hummock), VWC (interhummock)

## Time period
- Logger 1: 02-Aug-2013 to 29-Jul-2015
- Logger 2: 02-Aug-2013 to 21-Aug-2015
- Logger 3: 02-Aug-2013 to 21-Aug-2015
- Logger 4: 02-Aug-2013 to 21-Aug-2015
- Logger 5: 02-Aug-2013 to 29-Jul-2015

## Location coordinates
- Logger 1: 68.74459771 N, 133.5021632 W
- Logger 2: 68.74533925 N, 133.4939524 W
- Logger 3: 68.74526449 N, 133.4925088 W
- Logger 4: 68.74516902 N, 133.4952195 W
- Logger 5: 68.74549767 N, 133.4969109 W

## Metadata, authors, and contact
- Authors/Owners: Lorna Street; Philip Wookey
- Maintainer: Lorna Street
- Contact: l.e.street@ed-alumni.net

## Data quality and notes
- Data are continuous with no gap-filling.
- Not all variables are measured at every location; users should reference the per-logger variable set for analyses.
- Units:
  - Tsoil.C: degrees Celsius
  - Tair.C: degrees Celsius
  - RH.percent: percent
  - VWC.m3.per.m3: m3/m3
  - Wetness.percent: percent
- DateTime format: dd/mm/yyyy HH:MM:SS
- Missing value codes: represented by a period (.) in the dataset.