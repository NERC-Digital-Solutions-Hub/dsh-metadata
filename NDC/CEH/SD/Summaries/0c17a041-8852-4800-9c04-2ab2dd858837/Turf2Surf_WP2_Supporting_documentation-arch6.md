# Turf2Surf WP2 Supporting documentation for data

## Overview
- The Turf2Surf project (WP2) investigates coupled nutrient cycling in terrestrial and freshwater ecosystems, focusing on nitrogen and phosphorus impacts on carbon exchange and including measurements linked to JULES model parameters.
- WP2 aims to connect plant and soil nutrients to aboveground and belowground processes to inform data products and model inputs.
- This document describes the Conwy catchment data collection (habitats, sites) and the suite of measurements (biomass, productivity, plant physiology, leaf traits, soils, nutrients, and TXRF elemental analysis) collected between 2013 and 2016.

## Data scope and datasets
- Location: Conwy catchment, North Wales (~500 km2) with diverse habitats and climatic gradient.
- Datasets cover:
  - Aboveground biomass production and standing biomass
  - Plant photosynthesis measures (Vcmax, Jmax, Asat)
  - Leaf and plant community traits (N, P, LDMC, SLA, LMA, canopy height, bryophyte cover)
  - Soil properties (pH, bulk density, LOI, total C and N, EC)
  - Soil phosphorus pools and related measures (Olsen P, Root P, Complex-P, Enzyme-P, Proton-P)
  - Soil available carbon and nitrogen (DOC, TDN) and nitrate/ammonium analyses
  - Soil available cations (Ca, Na, K)
  - Root biomass (standing and in-growth roots) and root analysis (WinRhizo)
  - Soil elemental composition by TXRF (multi-element spectrum)
- Data products are organized into five CSV files (see Dataset structure).

## Habitats and sites
- Table of habitats identifies 23 site entries with unique site numbers, plot counts, and dominant plant descriptions.
- Sites include blanket bog, moorland, acid grassland, conifer woodland, broadleaved woodland, oakwood, juniper gill, hay meadows, improved/paddock grasslands, montane areas, arable land, and semi-improved grasslands.
- Sampling locations were spread across the Conwy catchment to capture habitat diversity and allow linking to ecosystem processes.

## Measurements and data types

- 3.1.1 Aboveground net primary productivity (NPP) and standing biomass
  - NPP measured annually (2013–2015) for dominant species across sites; winter clipping with grazing exclusion in some habitats.
  - Aboveground standing biomass estimated for 10 of 17 sites; methods differ by habitat (herbaceous vs. woodland).

- 3.1.2 Plant photosynthesis measures
  - Vcmax, Jmax, Asat measured for dominant species using CIRAS-I with CO2 chambers and Licor 6400 systems.
  - Data processed via fitting to Farquhar model (A-Ci curves) with temperature corrections; scripts and code provided (GitHub link).

- 3.1.3 Leaf traits and plant community traits
  - Measurements: leaf N, leaf P, LDMC, SLA, LMA, canopy height, bryophyte cover.
  - Leaf trait analyses tied to downstream parameterization for JULES; details on sampling, scanning, and analysis.

- 3.2.1 General soil measures
  - Intact soil cores collected to 1 m depth; analyses include SWC, BD, LOI, LOI-C, pH, EC, total C and N (via elemental analyzer).
  - QA/QC processes and multi-depth sampling across habitats.

- 3.2.2 Phosphorus
  - Olsen P, Root-P, Complex-P, Enzyme-P, Proton-P measurements.
  - Methods include colorimetric assays (Malachite Green) and extractions (Olsen P, 0.01 M CaCl2 for Root-P, citrate extractable P, enzyme-based extractions, HCl for recalcitrant P).
  - Data processing follows established references; detailed protocols provided.

- 3.2.3 Available carbon and nitrogen
  - DOC and TDN measured from soil extracts (0.5 M K2SO4 extraction); high-level QA and batch processing described.

- 3.2.4 Soil available cations (Ca, Na, K)
  - 0.5 M acetic acid extraction followed by flame photometry; QA/QC and unit conversions described.

- 3.2.5 Root biomass
  - Standing root biomass and fine/root length measurements via WinRhizo after soil cores; in-growth root cores to assess root growth over a season.
  - Biomass calculations (dry weight) and comparisons to aboveground biomass.

- 3.2.6 Soil elements – TXRF
  - Total elemental analysis for 30+ elements using TXRF; sample preparation, internal standards, and calibration steps described.
  - Limitations and considerations noted; analysis performed across 17 sites.

## Data processing and model integration
- WP2 links plant and soil nutrient data to ecosystem processes to inform JULES model parameters.
- NPP, leaf traits, photosynthesis parameters (Vcmax, Jmax) etc. are used to derive model inputs and calibrate ecosystem function representations.
- Specific data processing steps:
  - NPP data and processing described in Turf2Surf_WP2_NPP_Smart.rft (detailed methodology).
  - Photosynthesis parameter fits use Levenberg–Marquardt algorithm and Bernacchi temperature corrections; Farquhar model applied to A-Ci curves.
  - Leaf traits and biomass data processed to derive trait components needed for model inputs.

## Dataset structure and files
- The data are organized into five CSV files:
  - Turf2Surf_Plant_biomass_data.csv
  - Turf2Surf_Plant_structural_data.csv
  - Turf2Surf_Plant_physiological_data.csv
  - Turf2Surf_Soil_Carbon_data.csv
  - Turf2Surf_Soil_raw data.csv
- Common schema elements:
  - Column A: Site number (matches Habitat Table 1)
  - Column B: Habitat
  - Column C: Detailed Habitat description
  - Column D: Site name
  - Column E: Ecosystem Component (plant, soil, or roots)
  - Column F: If Plant, the specific plant species; otherwise NA
  - Column G: Plot number
  - Column H: Replicate number (used when plots are proximate but measurements are tied to dominant species)
  - Column I: Soil depth interval (for soil and root components)
- Missing values are indicated as NA due to restricted depths, limited replicates, or outliers.

## Data quality, QA/QC and limitations
- QA/QC processes exist for soil carbon and nitrogen analyses; calibration and standard curves used for P measurements and TXRF analyses.
- TXRF limitations are discussed in Turf2Surf_WP2_TXRF_Limitations_Glanville.rft.
- Data are tied to field sampling limitations (depth constraints, replicate availability) and units are explicitly defined within methods.

## Roles, contact and version history
- Data responsible contacts include: Simon Smart, Bridget Emmett, Lina Mercado, Helen Glanville, and Sabine Reinsch, among others.
- Version dates noted for the document: 01/06/2016; 25/08/2016; 04/11/2016.
- Authors: Sabine Reinsch (corresponding author), Helen Glanville, Simon Smart; and collaboration across CEH and Bangor/Exeter.

## Practical notes for data users
- Use the site and habitat classifications to link measurements across plant and soil domains.
- When integrating into models (e.g., JULES), reference the processing scripts for NPP, photosynthesis, and leaf trait conversions to model-ready parameters.
- Be mindful of depth- and habitat-specific sampling limits when aggregating or comparing across sites.
- The five CSV files are designed to be cross-referenced via Site number, Plot, Replicate, and depth where applicable.