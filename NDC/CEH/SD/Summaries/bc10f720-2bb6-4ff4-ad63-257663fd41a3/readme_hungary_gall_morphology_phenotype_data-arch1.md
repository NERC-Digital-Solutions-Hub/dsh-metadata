# Morphology phenotype data of 88 types of galls induced on oak trees by cynipid gallwasps from 6 sites in Hungary, 2000-2003: Supporting information

- This dataset records quantitative and categorical phenotypic attributes of 88 gall types induced on Quercus spp. by cynipid gallwasps, across 6 sites in Hungary during 2000–2003.
- It includes separate phenotypic scores for sexual and asexual generations, covering 31 sexual generation galls and 58 asexual generation galls, spanning 69 cynipid species.

## Data collection and scope

- Sampling: 10 galls per gall type sampled across sites 1–5 (as referenced in the map) between 2000 and 2003.
- Generations: Data recorded for both sexual and asexual generations where applicable.
- Location: 6 sites in Hungary (map described in the source).

## Data structure and variables

- Data rows: Each row corresponds to a single cynipid species and generation, for the mature gall.
- Number of data columns: 17 variables capturing internal and external gall properties.
- Units: Continuous measurements are in millimetres (mm) or cubic millimetres (mm^3).

- Variables:
  1) Linnean species name: Scientific name of the gallwasp species.
  2) Generation: Asexual or Sexual.
  3) Hair: Binary; 1 = hairy surface, 0 = not hairy.
  4) Dense_spines: Binary; dense coating of fine (<1 mm) spines.
  5) Sparse_spines: Binary; sparse coating of larger (>1 mm) spines.
  6) Sticky: Binary; sticky resin on surface.
  7) Space: Binary; internal air space present.
  8) Dummy: Binary; decoy/dummy inner chamber present.
  9) Peduncle: Binary; connected to host plant by a peduncle.
  10) Nectar: Binary; secreting sugar-rich nectar on surface.
  11) Dehisce: Binary; dehiscing (falling off) at maturity.
  12) Tough: Ordinal (1–4) describing hardness (1 softest to 4 hardest); some missing values.
  13) Shape: Categorical; cone, cylinder, or sphere.
  14) Radius: Continuous; gall radius in mm (base radius if cone).
  15) Height: Continuous; gall height in mm for cones/cylinders (not applicable to spheres).
  16) Gall_Size: Continuous; volume in mm^3 assuming the Shape category.
  17) Locularity: Categorical; Unilocular (single chamber) or Multilocular (multiple chambers).

- Data quality and formatting notes:
  - Some values are missing and denoted by -999 for certain species/generations.
  - Height missing for spherical galls; values may be -999 where data are not applicable.

## Quality control and data validation

- Maturity verification: Gall maturity confirmed by presence of fully mature larval/pupal in larval chambers.
- Identification: Based on diagnostic external gall features by experienced field staff; DNA barcoding (mitochondrial cytochrome b and ITS2) used when needed.
- Validation: Data and identifications undergo error checking; covers both internal and external gall structures.

## Potential analyses and uses

- Comparative morphology: Examine how gall traits vary by species, generation, and site.
- Correlational analyses: Explore relationships among surface traits (Hair, Spines, Sticky), internal structures (Space, Dummy, Peduncle, Nectar), and defensive relevance (Tough, Locularity, Shape, Radius/Height/Gall_Size).
- Predictive modelling: Build models to predict gall hardness, shape, or locularity from other phenotypic features.
- Evolutionary and ecological questions: Assess how sexual vs. asexual generations differ in morphology across species; potential links to defense against natural enemies.

## Related literature

- Bailey, R., Schönrogge, K., Cook, J. M., Melika, G., Csóka, Gy., Thúróczy, Cs., & Stone G. N. (2009). Host niches and defensive extended phenotypes structure parasitoid wasp communities. PLoS Biology, 7(8): e1000179.
- Nicholls, J. A., Challis, R. J., Mutun, S., & Stone, G. N. (2012). Mitochondrial barcodes are diagnostic of shared refugia but not species in hybridising oak gallwasps. Molecular Ecology, 21, 4051-4062.
- Roskam, J. C. (2019). Plant Galls of Europe (KNNV Uitgeverij, Amsterdam), 2201 pp.