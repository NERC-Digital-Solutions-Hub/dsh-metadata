# Supporting documentation for data resource Eng_Wales_SM_Surficial.csv

## Overview
- Data resource documenting dry bulk density, loss on ignition (LOI), and organic carbon content of surficial soils from English and Welsh saltmarshes (top 10 cm), based on 212 samples from 49 sites (2019).
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project; funded by NERC (NE/R010846/1).
- Team: William E.N. Austin (staff responsible) and a research group from University of St Andrews, University of Glasgow/Bangor University, Bangor University; includes the C-SIDE Citizen Science Team.
- Monitoring program covers England and Wales; sampling conducted January 2018 – December 2019; no repeat sampling planned.
- Data intended for assessing saltmarsh carbon stocks and enabling standardized, comparable environmental outputs.

## Data resource details
- Observables: 
  - Soil texture (Sandy/Not-Sandy/Organic)
  - Dry bulk density (g cm-3)
  - Organic matter content (LOI, %)
  - Organic carbon content (OC, %)
- Depth: top 10 cm of surficial soil
- Number of observations: 212 samples from 49 sites
- Site descriptions: sites selected to represent contrasting habitats across England and Wales (sediment types, vegetation, sea level history)
- Sampling method: 50 ml syringe core to 10 cm depth; GPS locations recorded; samples frozen at -20°C until analysis
- Calibration and standards: Elemental analyser calibration with Acetanilide; repeated analysis of standard (B2178)
- Statistical treatment: Not applicable (NA) for this resource
- Quality control: Citizen Science QC including visual checks, GPS habitat consistency checks, soil texture classification by four independent team members
- File format: .csv

## Location and sampling scope
- Geographic scope: England and Wales
- Site coordinates and representations: decimal latitude/longitude (WGS84), plus British National Grid (OSGB 1936) coordinates (X_easting, Y_northing)
- Specific example coordinates provided in the resource description (illustrative of data structure)

## Procedures and methodology
- Soil texture classification: follows Ford et al. (2019) methodology
- Dry bulk density: determined from dried samples using volume measurements and mass
- LOI: measured after drying and ashing to determine organic matter content
- Organic carbon: measured via elemental analysis after carbonate removal with acid (HCl)
- Laboratory workflow: soil samples milled, prepared, and analyzed with an Elemental Analyzer (Vario EL Cube) per cited references
- Field-to-lab workflow: samples collected in the field, GPS-recorded, preserved (frozen), then processed in the lab

## Data quality and integrity
- Quality control implemented for citizen-science contributed samples
- Geospatial validation: GPS coordinates cross-checked against habitat maps and aerial imagery
- Soil texture classifications independently performed by four team members; final classification reported as consensus
- Documentation includes calibration and reference procedures for traceability

## Data structure and resource description
- Core fields (examples): Saltmarsh_Name, Nation, Year, Lat_dec_deg, Long_dec_deg, Grid_Reference, X_easting, Y_northing, Sampling_Method, Depth_cm, Dry_Bulk_Density_g_cm_3, Soil_Texture, OC_Perc, LOI_Perc
- Data resource description format details: includes units, field descriptions, and cell formats (e.g., text, number)
- Column examples include sampling method (50 ml syringe), depth (cm), and measured properties with units

## Related references
- Methodology and calibration references underpinning LOI, dry bulk density, and organic carbon measurements, including:
  - Craft et al. (1991)
  - Dadey et al. (1992)
  - Ford et al. (2019)
  - Kennedy et al. (2005)
  - Nieuwenhuize et al. (1994)
  - Verardo et al. (1990)

## Context for use
- The dataset supports standardized reporting of saltmarsh soil carbon-related properties to inform environmental health assessments and policy-relevant monitoring over time.
- Designed to enable broader data reuse and accessibility, aligning with environmental data monitoring practices.