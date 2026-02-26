# Discovery metadata- Soil nutrients, soil pyrogenic carbon, soil bulk density and roots dry weight under different intensities of soil management in the Colombian Andes between 2019-2021

## Overview
- Objective: assess changes in soil characteristics across altitude and disturbance gradients to understand drivers of forest resilience and how perturbation affects ecosystem functioning.
- Context: part of the BioResilience project, funded by UK NERC, with collaboration among UNAD, INPA, and James Cook University.
- Coverage: data collected (and described) for 27 forest monitoring plots along an altitudinal gradient (lowlands, midlands, highlands) and a disturbance gradient (low, medium, high perturbation), in the Colombian Andes.

## Datasets and variables
- Four csv data files:
  - pyrogeniccarbonbr.csv: pyrogenic carbon and organic carbon metrics
    - Key variables: Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected, %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc), Cpyc_(%), %Cpyc/Cbulk, %OC
  - soilnutrientbr.csv: soil nutrient properties
    - Key variables: Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex
  - bulkdensitybr.csv: soil bulk density data
    - Key variables: Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem, Bulk_density
  - dryweigthbr.csv: roots dry weight data
    - Key variables: Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight
- Units and ranges are specified within the dataset descriptions (e.g., %C_(Bulk), TOC, D13C values in ‰, mg/kg for available P, cmolc/kg for exchangeable cations, g/cm^3 for bulk density, g for dry weight).

## Sampling design and locations
- Plots: 27 permanent monitoring plots, each 0.5 hectares.
- Altitudinal gradient (location categories):
  - Lowlands: 0–1200 m
  - Midlands: 1200–2200 m
  - Highlands: 2200–3200 m
- Disturbance gradient: low, medium, high perturbation with recovery times increasing from high disturbance (<20 years) to low disturbance (>30 years).
- Locations (examples): Serranía de las Quinchas (lowlands), Pedro Palo and Encino (midlands), Encenillo and Martos (highlands).
- Spatial references: plots include geographic coordinates; a figure/table summarizes plot codes, perturbation levels, altitude categories, and coordinates.

## Measurements and methods
- Pyrogenic carbon and TOC
  - Total Organic Carbon (TOC) determined by elemental analysis (Costech ECS-4010).
  - Pyrogenic carbon (Cpyc) quantified via hydrogen pyrolysis (HyPy).
  - Cpyc%/C_bulk calculated from HyPy results; D13C corrections following Wurster et al. (2012) for pyrogenic carbon isotopes.
- Soil nutrients
  - pH in water via shaking 10 g soil with 25 ml water and measuring the supernatant pH.
  - Available phosphorus (p_available) via sequential resin extraction, 0.5 M NaHCO3, 0.1 M NaOH, and 1 M HCl steps.
  - Total phosphorus (tot_p) via acid digestion with sulfuric acid and H2O2.
  - Particle size (sand, silt, clay) via Bouyoucos method after dispersion.
  - Exchangeable Ca, Mg, K, Na via Ag-TU extraction (silver thiourea method).
- Physical properties
  - Bulk density measured from pit samples, oven-dried to constant weight.
  - Roots dry weight obtained from samples at various depths/sites.
- Calibration and quality checks
  - Instrument calibration and reference values established from literature prior to measurements.
  - Quality control included independent review of database structure, missing values, data types, duplicates, and metadata consistency.

## Data structure and file formats
- Four CSV files collectively describing the dataset:
  - pyrogeniccarbonbr.csv: 14 columns (Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected, %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc), Cpyc_(%), %Cpyc/Cbulk, %OC)
  - soilnutrientbr.csv: 11 columns (Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex)
  - bulkdensitybr.csv: 10 columns (Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem, Bulk_density)
  - dryweigthbr.csv: 7 columns (Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight)
- Each row includes a Plot_code identifier linking measurements across files; depth-specific data are captured where applicable.

## Quality assurance and metadata
- Rigorous quality control to ensure accuracy, completeness, and consistency.
- External reviews by non-soil-team members to validate database structure, missing values, data typing, duplicates, and metadata alignment.
- Documentation provides detailed definitions, measurement units, and value ranges for all fields to support reproducibility and discoverability.

## Context and potential uses
- Context: Enables analysis of how soil nutrients, pyrogenic carbon stocks and composition, soil physical properties, and root biomass vary with altitude and perturbation intensity.
- Potential uses for analysts:
  - Identify correlations between soil chemical/physical properties and disturbance/recovery status.
  - Develop models predicting soil resilience indicators under different management intensities.
  - Compare pyrogenic carbon stocks and D13C signatures across altitudinal bands and disturbance levels.
  - Integrate with forest trait data and broader BioResilience findings to inform management and restoration strategies in Andean forests.

## References
- Ascough et al. (2009). Hydropyrolysis as a new tool for radiocarbon pre-treatment and quantification of black carbon.
- Koele et al. (2017). Amazon Basin forest pyrogenic carbon stocks and deep storage.
- Quesada et al. (2010, 2011). Variations in soil chemical/physical properties in Amazon forests.
- Tiessen & Moir (1993). Total and Organic Carbon in soil analysis.
- Wurster et al. (2012). Quantifying pyrogenic carbon using hydrogen pyrolysis.