# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

## Overview
- Physical and biogeochemical measurements of aboveground vegetation biomass from ten UK saltmarshes (2019–2020).
- 144 vegetation surveys across saltmarsh sites to quantify aboveground biomass and organic carbon content in blue carbon environments.

## Dataset contents
- Variables observed: location (latitude/longitude in decimal degrees; X easting, Y northing; elevation above ordnance datum), National Vegetation Classification (NVC), marsh zone (high/low/pioneer), harvested area (m2), biomass (g), aboveground biomass (g m-2), organic carbon content (%), aboveground carbon (g C m-2).
- Sample description: vegetation within 1 m2 quadrats; 0.125 m2 sub-samples harvested per site for biomass calculation; carbon measured on dried plant material.
- Data resource descriptions and header formats are provided to support interpretation and reuse.

## Location and coverage
- Geographic scope: United Kingdom saltmarshes.
- Site positions provided as decimal degrees (WGS84) and as X/Y coordinates; elevation above ordnance datum recorded.
- Site selection aimed to represent variability in coastline, sediment types, and OC content within Scotland and other UK saltmarshes.

## Measurements and variables
- Harvested area: area of vegetation harvested (m2) to calculate biomass.
- Biomass: dry mass of harvested vegetation (g); used to derive aboveground biomass per unit area (g m-2).
- OC_Perc: organic carbon content of vegetation (%).
- Aboveground_carbon_g_C_m_2: calculated aboveground carbon stock (g C m-2).

## Methods and sampling design
- Field sampling: 144 vegetation surveys; 1 m2 quadrats; vegetation described per British National Vegetation Classification (NVC) and 0.125 m2 sub-sampling for biomass.
- Location recording: DGPS used for precise geographic positioning.
- Sample processing: oven-dried vegetation at 60°C for 72 hours; dry biomass weighed; carbon analyzed by elemental analysis (Soli TOC) using the temperature gradient method (DIN 19539).
- Calibration: Soli TOC calibrated with CaCO3 and standardized TOC/ROC/TIC references.

## Data handling, QA and calibration
- Quality control: laboratory equipment calibrated according to University of St Andrews practices.
- Data management: describes data structure, header formats, and units to support data quality and reproducibility.
- Statistical treatment: not applicable (NA) in the dataset documentation.

## Data formats and metadata
- File format: CSV.
- Data resource descriptions and header definitions included to aid interpretation (e.g., Marsh_ID, Nation, Collection_Date, Latitude/Longitude, Elevation, NVC, Marsh_Zone, Harvested_Area_m2, Biomass_g, Aboveground_biomass_g_m2, OC_Perc, Aboveground_carbon_g_C_m_2).

## Data governance, access, and sharing
- Emphasizes the importance of data openness, metadata completeness, and sharing underlying data to enable scrutiny and reuse.
- Acknowledges potential barriers to using some data due to public sharing requirements and metadata gaps.
- Data quality and provenance clearly documented to support governance and future data integration.

## References
- DIN 19539 (2015/2018) – methodology for total carbon differentiation.
- Harvey et al. (2019) – no detectable broad-scale grazing effect on blue-carbon stock in salt marshes.
- Natali et al. (2020) – thermal stability of soil carbon pools.
- Rodwell (2000) – British vegetation classification reference.
- Smeaton et al. (2021) – marine sedimentary carbon stocks in UK EEZ.