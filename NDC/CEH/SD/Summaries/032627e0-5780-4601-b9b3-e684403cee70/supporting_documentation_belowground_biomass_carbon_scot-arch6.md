# Supporting documentation for data resource Belowground_Biomass_Carbon_Scot.csv

## Overview
- Documents the physical and biogeochemical measurements of belowground biomass and organic carbon content from Scottish salt marshes, collected in 2021.
- Data resource based on gouge sediment cores from four Scottish saltmarshes to quantify belowground biomass and carbon content in blue carbon environments across Scotland.
- Geographic scope includes multiple sites around the Scottish coastline with coordinates provided to support comparability.

## Data content and structure
- Variables (as described in the dataset description):
  - Marsh_ID (saltmarsh name), Year, Sample_Archive_Location, Local_Authority, Marsh_Type (estuarine, back-barrier, fringing, embayment)
  - Core_ID, Sampling_Method, Sample_Depth_cm
  - Lat_dec_deg, Long_dec_deg (WGS84 decimal degrees)
  - X_easting, Y_northing (alternative location coordinates)
  - NVC_Class (National Vegetation Classification)
  - Dry_Root_Biomass_kg_m_2, Belowground_Biomass_kg_m_2
  - OC_Perc (organic carbon percentage)
  - Belowground_C_kgC_m_2
- File format: .csv
- Year field indicates year of sample collection; sampling includes multiple sites per marsh and multiple cores per site.

## Data collection and methods
- Field sampling: Eight root sample cores collected from three Scottish saltmarshes using a gouge corer (5.7 cm diameter) to a depth of 10 cm.
- Site characterization: Core descriptions recorded with Troels-Smith (1955) scheme; sample locations captured with Differential GPS (DGPS).
- Sample processing: Roots washed to remove sediment using 10% Calgon; roots weighed pre- and post-oven-drying (60°C for 72 hours) to determine belowground biomass (kg m^-2).
- Carbon quantification: Samples milled, 50 mg analyzed with Elementar Soli total organic carbon (TOC) using a temperature gradient method (DIN 19539; Natali et al., 2020; Smeaton et al., 2021) to quantify organic carbon. Root subsamples analyzed in triplicate; belowground carbon (kg C m^-2) derived by combining OC measurements with biomass data.
- Calibration and QA: Soli TOC calibration with CaCO3 and silty soil OC standards; laboratory equipment calibrated per University of St Andrews practices.
- Data treatment: Statistical treatment not specified (NA).

## Data quality and provenance
- Emphasis on standardization of site locations and vegetation classification to enable cross-site comparisons.
- QA procedures include routine calibration of laboratory equipment.
- Data description includes explicit format and unit conventions to facilitate consistent use.

## Location, scope, and temporal coverage
- Geographic coverage: Saltmarsh sites around Scotland; coordinates provided in decimal degrees (WGS84) and corresponding X/Y coordinates.
- Temporal coverage: Year field indicates year of sample collection; dataset context is 2021 sampling.
- Marsh types represented: Estuarine, Back-Barrier, Fringing, Embayment.

## Data usage and interpretation notes
- Outputs include direct measurements of belowground biomass and carbon, enabling calculation of carbon stocks (kg C m^-2) in saltmarsh substrates.
- Users should note potential limitations:
  - Field sampling limited to eight cores per site across three marshes; spatial coverage may be patchy.
  - No statistical treatment reported; users may need to apply their own analyses for extrapolation or uncertainty.
- Data can support comparisons of biomass and carbon across marsh types and sites, and integration with vegetation classification (NVC) for ecological context.

## Access and formats
- Primary data format: .csv
- Metadata provides detailed field definitions, units, and collection methods to support data reuse and integration with other datasets.

## References and foundational methods
- Troels-Smith (1955) sediment characterization
- British National Vegetation Classification (NVC) scheme (Rodwell, 2000)
- TOC methodology and calibration references: DIN 19539 (2015), Natali et al. (2020), Smeaton et al. (2021)
- Calibration standards: CaCO3 and OC standards
- Related methodological and interpretive sources cited for context and reproducibility

## Key takeaways for data users
- A well-documented CSV resource detailing belowground biomass and organic carbon in Scottish saltmarshes, with clear field definitions, sampling methods, and calibration approaches.
- Suitable for site-level comparisons and integration with vegetation and location data to assess blue carbon stocks in Scottish saltmarsh ecosystems.
- Users should consider the relatively small number of cores/sites and the absence of reported statistical treatment when extrapolating beyond the sampled locations.