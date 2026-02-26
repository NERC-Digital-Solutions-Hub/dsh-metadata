# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

## Overview
- Physical and biogeochemical measurements of aboveground vegetation biomass and organic carbon content from UK saltmarshes (10 sites) during 2019–2020.
- 144 vegetation surveys using 1 m² quadrats; harvested area of 0.125 m² per quadrat to quantify aboveground biomass (g per m²) and OC content (%), resulting in aboveground carbon (g C m⁻²).
- Data captured in a CSV dataset designed to support blue-carbon assessments across the United Kingdom.

## Location and sampling design
- Geographic scope: saltmarsh sites around the United Kingdom coastline; observations include precise coordinates.
- Location data provided in both decimal degrees (WGS84) and X/Y (Eastings/Northings).
- Site descriptors include Nation and National Vegetation Classification (NVC).
- Marsh zones covered: High marsh, Low marsh, Pioneer marsh.
- Sampling framework: 144 vegetation surveys across ten saltmarshes; each survey uses a 1 m² quadrat from which a 0.125 m² area is harvested.

## Methods

### Field procedures
- Vegetation described according to the British National Vegetation Classification (Rodwell, 2000).
- Harvest within each quadrat: live vegetation harvested from 0.125 m²; dead litter collected from soil surface.
- DGPS used to record precise site location and elevation above ordnance datum.

### Laboratory procedures
- Drying: harvested vegetation oven-dried at 60°C for 72 hours to determine dry biomass.
- Biomass calculation: dry biomass divided by harvested area (0.125 m²) to obtain aboveground biomass (g m⁻²).
- Carbon quantification: milled samples analyzed with Elementar Soli TOC using a temperature-gradient method (DIN 19539) to determine organic carbon percentage (OC%).
- Calibration: Soli TOC calibrated with CaCO₃ and silty soil TOC/ROC/TIC standards (B2290).

### Quality control
- Laboratory equipment calibrated according to University of St Andrews practices.
- Data consistent with referenced methodological standards and calibration procedures.

## Data format and structure

### File formats
- Data resource is provided in .csv format.

### Key variables and headers
- Marsh_ID: Saltmarsh name (text)
- Nation: Nation where site is located (text)
- Collection_Date: Date of sample collection (date/number as described)
- Latitude_dec_degree: Latitude in decimal degrees (number)
- Longitude_dec_degree: Longitude in decimal degrees (number)
- X_easting: X (Eastings) (number)
- Y_northing: Y (Northing) (number)
- Elevation_above_OD_m: Elevation above ordnance datum (m) (number)
- NVC: National Vegetation Classification (text)
- Marsh_Zone: Marsh zone category (text; e.g., High marsh, Low marsh, Pioneer marsh)
- Harvested_Area_m_2: Area of vegetation harvested (m²) (number)
- Biomass_g: Dry biomass (g) (number)
- Aboveground_biomass_g_m_2: Aboveground biomass (g m⁻²) (number)
- OC_Perc: Organic carbon content (%) (number)
- Aboveground_carbon_g_C_m_2: Aboveground carbon (g C m⁻²) (number)

## Data resource description and references
- Data resource descriptions provided for Aboveground_Biomass_Carbon_UK.csv, outlining header definitions and data formats.
- References informing methods and calibration:
  - DIN 19539 (2015) for TOC gradient method.
  - Harvey et al. 2019 on blue-carbon stocks in salt marshes.
  - Natali et al. 2020 on thermal stability of soil carbon pools.
  - Rodwell 2000 (British plant communities, NVC).
  - Smeaton et al. 2021 on marine sedimentary carbon stocks (UK EEZ).

## Implications for environmental monitoring
- Provides standardized, location-linked measurements of aboveground biomass and organic carbon in UK saltmarshes.
- Facilitates temporal and spatial comparisons of blue-carbon stocks across sites.
- Dataset structure supports integration with other environmental data and subsequent policy or management evaluations.