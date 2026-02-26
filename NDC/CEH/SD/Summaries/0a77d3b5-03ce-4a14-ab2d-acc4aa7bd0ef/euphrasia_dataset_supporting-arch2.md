# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland). There are three data files:

- Euphrasia_population_information.csv
- Euphrasia_trait_data.csv
- Euphrasia_genome_size_data.csv

## Overview
- Focus: native eyebright plants (Euphrasia) across Britain and Ireland, with emphasis on Fair Isle, Shetland.
- Purpose: provides standardized sampling, trait measurements, and genome size data to support analyses of intraspecific and interspecific variation.
- Linkages: associated with Becher et al. (2020, 2021) studies.
- Formats: three CSV data files containing population sampling, trait measurements (wild and common garden), and genome size data.

## Data files and contents

- Euphrasia_population_information.csv
  - Contains two tables:
    - Table 1: seeds used in a common garden experiment to test whether species differences persist under standardised conditions.
      - Fields: Euphrasia species, population code (label used in other data files), sampling site latitude and longitude.
    - Table 2: plant tissue used for genomic sequencing.
      - Fields: label (unique individual ID), Species (morphology-based), Fair Isle (yes/no), Ploidy (2x or 4x), Origin (sampling location detail).

- Euphrasia_trait_data.csv
  - Contains four tables reporting morphological trait measurements.
    - Tables 1 & 2: traits measured in the wild.
    - Tables 3 & 4: traits measured with seeds grown in a common garden at Royal Botanic Garden Edinburgh.
  - Data structure:
    - Values per species (Tables 1 & 3) and per population (Tables 2 & 4).
    - Traits measured on a defined sampling date in the field; in the common garden, at first flowering and at end of flowering.
    - Species data summarize three species:
      - Earc = Euphrasia arctica
      - Efou = Euphrasia foulaensis
      - Emic = Euphrasia micrantha
    - Population data align with population definitions in Euphrasia_population_information.csv.
    - Columns include means and standard errors (se).
  - Note: Further details on traits are provided in Becher et al. (2020).

- Euphrasia_genome_size_data.csv
  - Genome size measurements by flow cytometry for Euphrasia individuals.
  - Columns include:
    - Population_number (unique population ID)
    - Sample.number (collector number, if provided)
    - Sample.identity (Euphrasia species name)
    - Location.details (site name and county)
    - Lat, Long (coordinates)
    - pg2C (2C genome size in picograms)
    - S.D. (standard deviation of pg2C)
    - hybrid? (whether sample is a hybrid)
    - ploidy (ploidy level)
    - specPop (species-population concatenation used in analyses)
    - popMeans (mean genome size for a population, 1C value in pg)
    - popSd (SD of popMeans)
    - popN (number of individuals in a population)
    - spMeans (mean 1C genome size for a species in pg)
    - spSd (SD of spMeans)
    - spN (number of individuals measured per species)
    - pg1C (individual 1C genome size in pg)

## How this supports environmental monitoring and analysis
- Standardized, multi-level data across populations and species enable consistent monitoring of biodiversity traits and genome size variation.
- Spatially explicit: includes site coordinates and focal study site (Fair Isle), supporting geographic analyses and island-mainland comparisons.
- Data integration potential: structured to join population, trait, and genome data via population identifiers and species codes, facilitating comprehensive environmental-health-like assessments of biodiversity responses.
- Provenance and reproducibility: linked to published work (Becher et al. 2020, 2021), with clearly described metadata and measurement approaches (field and common-garden contexts).

## Data management and reuse considerations
- Cross-file linkage via population codes and species abbreviations (Earc, Efou, Emic) supports reproducible analyses.
- Trait data include means and standard errors, enabling uncertainty-aware comparisons across populations and environments.
- Genomic data provide both population-level and species-level summaries, useful for exploring genomic variation in relation to environmental or ecological factors.
- For deeper interpretation, consult Becher et al. (2020, 2021) cited in the references.

## Potential analyses and monitoring opportunities
- Compare genome size variation (2C/1C values) across geography, ploidy, and isolation (e.g., Fair Isle vs. other sites).
- Assess how morphological traits differ among species and populations in wild versus common garden settings.
- Integrate with external environmental data (climate, soil, habitat type) to examine environment-trait-genome relationships.
- Use population identifiers to map distributions and track potential changes over time if longitudinal data become available.

## References
- Becher H, Powell RF, Brown MR, Metherell C, Pellicer J, Leitch IJ et al (2021). The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights. Annals of Botany 128(5): 639-651.
- Becher H, Brown MR, Powell G, Metherell C, Riddiford NJ, Twyford AD (2020). Maintenance of species differences in closely related tetraploid parasitic Euphrasia (Orobanchaceae) on an isolated island. Plant Communications 1(6): 100105.