# CONVERSION FROM STREM FLOW TO AREA-WEIGHTED RUNOFF

- What this document describes
  - A dataset detailing rainfall measurement sites and Hafren catchments, including site codes, coordinates, physical characteristics, land management, measurement method, and collection periods.
  - A conversion framework to translate stream flow (cumecs) to area-weighted runoff (mm/15min) and vice versa, for two catchments.

- Site details
  - Rainfall site (CR)
    - Location: LAT 52.4826, LONG -3.7263; ALT 575 m
    - Description: Near met. site at Carreg Wen
    - Environment: MAIN SOIL TYPES = Peat; VEGETATION = Acid moorland
    - Land management: Rough sheep grazing
    - Data period: START 6-Mar-2007, END 27-Jan-2009
    - Measurement note: Volume measured using ground-level tipping-bucket rain gauge ~20 m away
  - Lower Hafren (LHF)
    - Location: LAT 52.4754, LONG -3.7052; ALT 352 m
    - Description: Main Hafren stream channel above lower flume
    - Environment: MAIN SOIL TYPES = Podzol/Gley; VEGETATION = 50% plantation Sitka spruce forest with semi-natural moorland headwaters
    - Land management: Phased felling / thinning since 1985
    - Data period: START 6-Mar-2007, END 11-Mar-2008
  - Upper Hafren (UHF)
    - Location: LAT 52.4879, LONG -3.7269; ALT 550 m
    - Description: Main Hafren stream channel above forest boundary
    - Environment: MAIN SOIL TYPES = Peat; VEGETATION = Semi-natural acid moorland
    - Land management: Very low intensity sheep grazing
    - Data period: START 6-Mar-2007, END 27-Jan-2009

- Catchment information
  - Lower Hafren (LHF): Catchment area = 3.58 km²
  - Upper Hafren (UHF): Catchment area = 1.22 km²
    - Note: UHF drainage area is 122 ha to the flow gauging point and 117 ha to the chemistry sampling point

- Data conversion formulas
  - From cumecs to mm/15min (flow to area-weighted runoff)
    - mm/15min = cumecs × 0.9 ÷ catchment_area_km2
  - From mm/15min to cumecs (area-weighted runoff to flow)
    - cumecs = mm/15min × catchment_area_km2 ÷ 0.9

- Practical implications for data leaders
  - Defines a structured set of site metadata (location, environment, management) and their collection periods for governance, discoverability, and metadata quality.
  - Provides explicit conversion rules to harmonize flow and rainfall-based runoff metrics across catchments of known areas.
  - Supports data interoperability between hydrological measurements (cumecs) and hydro-meteorological runoff (mm/15min) for decision-making and reporting.