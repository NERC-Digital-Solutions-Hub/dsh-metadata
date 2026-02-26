# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

- What the dataset contains: Physical and biogeochemical measurements of aboveground vegetation biomass from across ten UK saltmarshes, collected in 2019–2020; 144 vegetation surveys aimed at quantifying aboveground biomass and organic carbon content in blue carbon environments across the United Kingdom.

- Location and sampling design: Sites selected around the UK coastline (including Scotland) to represent saltmarsh vegetation, sediment types, and organic carbon content. Observations provided in decimal degrees (WGS84) and as X (Easting) and Y (Northing) coordinates. DGPS used for precise location and elevation above ordnance datum. At each site, a 1 m2 quadrat was sampled; within quadrats, 0.125 m2 areas were harvested.

- Variables and data structure: Key fields include:
  - Marsh_ID (saltmarsh name)
  - Nation
  - Collection_Date
  - Latitude_dec_degree, Longitude_dec_degree
  - X_easting, Y_northing
  - Elevation_above_OD_m
  - NVC (National Vegetation Classification)
  - Marsh_Zone (e.g., High/Low/Pioneer marsh)
  - Harvested_Area_m_2
  - Biomass_g (dry biomass)
  - Aboveground_biomass_g_m_2
  - OC_Perc (organic carbon content)
  - Aboveground_carbon_g_C_m_2

- Methods and procedures: 
  - Field: 144 vegetation surveys; vegetation described per British NVC (Rodwell, 2000); harvest of 0.125 m2 per quadrat; live vegetation cut at soil level; dead litter collected.
  - Laboratory: drying at 60°C for 72 hours; dry biomass weighed; OC quantified by milling dried samples and analyzing ~50 mg with a Soli TOC (temperature gradient method) following DIN 19539 (Natali et al., 2020; Smeaton et al., 2021).
  - Calibration: Soli TOC calibrated with CaCO3 and standard materials (B2290).
  - Data processing: Biomass per harvested area calculated to obtain aboveground biomass (g m-2) and aboveground carbon (g C m-2); statistical treatment noted as NA.

- Data quality and checks: Laboratory equipment calibrated according to University of St Andrews practices; data checks performed; “NA” indicates not applicable or missing data in specified fields.

- File formats and data structure: Data resource provided as CSV (.csv); accompanying data resource descriptions and header mappings specify column descriptions and formats (e.g., Description, Cell Format; text vs. number vs. date).

- References and methodological context: 
  - DIN 19539: 2015–08 for TOC methodology
  - Harvey et al., 2019 (blue-carbon soil effects)
  - Natali et al., 2020 (TOC/temperature gradient methods)
  - Rodwell, 2000 (British vegetation classification)
  - Smeaton et al., 2021 (marine sedimentary carbon stocks)

- Additional notes for reuse: The dataset includes explicit header descriptions and cell formats to aid self-serve understanding and reuse; the description clarifies which fields are measured directly and which are derived (e.g., aboveground carbon from biomass and OC content).