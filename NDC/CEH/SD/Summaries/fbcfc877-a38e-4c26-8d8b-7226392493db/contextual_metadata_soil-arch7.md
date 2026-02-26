# Discovery metadata- Soil nutrients, soil pyrogenic carbon, soil bulk density and roots dry weight under different intensities of soil management in the Colombian Andes between 2019-2021

## Overview
- Four CSV-based databases describe soil nutrients, pyrogenic carbon, soil bulk density, and roots dry weight.
- Study spans 27 permanent monitoring plots (0.5 ha each) across an altitudinal gradient in the Colombian Andes, collected 2019–2022.
- Designed to assess how soil characteristics vary with forest disturbance gradients (low, medium, high perturbation) and altitude (lowlands, midlands, highlands).
- Data generated within the BioResilience project; labs involved include UNAD, Instituto Nacional de Pesquisas da Amazônia, and James Cook University; UK NERC funding supported the work.

## Spatial design and locations
- 27 plots, each 0.5 hectares.
- Altitude categories:
  - Lowlands: 0–1200 m
  - Midlands: 1200–2200 m
  - Highlands: 2200–3200 m
- Locations (representative examples):
  - Lowlands: Serranía de las Quinchas (Puerto Boyacá, Boyacá)
  - Midlands: Pedro Palo (Tena, Cundinamarca) and Encino (Santander)
  - Highlands: Encenillo (Guasca, Cundinamarca) and Martos (Guatavita, Cundinamarca)
- Disturbance gradient: low, medium, high perturbation with corresponding recovery times (more than 30 years, 20–30 years, less than 20 years).
- Plot coordinates are provided for spatial mapping and GIS integration.

## Datasets and key variables
- Four CSV files:
  - pyrogeniccarbonbr.csv
    - Variables include: Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected, %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc), Cpyc_(%), %Cpyc/Cbulk, %OC.
  - soilnutrientbr.csv
    - Variables include: Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex.
  - bulkdensitybr.csv
    - Variables include: Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem, Bulk_density.
  - dryweigthbr.csv
    - Variables include: Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight.
- Units and data types (examples):
  - pH (water), p_available and tot_p (mg/kg or related units), particle sizes (sand/clay/silt in %), Ca_ex/Mg_ex/K_ex/Na_ex (cmolc/kg), TOC and pyrogenic carbon metrics (%), D13C values (‰), bulk density (g/cm3), dry weight (g).
- Data files contain metadata fields such as Sample_Id and Project/Collected to trace data provenance.
- Depth-specific measurements and location-based attributes (Municipio, Departamento, Farm) support spatial analyses.

## Data collection, processing and quality control
- Collection and analysis methods:
  - Pyrogenic carbon: TOC by elemental analysis; pyrogenic carbon via hydrogen pyrolysis (HyPy); Cpyc%/Cbulk derived from HyPy methodology.
  - Soil nutrients: pH in water; available P by sequential resin/chemical extractions; total P by acid digestion; texture by Bouyoucos method; exchangeable cations by Ag-TU extraction.
  - Bulk density: pit-based sampling with oven-dried weight.
  - Root dry weight: measured from root samples.
- Calibration and quality control:
  - Instrument calibration and reference value checks established via literature.
  - Independent review of databases and metadata to verify structure, completeness, typing, duplicates, and validity.
  - Metadata validation for accuracy and consistency.
- Data provenance:
  - Research conducted under BioResilience with collaboration across institutions and funded by NE/NERC.

## Data structure and access
- Four CSV files with descriptive column headers as listed above.
- Plot_code (1–27) enables cross-dataset joins; depth and ecosystem/land-use attributes provide context for GIS layering.
- Detailed variable descriptions and unit information accompany each file to aid correct interpretation and mapping.

## GIS applications and use cases
- Create map-based data products showing spatial distribution of soil properties across altitude and disturbance gradients.
- Join soil chemistry, pyrogenic carbon, bulk density, and root biomass datasets by Plot_code for composite soil-health maps.
- Analyze spatial patterns of nutrient availability, carbon stocks, and physical soil properties in relation to elevation, land use, and perturbation history.
- Support policy and management decisions by visualizing resilience-related soil factors across the Colombian Andes.

## Notes and references
- Data collection period spans 2019–2022.
- Key methodological references include HyPy for pyrogenic carbon, standard soil chemistry and texture methods, and calibration/QC practices outlined in the cited literature (Ascough et al., Koele et al., Quesada et al., Tiessen & Moir, Wurster et al.).