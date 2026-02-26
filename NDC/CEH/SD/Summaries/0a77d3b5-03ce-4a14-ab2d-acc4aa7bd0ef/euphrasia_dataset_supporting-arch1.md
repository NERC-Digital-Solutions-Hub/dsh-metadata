# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland).

## Overview
- Native eyebright plants across Britain and Ireland, with emphasis on Fair Isle.
- Data cover population sampling, morphological trait measurements, and genome size, linked to both wild and common garden contexts.
- Associated with analyses in Becher et al. (2020) and Becher et al. (2021).

## Data files included
- Euphrasia_population_information.csv
  - Two tables:
    - Table 1: Sampling information for seeds used in a common garden experiment to test species differences under standardised conditions (species, population code, and sampling site coordinates).
    - Table 2: Samples used for genomic sequencing (label/ID, Species, Fair Isle indicator, Ploidy, Origin).
- Euphrasia_trait_data.csv
  - Four tables reporting morphological trait measurements:
    - Tables 1 & 2: traits measured in the wild.
    - Tables 3 & 4: traits measured with seeds grown in a common garden at the Royal Botanic Garden Edinburgh.
  - Data are presented per species (Tables 1 & 3) and per population (Tables 2 & 4); includes means and standard errors.
  - Species abbreviations: Earc = Euphrasia arctica; Efou = Euphrasia foulaensis; Emic = Euphrasia micrantha.
  - Field measurements taken on a defined sampling date; common garden measurements taken at first flowering and at the end of flowering.
  - Population data linked to Euphrasia_population_information.csv; additional methodological details provided in Becher et al. (2020).
- Euphrasia_genome_size_data.csv
  - Genome size measurements by flow cytometry for wild-collected tissues.
  - Processed at Royal Botanic Garden Kew; internal standard: Oryza sativa 'IR36'.
  - Columns and key fields:
    - Population_number: unique population ID
    - Sample.number: collector number (if provided)
    - Sample.identity: Euphrasia species name
    - Location.details: site name and county
    - Lat / Long: coordinates of collection
    - pg2C: 2C genome size estimate (pg)
    - S.D.: standard deviation of pg2C
    - hybrid?: whether the sample is a hybrid
    - ploidy: ploidy level
    - specPop: concatenated species and population for analysis
    - popMeans / popSd / popN: population-level mean, standard deviation, and count
    - spMeans / spSd / spN: species-level mean, standard deviation, and count
    - pg1C: individual 1C genome size (pg)
- References
  - Becher H, Powell RF, Brown MR, Metherell C, Pellicer J, Leitch IJ et al (2021). The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights. Annals of Botany.
  - Becher H, Brown MR, Powell G, Metherell C, Riddiford NJ, Twyford AD (2020). Maintenance of species differences in closely related tetraploid parasitic Euphrasia (Orobanchaceae) on an isolated island. Plant Communications.