# Vegetation work

## Overview
- This document outlines field and laboratory methods to quantify vegetation, soil, microbial communities, and greenhouse gas fluxes to support GIS-based data visualizations and spatial analyses.
- Data are designed to be transformed into map layers showing biodiversity, functional traits, soil properties, and gas flux patterns.

## Data collected and variables

- Vegetation metrics
  - Four randomly placed 50 cm x 50 cm quadrats per site
  - Visual percent cover by species; species richness
  - Grass and forb percent cover; biomass (clipped, dried at 80°C, summed across quadrats)
  - Shannon diversity; community weighted mean (CWM) trait values drawn from trait databases

- Greenhouse gas flux (CO2, CH4, N2O)
  - Net ecosystem CO2 exchange, photosynthesis, respiration measured with soil collars and IRGA
  - Soil moisture, temperature, and PAR recorded
  - Calculations convert chamber measurements to fluxes (mg CO2 m^-2 h^-1)
  - Methane, CO2, and N2O sampled via reflective chambers with gas chromatography; time-staggered collections (0, 10, 20, 30 minutes)

- Soil sampling and properties
  - Six soil samples per site, 4 cm core width, up to 10 cm depth
  - Samples split for PLFA and DNA; remaining soil stored for processing
  - Bulk density (0–5 cm and 5–10 cm) after drying
  - pH (5 g soil, 1:1 with water)
  - Volumetric moisture content (drying to determine moisture)

- Lipidomics and fatty acids
  - Bligh and Dye extraction; lipid class separation (neutral lipids, glycolipids, phospholipids)
  - Internal standards; GC analysis for fatty acids (multiple chain lengths)
  - Data normalized to soil dry weight; bacteria-dominated FA profiles

- DNA sequencing
  - PowerSoil DNA extraction; 16S (bacteria) and 18S (eukaryotes) amplicons
  - Illumina MiSeq (600 cycles); dual-indexed libraries; >17 million reads per run
  - OTU clustering at 97% similarity; relative abundance per OTU per sample

- Soil fauna and nematodes
  - Soil cores collected; Berlese-Tullgren funnels for microarthropods and annelids
  - Hand-sorting of large earthworms; ethanol storage for later sorting
  - Nematodes extracted via wet extraction (24 h); stored for functional group identification

- Trait data
  - Plant traits: longevity, plant height, specific leaf area (SLA), root architecture, rooting depth, VAM affinity
  - Sources: LEDA traitbase, PlantATT, and related literature
  - Root architecture categories include fibrous, adventitious, bulbous, nodal, rhizomes, stolons, tap roots (with ordinal coding)

## Data processing and outputs

- Quality assurance and transformation
  - Data cleaning, normalization, and integration across methods
  - Harmonization of spatial and temporal resolutions for map-ready products
  - Documentation and metadata for traceability and reuse

- Potential GIS-ready outputs
  - Vegetation maps: species richness, percent cover by major groups (grasses/forbs), and biomass density per quadrat
  - Functional trait maps: CWM values for longevity, height, SLA, root architecture, rooting depth, and mycorrhizal affinity
  - Microbial community maps: OTU relative abundances (bacteria vs. eukaryotes) by sample
  - Soil property maps: pH, volumetric moisture, and bulk density layers
  - Gas flux maps: CO2, CH4, and N2O flux estimates across the site
  - Soil fauna and nematode distributions: abundance and functional group representations
  - Integrated faceted visuals: linking vegetation traits with soil properties and gas flux patterns

## Workflow, QA, and iterative refinement

- Iterative development and testing of early data products with end users (policy colleagues, clients, or the public)
- Cross-dataset verification to ensure compatibility of units, scales, and coordinate references
- Ongoing data quality checks to address inconsistencies across laboratories and instruments

## Data management challenges relevant to GIS

- Data are spread across multiple sources (field plots, lab analyses, sequencing facilities) and formats
- Varying spatial resolutions (quadrats, soil cores, plot-level aggregates) require harmonization
- Data gaps or uneven resolution at appropriate scales for map products
- Need for consistent data standards and metadata to enable reuse and integration
- Managing large, complex datasets (e.g., sequencing OTUs, PLFA profiles) and ensuring staff have requisite skills

## Notes on trait and methodological references

- Plant functional trait values drawn from established trait databases (e.g., LEDA, PlantATT) and literature
- Analytical approaches for trait calculations and microbial community analyses grounded in cited foundational works (e.g., Shannon-Weaver, PLFA methodologies)