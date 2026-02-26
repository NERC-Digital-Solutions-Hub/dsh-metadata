# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland).

## Overview
- Describes data on native eyebright Euphrasia across Britain and Ireland, with special focus on Fair Isle.
- Comprises three CSV data files that support analyses described in Becher et al. (2020, 2021).
- Data types include sampling information for common garden and genomic sequencing, morphological trait measurements, and genome size estimates via flow cytometry.
- Provides context for combining and re-using data to explore species differences, population variation, and genome size variation.
  
## Data files

- Euphrasia_population_information.csv
  - Contains two tables: Table 1 (sampling information for seeds used in a common garden) and Table 2 (tissue used for genomic sequencing).
  - Key fields:
    - Species, population code (label used in other data files), latitude, longitude (sampling sites).
    - For Table 2: label (unique individual identifier), Species (morphology-based), Fair Isle (sampling site indicator), Ploidy (2x or 4x), Origin (sampling location details).

- Euphrasia_trait_data.csv
  - Contains four tables reporting morphological trait measurements.
  - Layouts:
    - Tables 1 & 3: trait data summarized per species (E arc = Euphrasia arctica, E fou = Euphrasia foulaensis, E mic = Euphrasia micrantha).
    - Tables 2 & 4: trait data summarized per population (labels from Euphrasia_population_information.csv).
  - Data collection contexts:
    - Traits measured in the wild (single sampling date) and in a common garden (Royal Botanic Garden Edinburgh).
    - For each data set: separate columns provide mean values and standard errors (se).
  - Notes: Tables 1 & 3 correspond to species-level summaries; Tables 2 & 4 to population-level summaries; Becher et al. (2020) provide further trait details.

- Euphrasia_genome_size_data.csv
  - Genome size measurements (flow cytometry) for Euphrasia individuals.
  - Key columns:
    - Population_number, Sample.number, Sample.identity, Location.details, Lat, Long.
    - pg2C (2C genome size in picograms), S.D. (standard deviation), hybrid?, ploidy, specPop (species + population label), popMeans, popSd, popN, spMeans, spSd, spN, pg1C (1C genome size for individuals).
  - Methods: genome sizes estimated with flow cytometry using propidium iodide-stained nuclei and internal standard Oryza sativa 'IR36' (Becher et al., 2021).

## Metadata and references
- Species abbreviations in trait data: Earc (Euphrasia arctica), Efou (Euphrasia foulaensis), Emic (Euphrasia micrantha).
- Data provenance: samples sent to Royal Botanic Garden Edinburgh and to other facilities for analysis; alignment with Becher et al. (2020, 2021) for interpretation.
- References:
  - Becher H, Powell RF, Brown MR, Metherell C, Pellicer J, Leitch IJ et al (2021). The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights. Annals of Botany.
  - Becher H, Brown MR, Powell G, Metherell C, Riddiford NJ, Twyford AD (2020). Maintenance of species differences in closely related tetraploid parasitic Euphrasia on an isolated island. Plant Communications.