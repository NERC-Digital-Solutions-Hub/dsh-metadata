# Supporting documentation for data resource Aboveground_Biomass_Carbon_UK.csv

## Scope and Purpose
- Describes aboveground vegetation biomass and organic carbon content for UK saltmarshes (2019–2020).
- Based on 144 vegetation surveys across ten saltmarsh sites to quantify biomass and organic carbon in blue carbon environments around the United Kingdom.
- Data intended for GIS-based visualization and spatial analysis, with detailed metadata and measurement protocols.

## Spatial Coverage and Coordinate Systems
- Geographic extent: United Kingdom saltmarsh areas, including Scotland.
- Location representations:
  - Latitude and longitude in decimal degrees using the WGS84 projection.
  - X (Easting) and Y (Northing) coordinates.
- Site locations selected to represent saltmarsh vegetation, sediment types, and organic carbon content.

## Sampling and Laboratory Methods
- Field sampling: 144 vegetation surveys using 1 m^2 quadrats; within each quadrat a 0.125 m^2 area harvested.
- Vegetation description follows the British National Vegetation Classification (NVC) scheme (Rodwell, 2000).
- Location and elevation recorded with a DGPS.
- Sample processing:
  - Harvested vegetation oven-dried at 60°C for 72 hours; dry biomass calculated as mass per harvested area (g per 0.125 m^2) and converted to aboveground biomass (g m^-2).
  - Sub-samples milled; 50 mg analyzed with a Soli TOC for organic carbon content (OC) following DIN 19539 methodology.
  - Aboveground carbon calculated from OC content and biomass data.
- Calibration and quality control:
  - Soli TOC calibrated with CaCO3 and standard materials.
  - Laboratory equipment calibrated per University of St Andrews practices.
- Statistical treatment: Not applicable (NA) for this dataset; data checked via standard laboratory QA procedures.

## Data Structure and Variables
- File formats: CSV.
- Key fields (examples):
  - Marsh_ID: Saltmarsh name (Text)
  - Nation: Nation where site is located (Text)
  - Collection_Date: Date of sample collection (Date/Number)
  - Latitude_dec_degree: Latitude (decimal degrees, WGS84) (Number)
  - Longitude_dec_degree: Longitude (decimal degrees, WGS84) (Number)
  - X_easting: Location as X (Easting) (Number)
  - Y_northing: Location as Y (Northing) (Number)
  - Elevation_above_OD_m: Elevation above ordnance datum (m) (Number)
  - NVC: National Vegetation Classification (Text)
  - Marsh_Zone: Marsh zone category (e.g., High marsh, Low marsh, Pioneer marsh) (Text)
  - Harvested_Area_m_2: Harvested vegetation area (m^2) (Number)
  - Biomass_g: Dry biomass (g) from harvested area (Number)
  - Aboveground_biomass_g_m_2: Aboveground biomass (g m^-2) (Number)
  - OC_Perc: Organic carbon content (%) (Number)
  - Aboveground_carbon_g_C_m_2: Aboveground carbon (g C m^-2) (Number)

## Data Quality, Provenance, and Referencing
- Data provenance includes field collection details, NVC classification, laboratory analyses, and calibration procedures.
- Calibration standards and methods cited include:
  - DIN 19539: TOC measurement standardization.
  - Rodwell (2000) NVC framework.
  - Harvey et al. (2019) and Natali et al. (2020) related to carbon stock methodologies.
  - Smeaton et al. (2021) supporting marine sedimentary carbon stocks.
- References provided for methods and context, ensuring traceability of measurements and analysis.

## Usage and Applications for GIS
- Enables map-based visualization of biomass and carbon stocks across UK saltmarshes.
- Facilitates spatial analyses such as:
  - Comparing biomass and OC content by site, nation, or marsh zone.
  - Integrating lat/long and projected coordinates (X/Y) for diverse GIS workflows.
  - Linking with NVC classifications and habitat descriptors for ecological mapping.
- Useful for blue carbon assessments, coastal ecosystem services evaluations, and policy-relevant spatial planning.

## Limitations and Considerations
- Data represent 2019–2020 field campaigns; potential temporal variability beyond that window.
- Sampling focused on saltmarshes; applicability to other coastal habitats may be limited.
- NA entry for certain statistical treatments indicates no downstream statistical analyses within this resource.

## References
- DIN 19539: 2015-08. Investigation of solids Temperature dependent differentiation of Total Carbon (TOC400, ROC, TIC900).
- Harvey, R.J., Garbutt, A., Hawkins, S.J. and Skov, M.W. (2019). No detectable broad-scale effect of livestock grazing on soil blue-carbon stock in salt marshes. Frontiers in Ecology and Evolution, 7, p.151.
- Natali, C., Bianchini, G., & Carlino, P. (2020). Thermal stability of soil carbon pools: Inferences on soil nature and evolution. Thermochimica Acta, 683, 178478.
- Rodwell, J. S. (2000). British plant communities, Maritime Communities and Vegetation of Open Habitats. Cambridge University Press.
- Smeaton, C., Hunt, C.A., Turrell, W.R. and Austin, W.E. (2021). Marine Sedimentary Carbon Stocks of the United Kingdom's Exclusive Economic Zone. Frontiers in Earth Science, 9, p.50.