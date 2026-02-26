# Bacterial community structure and soil process data from a sewage sludge amended upland grassland soil experiment, 2000 [NERC Soil Biodiversity Programme]

## Overview
- A dataset from the NERC Soil Biodiversity Thematic Programme focusing on how sludge and lime amendments affect bacterial community structure and soil processes in upland grassland.
- Located at the Sourhope Research Station, Cheviot Hills, Scotland; field experiment run in 1999–2000 with multiple treatments and temporal sampling.

## Study site, design and sampling strategy
- Location: Rigg Foot experimental field site, Sourhope Research Station (UK Ordnance Survey Grid Reference NT854196; acidic brown forest soils).
- Experimental design: randomised block with three replicates across four treatments — untreated control, lime only, sewage sludge only, sewage sludge with lime.
- Treatments and timing: lime applied (600 g m-2) across two years; anaerobically digested domestic sewage sludge applied ( August 1999; May 2000). Sampling began after sludge application; in 1999 root-zone samples; in 2000 only root-zone samples.
- Sampling: soil cores collected from all 12 plots over spring and summer of 1999–2000; in 2000 sampling occurred at 1, 3, 16, 30, and 58 days after sludge application (May 30, 2000).

## Data collected and analytical methods
- Soil characteristics: pH (1:2 soil:water), moisture, total carbon, total organic carbon, total Kjeldahl nitrogen, soil NH3; methods include standard soil chemistry analyses and LECO carbon analysis; samples stored at 4°C (within 7 days) or -70°C for molecular analyses.
- Soil process measurements: basal respiration (CO2 accumulation in sealed soils), nitrification potential (nitrite accumulation in chlorate-treated slurries); standard analytical protocols described.
- Molecular analyses: DNA extraction from soil; TTGE (temporal temperature gradient electrophoresis) of 16S rDNA fragments to assess eubacterial and ammonia-oxidizing bacteria (AOB) community structure; GC-clamped PCR products subjected to TTGE, with gel imaging and band pattern analysis.
- TTGE data analysis: band intensity and position quantified; similarity among TTGE profiles calculated with weighted Sorensen coefficients; clustering with UPGMA; time and treatment effects analyzed via two-factor ANOVA (time, treatment); exploratory PCA not used due to experimental design.

## Data structure and contents (datasets)
- Dataset 1034: Soil analysis data (2000)
  - Variables include: SAMPLE_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, pH, SM (moisture), TOC, TKN, RES (soil respiration), AM_OX (ammonia oxidation potential), NIT_RED (nitrification potential), METH_GEN (methane production), METH_OX (methane oxidation), among others; analyses performed May–August 2000; samples analyzed at University of Newcastle.
- Dataset 1035: Soil analysis data — Bulk Sampling Details (SAMPINFO)
  - Contains: SUID (Sampling Unit Identifier), BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT, SOIL_HORIZON, TIME_AFTER_SLUDGE, SAMPLE_TYPE; sampling details for May–August 2000.
- Dataset 1124: Numerical analysis of eubacterial community profiles (TTGE) (P2116_EUBACTERIAL_CP.csv)
  - TTGE data for eubacterial 16S rDNA fragments across treatments and sampling days; includes BAND1–BAND54 (presence/absence/intensity) and associated metadata (SUID, BLOCK, MAIN_PLOT, TREATMENT, DAYS_AFTER_SLUDGE, HORIZON).
- Dataset 1125: Numerical analysis of ammonia oxidizer community profiles (TTGE) (P2116_AMMONIA_OXIDISER_CP.csv)
  - TTGE data for ammonia-oxidizing bacteria; similar structure to 1124 with BANDs and relative intensities; includes DAYS_AFTER_SLUDGE and other identifiers.
- Dataset 1126: Numerical analysis of ammonia oxidizer community profiles for sludge-only treatment (P2116_AMMONIA_SLUDGE.csv)
  - TTGE data focusing on sludge-only treatment across all time points; includes BAND_NUMBER and RELATIVE_INTENSITY, along with standard sampling identifiers.
- Dataset 1127: Numerical analysis of ammonia oxidizer community profiles for untreated soil only (P2116_AMMONIA_UNTREATED.csv)
  - TTGE data for untreated soil across all time points; includes BAND_NUMBER and RELATIVE_INTENSITY and accompanying metadata.

## Data quality, access and usage notes
- Quality control: numeric range checks, formatting checks, and logical integrity checks were performed.
- Limitations: despite QA procedures, NERC cannot warrant the data's accuracy or fitness for any particular use; liability for use is disclaimed.
- Accessibility: data referenced to Sourhope Field Experiment; additional baseline data and context available via Environmental Information Centre (EIDC) catalogue; relevant literature and handbooks cited for methods and interpretation.

## Context and references
- Background and methodology linked to the NERC Soil Biodiversity Programme (1999–2000) and related publications (e.g., Gray et al. 2003; Griffiths et al. 2000; Scott et al. 2003; Usher et al. 2006).
- Supporting information available through EIDC catalogue records and associated data handbooks.