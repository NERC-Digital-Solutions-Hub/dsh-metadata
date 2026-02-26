# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

## Overview
- Data resource documenting dry bulk density, loss on ignition (LOI), and organic carbon content of surficial soils from English and Welsh saltmarshes (top 10 cm).
- Observations collected from 212 soil samples across 49 saltmarshes in England and Wales (Jan 2018 – Dec 2019).
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; funded by NERC (NE/R010846/1).
- Team includes universities (St Andrews, Glasgow, Bangor) and the C-SIDE Citizen Science Team; staff responsible: William E.N. Austin, with contributing researchers.

## Data content and schema
- Core variables and measurements:
  - Soil texture: Sandy / Not-Sandy / Organic
  - Dry bulk density: g cm-3
  - Organic matter content: LOI (%)
  - Organic carbon content: OC (%)
- Sample and location metadata:
  - Saltmarsh_Name; Nation; Year of sampling
  - Lat_dec_deg (decimal degrees, WGS84); Long_dec_deg (WGS84)
  - Grid_Reference (OSGB36); X_easting; Y_northing
  - Depth_cm (sampling depth, cm)
  - Sampling_Method (50 ml syringe)
- Data formats and structure:
  - Primary file format: .csv
  - Data resource description includes field-level details and cell formats for each variable

## Data collection, processing, and quality control
- Sampling protocol:
  - Soil samples collected to 10 cm depth using a 50 ml syringe; GPS coordinates recorded via mobile devices or RTK systems
  - Samples frozen at -20°C prior to analysis
  - Sites selected to represent contrasting habitats across England and Wales
- Laboratory methods:
  - LOI used to estimate organic matter; organic carbon measured by elemental analysis after acidification to remove carbonates
  - Calibrations: elemental analyzer calibrated with Acetanilide; repeated analysis of a standard (B2178) during runs
- Quality control:
  - Citizen Science samples QC: visual verification by salt marsh scientists; GPS coordinates cross-checked with habitat maps and aerial photos; soil texture classifications done by four independent team members
  - Overall data quality checks documented; statistical treatment not specified (NA)
- Data provenance and references:
  - Method references include Ford et al. 2019, Craft et al. 1991, Nieuwenhuize et al. 1994, Verardo et al. 1990, Dadey et al. 1992, Kennedy et al. 2005

## Metadata, formats, and accessibility
- Field descriptions and data dictionary:
  - Comprehensive resource description for each column (e.g., Lat/Long, Grid_Reference, X/Y, Depth_cm, Dry_Bulk_Density_g_cm_3, Soil_Texture, OC_Perc, LOI_Perc)
- Coordinate systems:
  - Latitude/Longitude in decimal degrees (WGS84)
  - Grid references provided in OSGB36 with corresponding easting/northing
- Data stewardship:
  - Clearly documented procedures, calibration steps, and quality checks; suitable for integration with other saltmarsh carbon datasets
  - Primary data asset is Eng_Wales_SM_Surficial.csv with accompanying data resource description and variable definitions

## Reuse, limitations, and context for Data Leaders
- Strategic value:
  - Demonstrates end-to-end data lifecycle: collection, processing, QC, metadata curation, and documentation
  - Supports carbon stock assessments in intertidal environments with geospatial and sample-level detail
  - Collaborative data asset spanning multiple institutions and a citizen science component
- Limitations and considerations:
  - No repeat sampling indicated; cross-sectional snapshot (2018–2019)
  - Statistical treatment not reported (NA), and QC notes highlight variability inherent in citizen science data
  - Depth limited to 10 cm; method and classifications rely on specific protocols and literature references
- Implications for data governance and strategy:
  - Provides a model for transparent documentation, calibration traceability, and independent quality checks
  - Enhances discoverability through explicit metadata (coords, grid references, sampling method, units)
  - Encourages broader community engagement while maintaining data integrity across networks

## References
- Craft, C.B., Seneca, E.D. and Broome, S.W., 1991. Loss on ignition and Kjeldahl digestion for estimating organic carbon and total nitrogen in estuarine marsh soils: calibration with dry combustion. Estuaries, 14(2), pp.175-179.
- Dadey, K.A., Janecek, T. and Klaus, A., 1992. Dry-bulk density: its use and determination. In Proceedings of the Ocean Drilling Program, Scientific Results (Vol. 126, pp. 551-554).
- Ford, H., Garbutt, A., Duggan-Edwards, M., Harvey, R., Ladd, C. and Skov, M.W., 2019. Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type. Biogeosciences, 16(2), pp.425-436.
- Kennedy, P., Kennedy, H. and Papadimitriou, S., 2005. The effect of acidification on the determination of organic carbon, total nitrogen and their stable isotopic composition in algae and marine sediment. Rapid Communications in Mass Spectrometry, 19(8), pp.1063-1068.
- Nieuwenhuize, J., Maas, Y.E. and Middelburg, J.J., 1994. Rapid analysis of organic carbon and nitrogen in particulate materials. Marine Chemistry, 45(3), pp.217-224.
- Verardo, D.J., Froelich, P.N. and McIntyre, A., 1990. Determination of organic carbon and nitrogen in marine sediments using the Carlo Erba NA-1500 Analyzer. Deep Sea Research Part A, 37(1), pp.157-165.