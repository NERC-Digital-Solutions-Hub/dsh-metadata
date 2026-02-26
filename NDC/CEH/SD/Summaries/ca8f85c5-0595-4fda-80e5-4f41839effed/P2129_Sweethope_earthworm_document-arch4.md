# Supporting Information

## Overview
- Describes the Sweethope earthworm mesocosm experiment within the NERC Soil Biodiversity Programme.
- Final sampling occurred in October 2001; dataset captures earthworm abundance/biomass and botanical composition at the end of the experiment.
- Two CSV datasets are provided:
  - 2129_BOTANICAL_COMPOSITION.csv (Dataset 1009)
  - P2129_EARTHWORM_SURVEY.csv (Dataset 1010)
- Includes data collection methods, experimental design, and metadata to support reuse, with quality control notes and literature references.

## Datasets and Content
- Dataset 1009: Sweethope Endpoint Botanical Composition Data
  - Fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C=Control, L=Limed), SPECIES, BOTANICAL_COMPOSITION (Braun-Blanquet scale 0–6)
  - Purpose: botanical composition of each experimental treatment at the end of the Sweethope experiment (16–17 Oct 2001)
- Dataset 1010: Sweethope Endpoint Earthworm Survey Data
  - Fields: SAMPLE_ID, SAMPLING_DATE, BLOCK, MAIN_PLOT, SUB_PLOT, CELL_X, CELL_Y, TREATMENT (C/L), SPECIES, ABUNDANCE (per m^2), BIOMASS (per m^2)
  - Purpose: earthworm census (abundance/biomass) at the end of the experiment (16–17 Oct 2001)

## Experimental Design & Sampling Context
- Site and setup:
  - Main Sourhope experimental site in southern uplands of Scotland; 100 soil boxes removed and reburied 100 m away at Sweethope to prevent contamination, forming an enclosure for the experiment.
  - Layout mirrored the main plots: 5 rows with replicated treatments within each row.
- Treatments:
  - No earthworm inoculation
  - Epigeic species inoculation (one species)
  - Endogeic species inoculation (one species)
  - Anecic species inoculation (one species)
  - All three functional groups inoculated (ABC)
- Inoculation details:
  - Epigeic: Lumbricus rubellus, 20 individuals/box
  - Endogeic: Allolobophora chlorotica, 15 individuals/box
  - Anecic: Lumbricus terrestris, 4 individuals/box
  - Inoculations conducted April 2000; soil boxes designed to prevent escape and allow reburial
- Additional management:
  - Lime treatments applied in line with Sourhope plots
  - Grass harvested from boxes roughly every two weeks; clippings analyzed for biomass
  - 50 boxes contained undisturbed soil; the remaining served as main experimental blocks with treatments

## Data Collection Methods
- Earthworm census:
  - Hand-sorting used to count and identify earthworms (avoiding chemical extraction biases)
  - Species identification via Sims & Gerard (1985); abundance and biomass calculated per m^2
  - Post-sorting, worms stored on damp tissue, then weighed to obtain biomass per m^2
- Botanical composition:
  - Plant species presence recorded using Braun-Blanquet scale at experiment end
  - Data capture aligned with Scott et al., 2003 framework

## Data Structure and Metadata
- Data are provided as two comma-separated value files with explicit column descriptions and data types:
  - 2129_BOTANICAL_COMPOSITION.csv
  - P2129_EARTHWORM_SURVEY.csv
- Column-level details include sampling metadata (date, sample identifiers, plot blocks), treatment identifiers, spatial coordinates (CELL_X, CELL_Y), and species-level measurements (BOTANICAL_COMPOSITION, ABUNDANCE, BIOMASS)
- Data dictionaries and accompanying methodological notes help interpret the grid-based sampling and replicates

## Data Quality and Access
- Quality control:
  - Numeric range checks, formatting, and logical integrity checks implemented
- Limitations and liabilities:
  - Data are subject to quality assurance, but the providers (NERC) do not guarantee accuracy or fitness for a particular use
  - No liability for misuse or misinterpretation of the data
- References and further reading provided to contextualize methods and results (e.g., Bishop et al. 2008; Scott et al. 2003; Sims & Gerard 1985; Spring 2003; Usher et al. 2006)

## References
- Bishop, H.O., Grieve, I.C., Chudek, J.A., & Hopkins, D.W. (2008). Liming upland grassland: effects on earthworm communities and soil carbon characteristics. European Journal of Soil Science.
- Scott, J., Bell, J., Kenny, C., Jeffers, J., Buckland, S., Burt-Smith, G. (2003). SOURHOPE FIELD DATA HANDBOOK 2003.
- Sims, R.W., & Gerard, B.M. (1985). Earthworms: keys and notes for identification and study of the species.
- Spring, C.A. (2003). The effects of earthworms on soil structure in an upland grassland. PhD Thesis.
- Usher, M.B., Sier, A.R., Hornung, M., Millard, P. (2006). Understanding biological diversity in soil: the UK’s Soil Biodiversity Research Programme. Applied Soil Ecology.