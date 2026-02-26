# CONVERSION FROM STREM FLOW TO AREA-WEIGHTED RUNOFF

## Overview
- Presents hydrological monitoring site data and a method to convert stream flow to area-weighted runoff for comparability across catchments.
- Documents three monitoring sites related to the Hafren catchment: Carreg Wen (rainfall site) and Lower Hafren (LHF) and Upper Hafren (UHF) catchments.
- Includes per-site metadata (location, physical environment, land management, monitoring window) and a formulaic approach to convert between cumecs and rainfall-runoff measures.

## Site Metadata

- Carreg Wen (Rainfall, CR)
  - Location: Easting 282869, Northing 288588; Latitude 52.4826, Longitude -3.7263; Altitude 575 m
  - Description: Near met. site at Carreg Wen
  - Main soil types: Peat
  - Vegetation: Acid moorland
  - Land management: Rough sheep grazing
  - Mining: NA
  - Start date: 6-Mar-2007
  - End date: 27-Jan-2009
  - Comments: Volume measured using ground-level tipping-bucket rain gauge ~20 m away

- Lower Hafren (Rainfall, LHF)
  - Location: Easting 284281, Northing 287758; Latitude 52.4754, Longitude -3.7052; Altitude 352 m
  - Description: Main Hafren stream channel above lower flume
  - Main soil types: Podzol/Gley
  - Vegetation: 50% plantation Sitka spruce forest with semi-natural moorland headwaters
  - Land management: Phased felling / thinning since 1985
  - Mining: None
  - Start date: 6-Mar-2007
  - End date: 11-Mar-2008
  - Comments: 

- Upper Hafren (Rainfall, UHF)
  - Location: Easting 282842, Northing 289180; Latitude 52.4879, Longitude -3.7269; Altitude 550 m
  - Description: Main Hafren stream channel above forest boundary
  - Main soil types: Peat
  - Vegetation: Semi-natural acid moorland
  - Land management: Very low intensity sheep grazing
  - Mining: None
  - Start date: 6-Mar-2007
  - End date: 27-Jan-2009
  - Comments: 

## Catchment Areas and Data Conversions

- Catchment areas
  - Lower Hafren (LHF): 3.58 km^2
  - Upper Hafren (UHF): 1.22 km^2
  - Note: UHF drainage area is 122 ha to the flow gauging point and 117 ha to the chemistry sampling point

- Conversion equations (to enable comparison between streamflow and area-weighted rainfall/runoff)
  - From cumecs to mm/15min (flow): mm/15min = cumecs × 0.9 / (catchment area in km^2)
  - From mm/15min (flow) to cumecs: cumecs = (mm/15min) × (catchment area in km^2) / 0.9

## Measurement Details and Data Quality Considerations

- Measurement method: Rainfall volume at Carreg Wen is recorded by a ground-level tipping-bucket rain gauge located ~20 m away.
- Data windows: Start and end dates indicate monitoring periods with potential short or missing intervals (e.g., LHF ends in 2008; UHF spans 2007–2009).
- Metadata completeness: Site-level metadata includes soil, vegetation, and land management, enabling hydrological interpretation; some fields are blank, indicating potential gaps.
- Data integration: The explicit conversion formulas support standardized reporting across sites with differing catchment sizes and measurement points, aiding transparency and comparability.

## Relevance for Monitoring Frameworks

- Provides concrete site-level descriptors (location, environment, land use) essential for evaluating environmental health measures and policy impacts.
- Establishes a clear, auditable method to harmonize hydrological data (flow vs. runoff) across catchments of different sizes.
- Supports data governance needs by documenting data collection methods, time windows, and the provenance necessary for quality assurance, transformation, and sharing.
- Highlights potential data challenges common to monitoring programs, such as metadata completeness, measurement gaps, and the need to transform raw data into comparable indicators.