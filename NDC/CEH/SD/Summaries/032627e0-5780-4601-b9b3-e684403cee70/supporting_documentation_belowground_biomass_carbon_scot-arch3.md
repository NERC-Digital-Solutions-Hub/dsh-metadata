# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

## Overview
- Physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes, collected in 2021.
- Purpose: quantify belowground biomass and organic carbon in blue carbon environments across Scotland to support environmental monitoring and policy evaluation.

## Data collection and scope
- Observations based on gouge sediment cores from four Scottish saltmarshes to capture belowground biomass and carbon content.
- Locations covered Scotland with coordinates provided in decimal degrees (WGS84) and also as X (easting) and Y (northing) values.
  - Examples of coordinates include 54.251069, -6.262840; 54.564402, 0.464285; 58.742170, -0.204728; 58.994955, -7.092833.
- Site descriptions indicate all sites are in similar environmental regions and were chosen around Scotland’s coastline to reflect saltmarsh types, sediment variation, and organic carbon content.
- Data resource type: belowground biomass (kg m^-2), belowground carbon (kg C m^-2), organic carbon percentage (%), with associated identifiers.

## Variables and measurements
- Marsh_ID: Saltmarsh name
- Year: Year of sample collection
- Sample_Archive_Location: Sample storage location
- Local_Authority: Local authority where marsh is located
- Marsh_Type: Estuarine, Back-Barrier, Fringing, Embayment
- Core_ID: Soil core identifier
- Sampling_Method: Method of sample collection
- Sample_Depth_cm: Depth range of sample (cm)
- Lat_dec_deg, Long_dec_deg: Latitude and longitude in decimal degrees (WGS84)
- X_easting, Y_northing: Location in projected coordinates
- NVC_Class: National Vegetation Classification
- Dry_Root_Biomass_kg_m_2: Dry weight of root biomass (kg m^-2)
- Belowground_Biomass_kg_m_2: Belowground biomass (kg m^-2)
- OC_Perc: Organic carbon content (%)
- Belowground_C_kgC_m_2: Belowground carbon (kg C m^-2)

## Methods and quality assurance
- Sampling: Eight root sample cores collected from three Scottish saltmarshes using a 5.7 cm gouge corer to 10 cm depth.
- Vegetation classification: British National Vegetation Classification (NVC) scheme (Rodwell, 2000) used for vegetation characterization.
- Location recording: Differential GPS (DGPS) used to record sample site locations.
- Sample preparation: Roots washed to remove sediment using 10% Calgon solution; roots weighed before and after oven drying at 60°C for 72 hours to determine biomass.
- Carbon quantification: Samples milled to fine powder; 50 mg per crucible analyzed with Elementar Soli TOC, using the temperature gradient method (DIN 19539) to quantify organic carbon; root sub-samples analyzed in triplicate.
- Calibration: TOC instrument calibrated with Calcium Carbonate (CaCO3) and standards for TOC/ROC/TIC (B2290).
- Data handling: Samples combined with biomass data to calculate belowground carbon.
- Quality control: Laboratory equipment calibrated per University of St Andrews practices.
- Statistical treatment: Not specified (NA).

## Data structure and formats
- Data file format: .csv
- Data resource description fields indicate:
  - Marsh_ID, Year, Sample_Archive_Location, Local_Authority, Marsh_Type, Core_ID, Sampling_Method, Sample_Depth_cm, Lat_dec_deg, Long_dec_deg, X_easting, Y_northing, NVC_Class, Dry_Root_Biomass_kg_m_2, Belowground_Biomass_kg_m_2, OC_Perc, Belowground_C_kgC_m_2
- Provides both descriptive metadata and numeric measurement fields to support analysis and integration with monitoring workflows.

## Reproducibility, standards, and governance considerations
- Clear documentation of sampling, lab methods, and calibration procedures supports reproducibility and auditability.
- Metadata and data sharing considerations are apparent (e.g., location data, DGPS, NVC classification) but may require metadata completeness and governance processes for broader data sharing and interoperability.
- File formats and structured data enable integration into dashboards or reports used in monitoring frameworks.

## Relevance for monitoring frameworks
- Provides baseline and site-specific measurements of belowground biomass and carbon along with organic carbon content, useful for tracking blue carbon stocks and habitat health over time.
- The dataset aligns with monitoring objectives such as assessing policy impacts on carbon storage, informing restoration or conservation decisions, and supporting national or regional environmental indicators.
- Metadata coverage (locations, marsh types, vegetation classification, sampling methods) supports transparency, comparability, and data governance essential for monitoring programs.

## Limitations and challenges
- Statistical treatment details are not provided (NA), which may limit certain analyses without further statistical context.
- Metadata completeness and standardization (e.g., full QA details, update cadence) could affect data usability for some monitoring purposes.
- Public sharing of underlying datasets is mentioned as a barrier in general, implying governance considerations for access and sharing.

## References
- Dadey, K.A., Janecek, T., and Klaus, A. (1992). Dry-bulk density: its use and determination.
- DIN 19539 (2015). Investigation of solids Temperature dependent differentiation of Total Carbon (TOC, ROC, TIC).
- Ford, H. et al. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type.
- Natali, C. et al. (2020). Thermal stability of soil carbon pools: Inferences on soil nature and evolution.
- Rodwell, J.S. (2000). British plant communities, Maritime Communities and Vegetation of Open Habitats.
- Smeaton, C. et al. (2021). Marine Sedimentary Carbon Stocks of the United Kingdom's Exclusive Economic Zone.
- Troels-Smith, J. (1955). Characterization of unconsolidated sediments.