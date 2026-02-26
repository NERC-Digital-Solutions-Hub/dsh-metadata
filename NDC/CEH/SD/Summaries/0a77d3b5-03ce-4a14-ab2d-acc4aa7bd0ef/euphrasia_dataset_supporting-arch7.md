# This dataset includes information on native eyebright plants ( Euphrasia , Orobanchaceae) studied and measured at a range of sites across Britain and Ireland, with a special sampling focus on Fair Isle (Shetland, Scotland). There are three data files:

- Euphrasia_population_information.csv
- Euphrasia_trait_data.csv
- Euphrasia_genome_size_data.csv

## Overview
- Aimed at enabling map-based exploration of Euphrasia species across Britain and Ireland, with emphasis on spatial sampling locations, population-level traits, and genome size data.
- Data collected from wild sites and a common garden experiment; includes location, species, ploidy, and sampling context.
- Key references: Becher et al. (2020, 2021) providing context for analyses and species differences.

## Data files and schema

- Euphrasia_population_information.csv
  - Contains two tables:
    - Table 1: sampling information for seeds used in a common garden experiment.
    - Table 2: samples used for genomic sequencing.
  - Key fields:
    - Species, population code (label used in other data files), latitude, longitude (sampling site).
    - Table 2 fields include: label (unique individual identifier), Species, Fair Isle (Yes/No), Ploidy (2x or 4x), Origin (sampling location detail).

- Euphrasia_trait_data.csv
  - Four tables reporting morphological trait measurements.
    - Tables 1 & 2: traits measured in the wild (per species and per population, respectively).
    - Tables 3 & 4: traits measured in a common garden (per species and per population, respectively).
  - Structure:
    - Per species (Tables 1 & 3): columns reflect three species codes (Earc = Euphrasia arctica, Efou = Euphrasia foulaensis, Emic = Euphrasia micrantha).
    - Per population (Tables 2 & 4): columns correspond to populations defined in Euphrasia_population_information.csv.
    - Each table includes mean values and standard errors (se).

- Euphrasia_genome_size_data.csv
  - Genome size measurements via flow cytometry for individual Euphrasia samples.
  - Key fields:
    - Population_number, Sample.number, Sample.identity (species name), Location.details (site and county), Lat, Long.
    - pg2C (2C genome size in picograms), S.D. (standard deviation of pg2C), hybrid? (yes/no), ploidy.
    - specPop (species-population identifier), popMeans/popSd/popN (population-level means, sds, counts), spMeans/spSd/spN (species-level means, sds, counts), pg1C (1C genome size in picograms).

## Geospatial components

- Locations include latitude and longitude for sampling sites; detailed location descriptions (site names, counties) accompany coordinates.
- Special sampling focus on Fair Isle (Shetland, Scotland) noted in population data.
- consolidates spatially-referenced data across populations, enabling mapping of species distributions, population locations, and site-specific trait/genome size attributes.

## Using the data in GIS

- Integrate by:
  - Joining Euphrasia_population_information.csv and Euphrasia_trait_data.csv on population identifiers.
  - Linking Euphrasia_genome_size_data.csv using Population_number or species-population identifiers.
  - Standardizing coordinate reference system (e.g., WGS84) for mapping lat/long values.
- Potential map products:
  - Species distribution maps across Britain and Ireland, with sampling sites highlighted.
  - Population-level trait maps (mean trait values with SE) by location or population.
  - Genome size variation maps at 2C/1C levels, per population and per species.
  - Comparative maps focusing on Fair Isle sampling and its relationship to broader regional patterns.
- Analytical workflows:
  - Visualize mean trait values and genome sizes by population; create choropleth or dot maps.
  - Join trait and genome data to site locations to explore spatial correlations.
  - Compare wild-site measurements with common garden results spatially where appropriate.

## Data quality and considerations

- Data are drawn from multiple sources and resolutions; some data may be incomplete or require reconciliation across tables.
- Hybrid samples are flagged in genome data; interpret cautiously in analyses separating species-level patterns.
- Ensure consistent data standards when merging tables (e.g., matching population codes to population_number and labels).
- Resolution is tied to sampling sites; large-scale spatial analyses should account for potential sampling gaps.

## References

- Becher H, Powell RF, Brown MR, Metherell C, Pellicer J, Leitch IJ et al (2021). The nature of intraspecific and interspecific genome size variation in taxonomically complex eyebrights. Annals of Botany.
- Becher H, Brown MR, Powell G, Metherell C, Riddiford NJ, Twyford AD (2020). Maintenance of species differences in closely related tetraploid parasitic Euphrasia on an isolated island. Plant Communications.