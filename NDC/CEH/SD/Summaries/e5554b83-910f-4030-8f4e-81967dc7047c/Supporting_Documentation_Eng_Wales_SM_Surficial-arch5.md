# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

## Overview
- Project: Carbon Storage in Intertidal Environments (C-SIDE)
- Funding: NERC (NE/R010846/1)
- Staff Responsible: William Austin
- Research Team: Paulina Ruranska (U. of St Andrews), Cai J.T. Ladd (U. of Glasgow/Bangor), Craig Smeaton (U. of St Andrews), Martin W. Skov (Bangor), William E.N. Austin (U. of St Andrews/SAS), C-SIDE Citizen Science Team
- Data resource name: Dry bulk density, loss on ignition and organic carbon content of surficial soils from English and Welsh saltmarshes, 2019
- Description: 212 surficial soil samples (top 10 cm) from 49 English and Welsh saltmarshes
- Monitoring period: January 2018 – December 2019 (English/Welsh portion of C-SIDE and CarbonQuest Citizen Science program)
- Sampling plan: No repeat sampling planned

## Data resource details
- Locations: English/Welsh saltmarshes; site coordinates provided in multiple formats
  - Geographical boundaries in WGS84 (latitude/longitude)
  - Decimal degrees: 49.906552, -6.725626 to 55.889857, 2.177307
  - British National Grid (OSGB 1936) with corresponding easting/northings
- Location description: Sites selected to represent contrasting habitats (sediment types, vegetation, sea-level history)
- Monitoring/sampling rate: 2018-2019 English/Welsh sampling plus Citizen Science (CarbonQuest); no planned repeat sampling
- Variables observed: Soil texture (Sandy/Not-Sandy/Organic); Dry bulk density (g cm-3); Organic matter content (LOI, %); Organic carbon content (% OC by Elemental Analysis)
- Procedures (field/lab): 
  - Field: Soil collected with a 50 mL syringe to 10 cm depth; GPS locations recorded; samples frozen at -20°C
  - Soil texture classified per Ford et al., 2019
  - Dry bulk density calculated from dried volumetric samples
  - LOI determined by ignition at 450°C for 4 hours
  - Organic carbon measured with Elemental Analyzer after acidifying to remove carbonates
- Calibration and QA/QC:
  - Elemental analyzer calibrated with Acetanilide
  - Repeated analysis of a medium Organic Soil standard (B2178)
  - Citizen Science samples quality checked visually; GPS coordinates compared to habitat maps; soil texture classifications validated by four team members independently
- Data management and sharing:
  - File formats: .csv
  - Data provenance documented through described procedures and references
- Documentation note: No additional information provided beyond the dataset description

## Data resource description (fields)
- Saltmarsh_Name: Saltmarsh name (Text)
- Nation: Nation (Text)
- Year: Year of sample collection (Number)
- Lat_dec_deg: Latitude in decimal degrees (WGS84) (Number)
- Long_dec_deg: Longitude in decimal degrees (WGS84) (Number)
- Grid_Reference: Ordnance Survey National Grid reference (Text)
- X_easting: Easting (Number)
- Y_northing: Northing (Number)
- Sampling_Method: 50 mL syringe (Text)
- Depth_cm: Depth of soil sample (cm) (Number)
- Dry_Bulk_Density_g_cm_3: Dry bulk density (g cm^-3) (Number)
- Soil_Texture: Soil texture (Text; values: Sandy, Not-Sandy, Organic)
- OC_Perc: Organic carbon content (% wt.) (Number)
- LOI_Perc: Loss on ignition / organic matter content (% wt.) (Number)

## References
- Craft, C.B., Seneca, E.D. and Broome, S.W. (1991). Loss on ignition and Kjeldahl digestion for estimating organic carbon and total nitrogen in estuarine marsh soils.
- Dadey, K.A., Janecek, T. and Klaus, A. (1992). Dry-bulk density: its use and determination.
- Ford, H. et al. (2019). Large-scale predictions of salt-marsh carbon stock based on simple observations of plant community and soil type.
- Kennedy, P. et al. (2005). The effect of acidification on determination of organic carbon and nitrogen.
- Nieuwenhuize, J. et al. (1994). Rapid analysis of organic carbon and nitrogen in particulate materials.
- Verardo, D.J. et al. (1990). Determination of organic carbon and nitrogen in marine sediments using elemental analysis.