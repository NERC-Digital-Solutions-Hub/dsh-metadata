# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland)

## Overview
- A multi-file dataset documenting Euphrasia populations across Britain and Ireland, with a focal sampling site on Fair Isle.
- Supports analyses of species differences, trait variation, and genome size variation, including comparisons between wild populations and common garden experiments.
- References provided to key studies (Becher et al. 2020, 2021) for context and methodological details.

## Datasets and contents
- Euphrasia_population_information.csv
  - Table 1: seeds used in a common garden experiment to test whether species differences persist under standardised conditions.
    - Fields: Euphrasia species, population code (label), sampling site latitude/longitude.
  - Table 2: Euphrasia samples used for genomic sequencing.
    - Fields: label (unique individual), Species (morphology-based), Fair Isle (sampling location status), Ploidy (2x or 4x), Origin (sampling location detail).

- Euphrasia_trait_data.csv
  - Four tables reporting morphological trait measurements.
    - Measurements conducted in the wild (Tables 1 & 2) and in a common garden (Tables 3 & 4).
    - Data structured by species (Tables 1 & 3) and by population (Tables 2 & 4) using population codes from Euphrasia_population_information.csv.
    - Timing: field sampling date; common garden measurements at first flowering and end of flowering season.
    - Descriptions indicate three species (Euphrasia arctica, Euphrasia foulaensis, Euphrasia micrantha) with column headers reflecting species, while population tables use population labels.
    - Includes mean values and standard errors (se); further trait details are documented in Becher et al. (2020).

- Euphrasia_genome_size_data.csv
  - Genome size measurements by flow cytometry for wild-collected Euphrasia tissue.
  - Key fields: Population_number, Sample.number, Sample.identity, Location.details, Lat, Long, pg2C (2C size in pg), S.D. (standard deviation), hybrid?, ploidy, specPop (species+population), popMeans, popSd, popN, spMeans, spSd, spN, pg1C (1C size in pg).
  - Describes methodology: PI-stained nuclei, internal standard Oryza sativa IR36, with references to Becher et al. (2021).

## Provenance and references
- Data linked to published analyses:
  - Becher et al. (2020): Maintenance of species differences in closely related tetraploid Euphrasia on an isolated island.
  - Becher et al. (2021): The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights.
- Sampling focus on Fair Isle (Shetland, Scotland) with broad geographic coverage across Britain and Ireland.

## Data model and relationships
- Population codes in Euphrasia_population_information.csv underpin population-based trait (Euphrasia_trait_data.csv) and genome-size analyses (Euphrasia_genome_size_data.csv).
- Three data streams:
  - Population sampling and demographics (Table 1 and 2 in population file).
  - Morphological trait variation (wild and common garden; Tables 1–4 in trait data).
  - Genomic genome size variation (2C and 1C estimates; genome data file).
- Metadata conventions include species labels, ploidy, origin details, and location coordinates to enable geographic analyses and reproducibility.

## Data quality, standards, and governance
- Data appears structured with explicit means and standard errors for traits, and explicit 2C/1C genome size measurements with associated statistics.
- Potential data-asset considerations for data leaders:
  - Ensure consistent mapping between population codes across files.
  - Maintain clarity on species identity vs. morphology-based labeling (Euphrasia arctica, foulaensis, micrantha).
  - Verify metadata completeness for sampling sites (location details, coordinates, origin).
  - Document data processing steps (how Table 1 vs Table 2 in population file were derived; handling of hybrids).
  - Align citations and ensure accessible references to Becher et al. (2020, 2021) for methodology and interpretation.

## Potential uses and value for data strategy
- Comparative analyses of species differences under standardized conditions (common garden) and in natural environments.
- Investigation of trait variation across species and populations, including geographic patterns.
- Exploration of genome size diversity within and between Euphrasia species, and its relation to ploidy and hybrid status.
- Integration into broader data ecosystems focusing on plant biology, speciation, and genome size variation; potential to inform cross-network collaborations given the Fair Isle focus.

## Access, reuse, and next steps
- Link data assets to the cited Becher et al. studies for methodological context and validation.
- Facilitate discoverability by registering dataset metadata (titles, authors, collection dates, locations, DOIs if available).
- Plan for data updates or extensions (additional populations, more trait measurements, ongoing genome-size assessments).
- Ensure licensing and usage rights are clear for downstream analyses and sharing.