# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland). There are three data files:

## Overview
- Documents native eyebright (Euphrasia) populations across Britain and Ireland, with emphasis on Fair Isle.
- Integrates population sampling, trait measurements, and genome size data to support comparative analyses under wild and common-garden conditions.
- Aligns with published analyses (Becher et al. 2020, 2021).

## Data Files and Key Content

- Euphrasia_population_information.csv
  - Contains two tables:
    - Table 1: Seeds used in a common garden experiment
      - Fields: Euphrasia species, population code (label used in other files), sampling site latitude and longitude.
    - Table 2: Plant tissue used for genomic sequencing
      - Fields: label (unique individual), Species (morphology-based), Fair Isle flag, Ploidy (2x or 4x), Origin (sampling location details).

- Euphrasia_trait_data.csv
  - Four tables of morphological trait measurements
    - Measured in the wild (Tables 1 & 2) and in a common garden (Tables 3 & 4)
    - Values by species (Tables 1, 3) and by population (Tables 2, 4)
    - Sampling dates differ for wild vs. garden measurements (defined dates)
    - Species abbreviations: Earc = Euphrasia arctica, Efou = Euphrasia foulaensis, Emic = Euphrasia micrantha
    - Tables 2 & 4 use population codes from Euphrasia_population_information.csv
    - Each table includes means and standard errors (se)
    - Additional trait details described in Becher et al. (2020)

- Euphrasia_genome_size_data.csv
  - Genome size measurements by flow cytometry
  - Fields include:
    - Population_number, Sample.number, Sample.identity, Location.details, Lat, Long
    - pg2C (2C genome size in picograms), S.D. (standard deviation)
    - hybrid? (hybrid status), ploidy
    - specPop (species-population label), popMeans, popSd, popN
    - spMeans, spSd, spN, pg1C (1C genome size for individuals)

## Data Provenance and References
- Becher H, Powell RF, Brown MR, Metherell C, Pellicer J, Leitch IJ et al (2021). The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights. Annals of Botany.
- Becher H, Brown MR, Powell G, Metherell C, Riddiford NJ, Twyford AD (2020). Maintenance of species differences in closely related tetraploid parasitic Euphrasia on an isolated island. Plant Communications.

## How this Supporting Monitoring Frameworks
- Provides structured, multi-level data (population, trait, and genome size) across spatially explicit sites, suitable for environmental health monitoring of taxonomic variation and adaptive differences.
- Includes standardized metadata (species, population codes, coordinates, ploidy, origin) enabling consistent data integration, comparison, and trend analysis.
- Supports evaluation of how species differences persist under standardized conditions (common garden) and how wild populations vary in morphology and genome size over geography.
- Facilitates reporting through clear data provenance and published references, aiding transparency and reproducibility.

## Data Quality, Metadata, and Governance Considerations
- Metadata present for location, sampling design, and measurement context, aiding verification and reuse.
- Data are split into distinct tables with cross-referenced population codes and species labels, requiring careful data linking across files.
- Potential data-quality considerations include:
  - Consistency of trait units and measurement dates between wild and garden settings.
  - Clear interpretation of population codes and origin fields when aggregating by site or species.
  - Handling of hybrids and ploidy variation in analyses comparing genome size.
- Public sharing of underlying data is supported by the dataset's structure and references, with data provenance enabling traceability to original studies.