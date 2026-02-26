# Soil invertebrate data 2007 [Countryside Survey], Great Britain

## Overview
- Dataset of soil invertebrate (mesofauna) counts from samples taken at 0-8 cm depth.
- Collected from up to 256 1km squares across Great Britain, surveyed in 2007 (CS2007).
- Includes counts for a wide range of major taxa, plus derived biodiversity and abundance metrics.

## Data structure and key variables
- Site and sampling identifiers:
  - SQUARE: 1km square sampling site code
  - PLOT: Plot identifier within each square
  - YEAR: Year of survey (2007)
- Taxa counts (numerical counts for each group), e.g.:
  - Acari (ACTO), Araneae (ARAN), Chilopoda (CHTO, CHGE, CHLI), Coleoptera (COLA, COAD),
    Collembola groups (EN, CONE, COPU, COSM, COPE), Diptera (DILA, DIAD), Gastropoda (GAST),
    Isopoda (ISOP), Lepidoptera (LEAD, LELA), Nematoda (NEMA), Oligochaeta (OLIG),
    Other groups (e.g., Diplura DIPL, Opilones OPIL, Pseudoscorpions PSEU, PSOC, etc.)
- Derived metrics (per core or per square as defined in the dataset):
  - TOTAL_CATCH: total invertebrates
  - COLL_TOTAL: total Collembola
  - AC_COLL_TOTAL: total mites and Collembola
  - MC_RATIO: ratio of mites to springtails in soils (0-8 cm depth)
  - TOTAL_TAXA: total invertebrate taxa richness
  - SHANNON: Shannon diversity index (dimensionless)
- Metadata and classification:
  - LC07, LC07_NUM: ITE Land Class 2007 (text and numeric code)
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: County or Council area
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Acknowledgement and rights:
  - Data must be acknowledged as Countryside Survey data owned by CEH/NERC
  - Countryside Survey © and related rights reserved

## Sampling design and scope
- Field strategy aligned with the Countryside Survey’s rigorous stratified sampling design.
- Great Britain stratified into Land Classes to reflect environmental gradients.
- 2007 sampling comprised 591 sample squares (289 England, 107 Wales, 195 Scotland).
- Soil cores collected from the top 0-15 cm region in field plots historically; for 2007, soil cores contributed toward 0-8 cm depth analyses within sampled squares.
- 921 soil cores analyzed across the study; 3-5 cores randomly selected from each set of five plots per square for analysis.

## Laboratory methods
- Extraction: Dry Tullgren extraction to separate soil fauna, conducted over 5 days.
- Processing: Soil cores placed on sieves, heated with a 40 W light to drive fauna into collection bottles containing 70% ethanol.
- Identification: Organisms identified to major taxa (taxonomic level 1); Collembola and mites identified to morphotype level.
- Core handling: Cores logged, processed for basic measurements, chemical analyses, and archival storage.

## Quality control and quality assurance
- Identification QC: After taxonomic 1-level identification, 1 in 10 of the first 500 samples re-counted/validated by a second staff member; discrepancies resolved and notes recorded.
- Ongoing QC: Recounts decreased progressively through the remaining samples; a small number of very small taxa may be lost during transfer between containers.
- QA framework: Adheres to Defra/NERC joint Codes of Practice.
- Data integrity: All data and methods are documented; changes and corrections logged.

## Documentation and references
- Primary protocol and methodologies:
  - Emmett, B.A. et al. 2008. Countryside Survey. Soils Manual. NERC/CEH; CS Technical Report No. 3/07.
  - Countryside Survey 2007 Soils Manual (CS2007 website documentation and related publications).
- Related publications and datasets:
  - Countryside Survey: UK Results from 2007 (Carey et al. 2008)
  - ITE Land Classification of Great Britain (Bunce et al. various years)
- Access and further information:
  - Countryside Survey website: http://www.countrysidesurvey.org.uk/
  - CS Soils Manual and technical reports referenced in Emmett et al. 2008

## Usage considerations for data analysts
- Suitable for examining correlations between soil invertebrate abundance/diversity and soil properties, land-class gradients, and geographic region (England, Scotland, Wales).
- Derived metrics (TOTAL_TAXA, SHANNON, MC_RATIO, etc.) facilitate biodiversity and community structure analyses.
- Ensure proper acknowledgment of Countryside Survey data (CEH/NERC) in any publication or presentation.
- Be mindful of depth scope (0-8 cm in dataset) versus broader soil depth contexts described in the soils manual (0-15 cm in some historic surveys).
- Refer to the CS2007 Soils Manual for sampling, QC, and statistical analysis procedures if replicating or integrating with other CS datasets.