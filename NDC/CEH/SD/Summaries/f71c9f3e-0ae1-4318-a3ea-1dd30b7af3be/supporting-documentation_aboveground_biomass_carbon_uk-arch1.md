# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

- Purpose
  - Support the Aboveground_Biomass_Carbon_UK.csv data resource by detailing physical and biogeochemical measurements of aboveground biomass from UK saltmarshes (2019–2020).
  - Aids in understanding, replicating, and reusing the dataset for blue carbon assessments and cross-site analyses.

## What the dataset contains

- Measurements
  - Physical biomass: aboveground biomass (g m^-2) derived from harvested vegetative material.
  - Organic carbon: organic carbon content (% OC) and aboveground carbon (g C m^-2).

- Scope and scale
  - Locations: ten saltmarshes across the United Kingdom.
  - Samples: 144 vegetation surveys (1 m^2 quadrats; harvested area 0.125 m^2 per quadrat).
  - Time frame: 2019–2020.

- Variables and data structure
  - Marsh_ID: saltmarsh name
  - Nation: country location
  - Collection_Date: date of sample collection
  - Latitude_dec_degree / Longitude_dec_degree: decimal degrees (WGS84)
  - X_easting / Y_northing: map grid coordinates
  - Elevation_above_OD_m: elevation above ordnance datum
  - NVC: National Vegetation Classification
  - Marsh_Zone: habitat zone (e.g., High marsh, Low marsh, Pioneer marsh)
  - Harvested_Area_m_2: area harvested per sample
  - Biomass_g: dry biomass mass (g)
  - Aboveground_biomass_g_m_2: biomass density (g m^-2)
  - OC_Perc: organic carbon content (%)
  - Aboveground_carbon_g_C_m_2: carbon stock per area (g C m^-2)

- Location and formats
  - Geographic extent includes sites across Scotland and other coastal UK regions.
  - Data are provided in .csv format.
  - Location details include both geographic coordinates (lat/long) and projected coordinates (X/Y).

## Methods and procedures

- Field sampling
  - At each site, a 1 m^2 quadrat was used; vegetation described per the British National Vegetation Classification (NVC) scheme.
  - Within each quadrat, 0.125 m^2 area harvested for biomass measurement.

- Laboratory processing
  - Harvested vegetation dried at 60°C for 72 hours; dry biomass weighed.
  - Dry biomass divided by harvested area to obtain aboveground biomass (g m^-2).
  - Sub-samples milled; 50 mg analyzed with Elementar Soli TOC (temperature gradient method) to quantify organic carbon.
  - Aboveground carbon calculated from OC content and biomass data.

- Calibration and quality control
  - TOC calibration with Calcium Carbonate (CaCO3) and silty soil TOC/ROC/TIC standards.
  - Laboratory equipment calibrated according to University of St Andrews procedures.

## Data provenance and metadata

- Data resource description
  - Includes header mappings and variable formats (e.g., descriptive text for Marsh_ID; numeric formats for coordinates, areas, and measurements).
  - Metadata supports discoverability and reuse of the dataset.

- References and standards
  - DIN 19539: TOC analysis standard
  - Rodwell (2000): British plant communities (NVC reference)
  - Harvey et al. (2019); Natali et al. (2020); Smeaton et al. (2021) cited for methods and context

## Usage and applications

- Suitable for estimating UK blue carbon stocks in saltmarsh vegetation.
- Enables cross-site comparisons of aboveground biomass and carbon content.
- Can be integrated with GIS workflows using provided coordinates and formats.
- Useful for informing carbon accounting, habitat management, and ecological research.

## Notes on data interpretation

- Statistical treatment of observations is not provided in this dataset (NA).
- Dataset emphasizes descriptive measurements collected under consistent field and lab protocols to support reproducibility and comparability.