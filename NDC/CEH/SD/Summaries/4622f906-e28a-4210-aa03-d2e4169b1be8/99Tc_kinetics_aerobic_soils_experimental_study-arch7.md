# Supporting documentation

## Overview
- Reports measurements of soluble, adsorbed, and organically bound 99Tc concentrations in soils after laboratory contamination with 99TcO4 and incubation for 897 days.
- Aims to understand long-term bioavailability and transformation of 99Tc in aerobic soils under temperate conditions, informing models for environmental impact after radioactive waste disposal.
- Dataset derived from 20 soils from central England, across different land uses (arable, grassland, moorland/woodland).

## Study and data scope
- Soil sampling and characterization
  - Twenty topsoil samples (0–15 cm) collected; four sub-samples per site combined to form ~3 kg composite samples.
  - Sites encompass diverse locations and soil properties; Table 1 lists location, land use, latitude/longitude, organic carbon, and pH.
- Contamination and microcosm setup
  - Contaminated with 99TcO4 at approximately 108 µg 99Tc per kg dry soil.
  - Soils distributed into three bottles per site (triplicate microcosms) with a single lid hole to allow gas exchange.
  - Incubated in darkness at 10.0 ± 1.0 °C for 897 days.
- Temporal sampling
  - Physico-chemical transformations tracked periodically via a sequential extraction scheme (timepoints described as incubation days).

## Data structure and variables
- Table 1 (soil properties)
  - For each soil: site code, land use, coordinates, organic carbon (%), pH.
- Table 2 (sequential extraction results)
  - For each soil/timepoint: 
    - soluble_99Tc_µg_kg (extracted with 0.01 M KNO3)
    - adsorbed_99Tc_µg_kg (extracted with 0.16 M KH2PO4)
    - organic_99Tc_µg_kg (extracted with 10% tetramethyl ammonium hydroxide)
  - Incubation_days variable indicating days since contamination.
  - Units: µg 99Tc per kg dry weight (DW).
- Extraction scheme
  - Step 1: 0.01 M KNO3 (soluble Tc)
  - Step 2: 0.16 M KH2PO4 (specifically adsorbed Tc)
  - Step 3: 10% tetramethyl ammonium hydroxide at 90 °C (organically bound Tc on humic/fulvic matter)

## Analytical methods
- Instrumentation
  - ICP-MS (iCAP-Q, Thermo Fisher) with collision-cell using helium.
- Sample introduction
  - Auto-sampler with ASXpress module and PFA nebuliser; internal standards Ge, Rh, Ir added in HNO3 and TMAH matrices.
- Calibration and standards
  - Calibration with Radioactive Standard NIST SRM 4288B (99TcO4− in 0.001 M KOH) across multiple concentrations (0.5–25 µg L−1).

## GIS-ready implications and potential uses
- Spatial attributes
  - 20 soils with precise coordinates enable mapping of Tc speciation across sites and land-use types.
- Attribute enrichment
  - Soil pH and organic carbon content as covariates for spatial analyses and modeling Tc partitioning.
- Temporal and compositional insights
  - Time-resolved fractions (soluble, adsorbed, organic) enable mapping of Tc transformation kinetics across soils.
- Applications
  - Develop spatially explicit models of long-term Tc bioavailability in aerobic temperate soils.
  - Produce map-based data products showing how soil properties and land use influence Tc partitioning over time.

## Data quality and limitations
- Laboratory conditions: results reflect controlled microcosm experiments, which may not fully represent field conditions.
- Data completeness: some entries in the extraction dataset may be missing (denoted by “-”).
- Temporal resolution: specific sampling intervals are defined by incubation days, not necessarily uniform across soils.

## Provenance
- Authors: M. Izquierdo, E. Bailey, N. Crout, H. Sanders, S. Young and G. Shaw; Institution: School of Biosciences, University of Nottingham, United Kingdom.