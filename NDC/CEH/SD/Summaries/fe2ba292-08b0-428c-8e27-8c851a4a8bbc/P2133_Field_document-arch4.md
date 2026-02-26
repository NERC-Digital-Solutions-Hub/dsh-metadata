# Measurements of microarthropod community structure and diversity from an upland grassland experimental site [NERC Soil Biodiversity Programme] Cole, L., Bardgett, R.D. and Buckland, S.M.

## Overview
- Part of the NERC Soil Biodiversity Thematic Programme (established 1999) focused on intensive study of a large field experiment at Sourhope, Scottish Borders.
- Aimed to understand soil biodiversity and the functional roles of soil organisms in key ecological processes.
- 24 projects studied soil structure, processes (carbon and nitrogen cycles), and roles of micro-fauna and micro-flora (bacteria, nematodes, protozoa, fungi) including microarthropods (mites, Collembola) and various macro/meso-fauna.
- Primary outputs include measurements of below-ground diversity and links to soil fertility manipulations.

## Study site, design, and sampling
- Location: Sourhope Field Experiment Site, Cheviot Hills, Scotland (55°28'30"N, 2°14'W), ~350 m altitude; semi-improved upland grassland.
- Climate: annual rainfall ~1117 mm; temperatures 3.8–12.2°C.
- Plant community: Agrostis capillaris, Festuca ovina, Poa pratensis, Anthoxanthum odoratum.
- Soil: humic brown (Sourhope series).
- Experimental design: five replicate blocks, each with six plots (12×20 m) and a randomized set of treatments.
  - Treatments: ammonium nitrate N fertiliser, calcium carbonate lime, both, or control (no fertiliser).
  - Treatment timing: N applied May 1999, Sept 1999, Apr 2000, May 2000; Lime applied May 1999 and Apr 2000.
  - Management: plots mowed five times per year; with cutting to 6 cm and removals.
- Sampling: soil cores collected across four occasions (Nov 1999, Feb 2000, May 2000, Aug 2000); additional paired cores in August for deeper analyses.
- Core details: 8 cm diameter, up to 10 cm depth for microarthropods; additional sampling down to 5 cm for roots and soils analyses.

## Data collected and variables
- Microarthropods: abundance and community structure of mites and Collembola; identification and counting of dominant taxa.
- Biomass and activity: microbial biomass carbon (fumigation-extraction), soil basal respiration.
- Soil and root chemistry: dry root biomass; total carbon (C) and nitrogen (N) content in soil and roots; soil moisture; pH (wet, with deionised water); organic matter via loss on ignition (LOI).
- Plant productivity: annual above-ground biomass (ANPP) estimates from multiple quadrats.
- Measurements and methods detailed, including equipment and analytical procedures (e.g., Dumas method for C/N, CHCl3 fumigation, infrared CO2 analysis).

## Data processing, indices, and analyses
- Taxonomic work: identification of Collembola and mites; grouping into dominant species and relative taxonomic units.
- Diversity metrics: Shannon-Wiener diversity index (H), evenness (J), and cumulative species richness (R) for microarthropods (overall and by group).
- Functional diversity: coarse indices for predatory vs. non-predatory mites.
- Biomass estimation: conversion factors from Luxton (1975) and Petersen (1975).
- Data management: standardized core processing and core replication information; five-block, main plot, sub-plot, and cell coordinates used to map sampling units.

## Datasets and data structure
Four comma-separated datasets are provided:
- Dataset 1040: Plant species data (P2133_FIELD_BOTANICAL_PERCENT.csv)
  - Contents: plant species per sampling unit/core; fields include SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, SPECIES.
- Dataset 1041: Field microarthropod population density data (P2133_FIELD_MPOD_NUMBERS.csv)
  - Contents: microarthropod counts per core; fields include SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, MITES, COLLEMBOLA, DEPTH_FROM, DEPTH_TO.
- Dataset 1042: Field microarthropod species abundance data (P2133_FIELD_MPOD_SPECIES.csv)
  - Contents: species-level abundances per core; fields include SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, SPECIES, COUNT.
- Dataset 1043: Field soils data (P2133_FIELD_SOILS.csv)
  - Contents: soil conditions and root data; fields include SUID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SAMPLE_TYPE, SURFACE_AREA, BIOMASSC (microbial biomass carbon), RESPIRATION (soil respiration), PH, LOI, ROOT (dry root biomass/core), SOIL_C_N, ROOT_C_N, PERCENT_MOISTURE, DEPTH_FROM, DEPTH_TO, etc.
- Each dataset contains extensive metadata describing data types, units, sampling hierarchy (Block, Main Plot, Sub-Plot, Cell), and analysis context.

## Quality control, governance, and caveats
- Quality control included numeric range checks, formatting verification, and logical integrity checks.
- Data are subject to quality assurance procedures; however, the issuing organizations do not warrant accuracy or fitness for a particular use and accept no liability for outcomes from data usage.
- The data come with detailed documentation to support discoverability and reuse, including data dictionaries and referenced methodological sources.

## Data lineage and references
- Core methodological and analytical references cited for procedures (e.g., Berlese-Tullgren extraction, microbial biomass via fumigation-extraction, Dumas method for C/N, pH measurement, LOI, respiration).
- Related literature and data handbook suggestions: Sourhope Field Data Handbook (2003), and publications on soil biodiversity and microarthropod diversity in temperate grasslands.
- Links to broader context: understanding relationships between soil microarthropod diversity, soil fertility manipulations, and below-ground ecosystem processes.

## Usage and implications for data leadership
- Demonstrates a well-documented, factorial field experiment with robust replication and long-term sampling suitable for data strategy around data provenance, metadata richness, and reproducibility.
- Provides structured, multi-dimensional data (taxonomic, functional, chemical, and productivity measures) across spatial (block/plot) and temporal (seasonal sampling) scales.
- Highlights the importance of clear data schemas, sampling unit identifiers (SUID), and comprehensive data dictionaries to support discoverability and cross-project collaboration.
- Serves as a model for end-to-end data governance: definition of variables, data capture protocols, processing workflows, quality control, and explicit disclaimers about data accuracy.