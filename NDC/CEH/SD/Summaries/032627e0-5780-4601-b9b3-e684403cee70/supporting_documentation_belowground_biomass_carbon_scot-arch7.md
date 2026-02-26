# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

## Purpose and scope
- Describes physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes (2021).
- Based on gouge sediment cores used to quantify root biomass and belowground carbon in blue carbon environments across Scotland.
- Supports GIS-based analysis and mapping of saltmarsh carbon stocks.

## Dataset overview
- Location: Four Scottish saltmarshes across Scotland, chosen to reflect coastline variability in saltmarsh types, sediment and organic carbon content.
- Measurements: Belowground biomass (kg m-2) and belowground organic carbon content (kg C m-2; OC % by weight).
- Sample depth: Cores collected to 10 cm depth; eight root cores per marsh from three saltmarshes.
- Recordings: Site-level coordinates provided in decimal degrees (WGS84) and in X (easting) and Y (northing) coordinates.
- File format: .csv with data resource descriptions and field definitions.

## Spatial coverage and geometry
- Spatial references included: Lat_dec_deg, Long_dec_deg (WGS84); X_easting, Y_northing (projected coordinates).
- Marsh locations described with latitude/longitude and corresponding projected coordinates to support GIS workflows.

## Observed variables and data types
- Identifiers: Marsh_ID (saltmarsh name), Core_ID, Year, Sample_Archive_Location, Local_Authority.
- Environment and classification: Marsh_Type (Estuarine, Back-Barrier, Fringing, Embayment); NVC_Class (National Vegetation Classification).
- Sampling and location: Sampling_Method; Sample_Depth_cm; Lat_dec_deg; Long_dec_deg; X_easting; Y_northing.
- Measurements: Dry_Root_Biomass_kg_m_2; Belowground_Biomass_kg_m_2; OC_Perc; Belowground_C_kgC_m_2.
- Data formats: Core observations and site metadata stored in .csv; numeric fields for measurements and coordinates; text for identifiers and categories.

## Methods and procedures
- Field sampling: Eight root sample cores per marsh, collected with a 5.7 cm gouge corer to 10 cm depth.
- Vegetation typing: British National Vegetation Classification (NVC) used to classify vegetation communities.
- Location recording: Differential GPS (DGPS) used to log sample site positions.
- Sample processing: Roots washed to remove sediment, weighed fresh, then oven-dried at 60°C for 72 hours to determine biomass.
- Carbon quantification: Roots milled; 50 mg subsamples analyzed with Elementar Soli TOC instrument using a temperature gradient method (to quantify organic carbon).
- Calibration: Soli TOC calibrated with CaCO3 and standard OC/ROC/TIC references.
- Replication: Root sub-samples analyzed in triplicate.
- Quality control: Laboratory equipment calibrated per University of St Andrews practices.

## Data quality and standards
- Calibration and standard references documented for carbon quantification.
- Quality checks implemented through routine lab calibration; missing values indicated as NA where applicable.
- Data structured to support reproducibility and cross-site comparability.

## Data structure and metadata
- Core schema includes fields with clear descriptions (Marsh_ID, Year, Sampling_Method, Depth, coordinates, NVC_Class, biomass and carbon metrics).
- Local authority and marsh type provide contextual metadata for spatial queries and filtering in GIS workflows.
- Coordinate system flexibility allows mapping in both geographic (WGS84) and projected coordinate spaces.

## How to use in GIS
- Integrate as point features using Lat/Long or X/Y coordinates; convert to a consistent projection if needed for analysis.
- Join with additional spatial layers (saltmarsh extents, vegetation maps, soil types) to assess spatial distribution of belowground carbon stocks.
- Use biomass and carbon metrics (Dry_Root_Biomass_kg_m_2, Belowground_Biomass_kg_m_2, OC_Perc, Belowground_C_kgC_m_2) for stock calculations and visualization (e.g., choropleth or proportional symbols).
- Leverage Year and Marsh_Type for temporal or categorical analyses across sites.

## References
- Dadey, K.A., Janecek, T., Klaus, A. (1992). Dry-bulk density: its use and determination.
- DIN 19539 (2015-08). Investigation of solids: TOC, ROC, TIC standards.
- Ford, H. et al. (2019). Large-scale predictions of salt-marsh carbon stock.
- Natali, C. et al. (2020). Thermal stability of soil carbon pools.
- Rodwell, J.S. (2000). British plant communities classification.
- Smeaton, C. et al. (2021). Marine sedimentary carbon stocks in UK EEZ.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.