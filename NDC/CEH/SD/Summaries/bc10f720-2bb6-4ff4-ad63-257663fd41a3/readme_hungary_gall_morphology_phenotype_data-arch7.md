# Morphology phenotype data of 88 types of galls induced on oak trees by cynipid gallwasps from 6 sites in Hungary, 2000-2003: Supporting information

- Scope and purpose
  - Describes a dataset of quantitative and categorical phenotypic attributes for 88 gall types induced on Quercus species by cynipid gallwasps.
  - Galls were collected from 6 sites in Hungary during 2000–2003; phenotypes were scored separately for sexual and asexual generations.
  - Includes 31 sexual generation galls and 58 asexual generation galls across 69 cynipid species, with measurements from roughly 10 galls per gall type.

- Data capture and traits
  - Measurements capture the internal and external structure of mature galls.
  - Phenotypic properties are categorized as binary, ordinal, or continuous (mm or mm^3).
  - Continuous measurements obtained with digital calipers; some values may be missing or marked as -999.
  - Units: all continuous variables in millimeters (radius, height) or cubic millimeters (Gall_Size).

- Data structure (17 variables)
  1. Linnean species name
  2. Generation (Asexual or Sexual)
  3. Hair: binary (1 = hairy, 0 = not)
  4. Dense_spines: binary (dense fine spines)
  5. Sparse_spines: binary (sparse larger spines)
  6. Sticky: binary (resin-coated)
  7. Space: binary (internal air space)
  8. Dummy: binary (decoy/dummy chamber)
  9. Peduncle: binary (connected by a stalk)
  10. Nectar: binary (nectar secretion)
  11. Dehisce: binary (dehiscing at maturity)
  12. Tough: ordinal (1 softest to 4 hardest)
  13. Shape: categorical (cone, cylinder, sphere)
  14. Radius: continuous (mm)
  15. Height: continuous (mm; for cones/cylinders; not provided for spheres)
  16. Gall_Size: continuous (mm^3, volume assuming Shape)
  17. Locularity: categorical (Unilocular or Multilocular)

- Data quality and validation
  - Gall maturity confirmed by presence of fully mature larval/pupal in chambers.
  - Field identifications based on external diagnostic features; validated with DNA barcoding when needed (mitochondrial cytochrome b and nuclear ITS2) per Nicholls et al. 2012.
  - Data have been carefully checked for errors; missing values denoted by -999 for some records.

- Spatial and temporal context
  - Six sites across Hungary; location map referenced in the document.
  - Sampling conducted 2000–2003; continuous measurements taken from samples across sites 1–5; site-level distinctions available via the map and site identifiers, though explicit coordinates are not listed in the 17-variable schema.

- Practical GIS-centric implications
  - Compatible as a tabular dataset for GIS—enabling thematic mapping of gall traits by site and generation.
  - Enables spatial comparisons of phenotype distributions (binary/ordinal/continuous traits) across geographical locations.
  - Potential to integrate with host tree data (Quercus spp.) and DNA barcode results for expanded biogeographic and phylogenetic analyses.
  - Useful for quality control and data provenance in spatial analyses, given explicit validation steps and error-checking procedures.

- References
  - Bailey, R. et al. (2009). Host niches and defensive extended phenotypes structure parasitoid wasp communities. PLoS Biology.
  - Nicholls, J. A. et al. (2012). Mitochondrial barcodes are diagnostic of shared refugia but not species in hybridising oak gallwasps. Molecular Ecology.
  - Roskam, J. C. (2019). Plant Galls of Europe.