# Discovery metadata- Soil nutrients, soil pyrogenic carbon, soil bulk density and roots dry weight under different intensities of soil management in the Colombian Andes between 2019-2021

## Overview
- A multi-file soil dataset from 27 forest monitoring plots across a Colombian altitudinal gradient (lowland, midland, highland) and a forest disturbance gradient (low, medium, high perturbation).
- Data collected 2019–2022 within the BioResilience project to study changes in soil characteristics with perturbation and their relation to forest resilience.
- Supported by UK Natural Environment Research Council (NE/R017980/1).

## Dataset composition
- Four CSV files:
  - pyrogeniccarbonbr.csv: Aerial/soil carbon metrics including TOC, pyrogenic carbon (Cpyc), D13C for pyrogenic carbon, Cpyc%/CBulk, %OC, depth ranges, plot and sample identifiers.
  - soilnutrientbr.csv: Soil chemistry and particle-size data including pH, available phosphorus, total phosphorus, sand/clay/silt, exchangeable Ca, Mg, K, Na.
  - bulkdensitybr.csv: Bulk density data with plot code, depth, date, and location metadata (Municipio, Departamento, Farm, Land_use, Ecosystem).
  - dryweigthbr.csv: Roots dry weight data by plot and depth with corresponding location metadata.
- Each file includes consistent plot coding (Plot_code 1–27) and location metadata aligned to the study sites.

## Sampling design and locations
- 27 permanent monitoring plots of 0.5 ha each.
- Altitudinal gradient categories:
  - Lowlands, Midlands, Highlands with specific localities described (e.g., Serranía de las Quinchas, Pedro Palo, Encino, Encenillo, Martos).
- Disturbance gradient categories:
  - Low, Medium, High perturbation; three plots per perturbation level per location.
- Coordinates and site descriptions provided to contextualize environmental variability.

## Methods and data processing
- Pyrogenic carbon and TOC
  - TOC (%C_bulk) determined by elemental analysis (Costech ECS-4010).
  - Pyrogenic carbon (Cpyc) analyzed via hydrogen pyrolysis (HyPy).
  - Cpyc%/C_bulk calculated from HyPy results; stable PyC fraction quantified per Wurster et al. 2012 methods.
  - D13C values provided for pyrogenic carbon (Lower/Median/Upper) with associated errors.
- Soil nutrients and textures
  - pH measured in water after 1-hour extraction.
  - Available P via sequential extraction; total P by acid digestion (Tiessen & Moir, 1993).
  - Particle-size analysis by Bouyoucos method (sand, silt, clay).
  - Exchangeable Ca, Mg, K, Na using Ag-TU extraction.
- Bulk density and roots
  - Bulk density derived from pit samples; roots dry weight measured by standard drying methods.
- Data transformations and documentation
  - Documentation covers measurement units, calibration steps, and correction factors (e.g., a noted erratum for a PyC% equation in Wurster et al. 2012).
  - Data were calibrated against literature reference values prior to analysis.

## Data quality, metadata, and governance
- Calibration and instrument checks conducted before measurements.
- Quality control includes: external review of database structure, completeness, typing, removal of duplicates, and metadata validation for accuracy and consistency.
- Metadata emphasize data structure, units, valid ranges, detection limits, and per-replicate data details.
- Clear data provenance: project context, sampling, laboratory analyses, and analytic references are provided.

## Data schema and units
- pyrogeniccarbonbr.csv (14 columns): Plot_code, depth_range_cm, depth_upper_cm, depth_lower_cm, depth_mid_cm, Sample_Id, Project/Collected, %C_(Bulk), Lower_D13C_(pyc), Median_D13C_(pyc), Upper_D13C_(pyc), Cpyc_(%), %Cpyc/Cbulk, %OC.
  - Units: %C_(Bulk) (%), D13C (‰), Cpyc (%) and related ratios, %OC (%).
- soilnutrientbr.csv (11 columns): Plot_code, pH, p_available, tot_p, sand, clay, silt, Ca_ex, Mg_ex, K_ex, Na_ex.
  - Units: pH (dimensionless), mg/kg for available P, % for texture, cmolc/kg for exch. cations.
- bulkdensitybr.csv (10 columns): Plot_code, Depth, Date_sample_taking, Municipio, Departamento, Farm, Land_use, Ecosystem, Bulk_density.
  - Units: Bulk_density (g/cm3); Date as MM/DD/YY.
- dryweigthbr.csv (7 columns): Plot_code, Ecosystem, Land_use, Municipio, Departamento, Depth, Dry_weight.
  - Units: Dry_weight (g).

## Provenance, references, and usage notes
- Project: BioResilience—transdisciplinary study of forest resilience after post-conflict in Colombia.
- Key references for methods and interpretation: Hydropyrolysis for PyC, PyC and OC quantification methods (HyPy), and standard soil carbon/nutrient analysis protocols (Quesada et al., Tiessen & Moir, Gee & Bauder, etc.).
- Data suitable for analyses of soil nutrient status, pyrogenic carbon stocks, soil bulk density, and root biomass across disturbance and elevation gradients, with careful attention to depth, plot, and ecosystem context.
- Data sharing and updates implied by the governance framework; structure supports discovery and reuse in data portals.