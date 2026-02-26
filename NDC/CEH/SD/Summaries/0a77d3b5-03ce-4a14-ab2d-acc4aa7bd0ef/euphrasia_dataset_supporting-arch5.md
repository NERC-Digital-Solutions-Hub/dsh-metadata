# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland). There are three data files:

- Euphrasia_population_information.csv
  - Contains two tables reporting sampling information for seeds used in a common garden (Table 1) and plant tissue used for genomic sequencing (Table 2).
  - Table 1: includes Euphrasia species, population code (label used in other data files), and latitude/longitude of sampling site.
  - Table 2: includes label (unique individual identifier), Species (morphology-based), Fair Isle (whether collected there), Ploidy (2x or 4x), Origin (sampling location details).

- Euphrasia_trait_data.csv
  - Contains four tables reporting morphological trait measurements of Euphrasia plants.
  - Measured in the wild (Tables 1 & 2) and in a common garden at the Royal Botanic Garden Edinburgh (Tables 3 & 4).
  - Data are presented per species (Tables 1 & 3) and per population (Tables 2 & 4); separate columns provide mean values and standard errors (se).
  - Species abbreviations: Earc = Euphrasia arctica, Efou = Euphrasia foulaensis, Emic = Euphrasia micrantha.
  - Separate trait data for field sampling date and for flowering-stage dates; additional details are provided in Becher et al. (2020).

- Euphrasia_genome_size_data.csv
  - Reports genome size measurements by flow cytometry for Euphrasia individuals.
  - Measurements were made on wild tissue samples submitted to RBG Kew; genome sizes estimated with PI-stained nuclei using Oryza sativa 'IR36' as an internal standard (Becher et al. 2021).
  - Key columns include:
    - Population_number (unique population identifier)
    - Sample.number (collector number, if supplied)
    - Sample.identity (Euphrasia species name)
    - Location.details (site name and county)
    - Lat / Long (sampling coordinates)
    - pg2C (2C genome size in picograms)
    - S.D. (standard deviation of pg2C)
    - hybrid? (whether sample is a hybrid)
    - ploidy (ploidy level)
    - specPop (species-population concatenation used in analyses)
    - popMeans / popSd / popN (population-level mean, sd, and N for genome size)
    - spMeans / spSd / spN (species-level mean, sd, and N)
    - pg1C (individual 1C genome size in picograms)

- References
  - Becher H, Powell RF, Brown MR, Metherell C, Pellicer J, Leitch IJ et al (2021). The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights. Annals of Botany 128(5): 639-651.
  - Becher H, Brown MR, Powell G, Metherell C, Riddiford NJ, Twyford AD (2020). Maintenance of species differences in closely related tetraploid parasitic Euphrasia (Orobanchaceae) on an isolated island. Plant Communications 1(6): 100105.

## Data structure and provenance

- The dataset combines population-level sampling, trait measurements, and genome size data to enable analyses of species differences, population variation, and genome size variation in Euphrasia across Britain and Ireland, with emphasis on Fair Isle.
- It links via population identifiers, species labels, and population-level metadata to support integrative analyses and replication of findings (Becher et al. 2020, 2021).

## Key governance and stewardship considerations

- Metadata consistency
  - Map species abbreviations (Earc, Efou, Emic) to full species names in metadata and downstream datasets.
  - Ensure population codes and labels used in Euphrasia_population_information.csv align with those in Euphrasia_trait_data.csv and Euphrasia_genome_size_data.csv.
- Data quality and provenance
  - Validate geographic coordinates (Lat/Long) and site details against sampling records.
  - Confirm measurement units across files (pg2C and pg1C for genome sizes; mean and se for trait data).
  - Document sequencing and sampling methods, including flow cytometry protocol and internal standards (as referenced).
- Interoperability and reuse
  - Provide a data dictionary or readme that describes each field, units, and any derivations.
  - Include crosswalks to primary publications (Becher et al. 2020, 2021) for methodological context and validation.
- Data preservation and updates
  - Establish versioning and release notes if updates occur (e.g., corrected coordinates, additional samples, or updated trait values).
  - Maintain links to theBecher et al. studies to preserve scientific context for the data.

## How this dataset supports the Data Stewards aim

- Provides a multi-file, well-documented dataset with clear population and specimen identifiers, enabling standardized data governance and discoverability.
- Includes diverse data types (sampling metadata, morphological traits, and genome size measurements) that require consistent metadata and careful cross-referencing across tables.
- Facilitates reuse by data producers and users who need to understand provenance (sampling sites, timing, and methods) and by downstream analyses that compare species and population-level genome size variation.
- Aligns with published studies, allowing researchers to reproduce analyses or extend them with additional data, while maintaining explicit references to Becher et al. works for methodological grounding.