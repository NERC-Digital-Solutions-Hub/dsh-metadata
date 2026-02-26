# The provenance trial environment

- Overview
  - Established by France’s National Institute for Agricultural Research (INRA) as the La Petite Charnie provenance trial.
  - Includes almost 200,000 trees representing 103 Quercus petraea provenances and 9 Quercus robur provenances.
  - Located in a temperate, Atlantic, wet climate with red sandstone, schist, and clay substrata; surrounded by mature oak forest and mixed hardwoods.
  - Local native populations not represented in the trial; closest comparable population is ~50 km away (Forêt de Bercé).

- Experimental design and scope
  - Within each soil zone, each provenance is represented by two or three plots, each plot comprising 24 trees planted in a 4 by 6 grid.
  - Spacing: 1.75 m within rows and 3 m between columns.
  - Blocks aggregate 8 plots from different provenances; position of blocks randomized within soil zones to enable separation of plot, block, soil-zone, and provenance effects.
  - For this subset, block effects were not considered; plot positions within soil zones treated as random.
  - Each sampled provenance planted in multiple replicate plots across five soil zones; selected 2 plots per soil zone per provenance, totaling 200 study plots and 4,800 trees.

- Herbivore survey (cynipid gall survey)
  - Surveyed across 20 selected provenances in 2008 and 2009, covering broad Western Palaearctic distributions.
  - Four sampling events per year: spring (sexual) and autumn (asexual) generations, each year.
  - In each of 200 plots, galls were sampled from 12 of the 24 available trees (total 2,400 trees).
  - To minimize edge effects, sampled trees were the two internal rows of six trees per plot.
  - For each survey, 10 twigs per tree were sampled, each twig representing the last two years’ growth.
  - Galls identified to species and generation in the field using a morphological key and extensive field experience.

- Nature and units of recorded values
  - Data type: Counts
  - Gall counts captured for multiple gall species/generations (see data fields below).

- Data structure and fields
  - Identifier and provenance codes: ProvCode, ParcelleID
  - Spatial and experimental design: SoilZone, Soile Zone (1–5), Plot-level design identifiers
  - Temporal and sampling: YearGen (generation and year; S = spring, A = autumn; 08 = 2008, 09 = 2009)
  - Tree and shoot identifiers: TreeNo, ShootNo, Shoot ID
  - Gall count fields by species and generation:
    - AfecAsex (Andricus foecundatrix, asexual)
    - AglanAsex (Andricus glandulae, asexual)
    - AsolAsex (Andricus solitarius, asexual)
    - NalbAsex (Neuroterus albipes, asexual)
    - NantAsex (Neuroterus anthracinus, asexual)
    - NqbAsex (Neuroterus quercusbaccarum, asexual)
    - NnAsex (Neuroterus numismalis, asexual)
    - CdivAsex (Cynips divisa, asexual)
    - CqfAsex (Cynips quercusfolii, asexual)
    - AtestSex (Andricus testaceipes, sexual)
    - NalbSex (Neuroterus albipes, sexual)
    - NantSex (Neuroterus anthracinus, sexual)
    - NnSex (Neuroterus numismalis, sexual)
    - NqbSex (Neuroterus quercusbaccarum, sexual)

- Quality control
  - One-to-one training of data collectors
  - Double-checking for outliers during data transcription

- Data governance and sharing considerations (implications for Data Stewards)
  - Metadata completeness: ensure clear definitions for each field (e.g., YearGen coding, plot identifiers, twig sampling scheme).
  - Data dictionary alignment: confirm compatibility with field codes and units across related datasets; note linkage to File S1 for additional design details.
  - Provenance and context: maintain documentation on experimental design, randomization, and replication to enable correct analysis and reproducibility.
  - Data quality and consistency: monitor for missing values, outliers beyond transcription checks, and consistency of species/genera identifications.
  - Sharing and access: prepare for deposition into data portals; document any embargoes or restrictions, and clearly state units (counts) and scope (gall species/generations).
  - Interoperability challenges: the study spans multiple species, generations, and plots; ensure data can be integrated with other environmental and phenotypic datasets.
  - Maintenance and updates: track any updates or corrections to field definitions, plot assignments, or taxonomic keys; plan for long-term accessibility of supplementary materials (e.g., File S1).

- Notes and references
  - Related methodological and geographic context referenced as Bacilieri & Krémer (1995)
  - File S1 contains additional trial design details referenced in the study context