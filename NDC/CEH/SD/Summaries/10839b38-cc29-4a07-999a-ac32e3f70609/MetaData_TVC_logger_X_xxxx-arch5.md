# Soil temperature, soil moisture, air temperature and relative humidity for main vegetation types at SikSik Creek, nr. Trail Valley Creek, NWT, Canada.

## Overview
- Data structure: 5 CSV files, each corresponding to one logger in each vegetation type.
  - Filenames: TVC_logger 1_sedge.csv; TVC_logger 2_riparian.csv; TVC_logger 3_betula.csv; TVC_logger 4_alder.csv; TVC_logger 5_lichen heath.csv
- Authors/Owner: Lorna Street and Philip Wookey
- Maintainer: Lorna Street
- Contact: l.e.street@ed-alumni.net
- Period of record (per logger):
  - Logger 1: 02-Aug-2013 to 29-Jul-2015
  - Logger 2: 02-Aug-2013 to 21-Aug-2015
  - Logger 3: 02-Aug-2013 to 21-Aug-2015
  - Logger 4: 02-Aug-2013 to 21-Aug-2015
  - Logger 5: 02-Aug-2013 to 29-Jul-2015
- Location and GPS:
  - SikSik Creek catchment, Trail Valley Creek, NWT, Canada
  - Logger 1: 68.74459771 N, 133.5021632 W
  - Logger 2: 68.74533925 N, 133.4939524 W
  - Logger 3: 68.74526449 N, 133.4925088 W
  - Logger 4: 68.74516902 N, 133.4952195 W
  - Logger 5: 68.74549767 N, 133.4969109 W
- Data volume:
  - Logger 1: 418,072 records
  - Logger 2: 539,115 records
  - Logger 3: 539,115 records
  - Logger 4: 539,110 records
  - Logger 5: 418,060 records

## Data content and structure
- Measured variables (10-minute intervals; continuous data, no gap-filling):
  - Soil temperature at 5 cm depth (Tsoil.C; °C)
  - Air temperature (Tair.C; °C)
  - Relative humidity (RH.percent; %)
  - Volumetric water content (VWC.m3.per.m3; m3 m-3)
  - Surface wetness (Wetness.percent; %); measured only at the lichen heath location
- Depths and sensor details:
  - Soil temperature: 5 cm depth using Onset 12-bit Temperature Smart sensors
  - Soil VWC: 5 cm depth using ECH2O EC-5 sensors (factory calibration)
  - Air temperature and RH: measured at ~0.5 m above ground with radiation shielding; sensor type specified (Onset Temperature Smart sensors or Onset Temperature/Relative Humidity Smart sensors)
  - Surface wetness: Onset Leaf wetness sensor (only at lichen heath)
- Not all variables are present at every location:
  - Logger 1: soil temperature, air temperature, RH, soil VWC
  - Logger 2: soil temperature, air temperature, RH, soil VWC (Sphagnum moss) and soil VWC (under willow shrub)
  - Logger 3: soil temperature (hummock), air temperature, RH, soil VWC (hummock) and soil VWC (interhummock)
  - Logger 4: soil temperature (hummock), air temperature, RH, soil VWC (hummock) and soil VWC (interhummock)
  - Logger 5: soil temperature (hummock), surface wetness, soil VWC (hummock) and soil VWC (interhummock)

## Variable definitions and units
- Record: Record number (no unit)
- DateTime: Date and time (dd/mm/yyyy HH:MM:SS)
- Tsoil.C: Soil temperature at 5 cm depth (°C)
- Tair.C: Air temperature (°C)
- RH.percent: Relative humidity (%)
- VWC.m3.per.m3: Volumetric water content (m3 m-3)
- Wetness.percent: Surface wetness (%)

## Data governance and provenance
- Data ownership and stewardship clearly documented (authors, maintainer, contact).
- Metadata includes per-logger period of record, exact locations (GPS), and sensor/measurement details.
- Data format is CSV with defined variable names, units, and missing value code (period/dot).
- Data quality notes:
  - 10-minute interval measurements with no gap-filling; continuous records.
  - Calibration information noted where applicable (factory calibration for VWC sensors).
  - Variability in measured variables across loggers due to site-specific conditions (e.g., hummock vs interhummock, presence/absence of surface wetness measurement).
- Data access and reuse:
  - Contact maintained for data access and questions (Lorna Street).
  - Documentation provides sufficient detail for discovery, interpretation, and reuse by data users and other stakeholders.

## Takeaways for data stewardship
- The dataset adheres to clear metadata, sensor specifications, and time-resolution standards suitable for long-term environmental monitoring.
- Important considerations for reuse:
  - Account for site- and logger-specific variable availability.
  - Respect the 10-minute sampling cadence and noted measurement depths.
  - Use the per-logger period of record and GPS coordinates to align with other spatial datasets.
  - Refer to the exact variable definitions and units to ensure consistent analysis and integration with other data sources.