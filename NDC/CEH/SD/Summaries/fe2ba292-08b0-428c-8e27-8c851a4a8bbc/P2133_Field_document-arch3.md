# Measurements of microarthropod community structure and diversity from an upland grassland experimental site [NERC Soil Biodiversity Programme]

## Overview
- Describes the NERC Soil Biodiversity Thematic Programme (started 1999) and its field experiment at Sourhope, Scotland, focusing on how soil microarthropod communities relate to soil fertility manipulations and ecosystem processes.
- Aims to understand soil biota diversity and their functional roles in key ecological processes by measuring microarthropod community structure, diversity, productivity, and below-ground functions.

## Study design and site
- Location: Sourhope field site, Cheviot Hills, upland grassland (~350 m altitude) with mixed grass species; semi-improved soil type.
- Experimental design: five replicate blocks, each containing six plots, with factorial treatments including nitrogen fertiliser (N), lime (CaCO3), both, or control.
- Treatments applied: N and lime applied in specified years; plots mowed multiple times per growing season.
- Sampling scheme: soil cores collected at multiple times (Nov 1999, Feb 2000, May 2000, Aug 2000) from all blocks/plots; additional paired cores for some August sampling.
- Measurements span above-ground productivity (ANPP) and below-ground biodiversity and function.

## Data collected and key variables
- Microarthropod data:
  - Abundance and species composition of microarthropods (mites and Collembola); identification and counting.
  - Diversity metrics: Shannon-Wiener index (H), evenness (J), cumulative species richness (R).
  - Group-level diversity: overall mites and Collembola; functional diversity for predatory vs non-predatory mites.
  - Microarthropod community biomass estimated from group-specific conversion factors.
- Plant and above-ground productivity:
  - ANPP estimates from 0.25 m² quadrats across five mowing occasions.
- Soil and root analyses:
  - Dry root biomass per core; total C and N in roots and soil (via automated elemental analysis).
  - Soil moisture, pH (wet method), organic matter (loss on ignition).
  - Microbial biomass carbon via fumigation-extraction (CHCl3) and CO2 soil respiration.
  - Additional soil metrics: percent moisture, LOI, and C:N ratios.
- Data collection methods:
  - Microarthropods extracted with Berlese-Tullgren funnels; identification of Collembola and mites using standard taxonomic references.
  - Microbial biomass C measured using defined fumigation-extraction protocol.
  - Soil respiration measured as CO2 evolution after 24 h incubation at 25°C.
  - C and N analyses performed with Dumas method on dried, ground samples.

## Data structure and formats
- Dataset 1040: Plant species data (P2133_FIELD_BOTANICAL_PERCENT.csv)
  - Fields include: SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, SPECIES.
- Dataset 1041: Field microarthropod population density data (P2133_FIELD_MPOD_NUMBERS.csv)
  - Fields include: SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, MITES, COLLEMBOLA, DEPTH_FROM, DEPTH_TO.
- Dataset 1042: Field microarthropod species abundance data (P2133_FIELD_MPOD_SPECIES.csv)
  - Fields include: SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, SPECIES, COUNT.
- Dataset 1043: Field soils data (P2133_FIELD_SOILS.csv)
  - Fields include: SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, BIOMASSC, RESPIRATION, PH, LOI, ROOT, SOIL_C_N, ROOT_C_N, PERCENT_MOISTURE, DEPTH_FROM, DEPTH_TO.
- Each dataset is accompanied by a detailed data dictionary describing field purpose, data types, units, and missing values.

## Measurements, methods and quality
- Measurement techniques:
  - Microarthropods: Berlese-Tullgren extraction; taxa identification and counting; biomass estimates from taxon-specific factors.
  - Soil microbes and processes: fumigation-extraction for microbial biomass C; soil respiration via headspace CO2; LOI for organic matter; soil pH.
  - Plant biomass: above-ground productivity from repeated quadrats.
  - Root and soil chemistry: dry root biomass; total soil/root C and N; soil moisture.
- Quality control:
  - Numerical range checks, data formatting checks, and logical integrity checks implemented.
  - Data subject to quality assurance, but the programme (NERC) does not warrant accuracy or fitness for a particular use and disclaims liability for data use.
- Documentation and references:
  - Rich supporting literature, including methodological references for all analyses; Sourhope Field Data Handbook and related materials referenced for data usability and context.

## Implications for monitoring frameworks
- Demonstrates the value of a well-documented, multi-metric monitoring approach that combines biodiversity (diversity indices, species composition) with functional and ecosystem-process measures (biomass, respiration, C/N dynamics).
- Highlights the importance of:
  - Comprehensive metadata and data dictionaries to enable data reuse and governance.
  - Transparent data provenance, including sampling design, depth, plots, treatments, and sampling dates.
  - Standardized measurement protocols and QA procedures to support comparability and quality.
  - Public sharing of underlying data and clear data governance statements, while acknowledging potential barriers (metadata gaps, data ownership, and data sharing requirements).
- Illustrates effectiveness of factorial, replicated experimental designs in isolating treatment effects on below-ground biodiversity and ecosystem function.
- Provides a concrete model for structuring environmental health indicators (diversity, biomass, microbial activity, soil chemistry) to inform policy scrutiny, evaluation, and future decision-making.