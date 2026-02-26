# The provenance trial environment

- Overview
  - The La Petite Charnie provenance trial was established by INRA to study tree provenance effects across Quercus petraea and Quercus robur.
  - Includes about 200,000 trees representing 103 Q. petraea provenances and 9 Q. robur provenances from a broad native range.
  - Local context: Atlantic, temperate, wet climate; red sandstone, schist, and clay substrata; surrounding mixed oak and beech/ash/hornbeam forest.
  - Native populations of trees at La Petite Charnie are not represented; closest native population is Forêt de Bercé (~50 km away).

- Experimental design and layout
  - Within each soil zone, provenances are represented by two or three plots, each containing 24 trees planted in four columns by six trees.
  - Spacing: 1.75 m within columns; 3 m between columns.
  - Blocks with 8 plots representing different provenances are randomized within soil zones to enable separation of plot, block, soil zone, and provenance effects.
  - For this subset, block effects were not considered; plot positions within soil zones were treated as random.
  - Sampling plan: 2 plots per soil zone per provenance, yielding 200 study plots and 4,800 trees in total.
  - Edge effect mitigation during herbivore surveys: only the two internal rows of six trees per plot were surveyed.

- Herbivore survey (gallwasps)
  - Target organisms: cynipid gallwasps with broad Western Palaearctic distributions.
  - Survey period: across 20 selected provenances in 2008 and 2009.
  - Generations surveyed: spring (sexual) and autumn (asexual) each year, totaling four surveys per plot.
  - Sampling per plot: galls were counted on 12 of 24 trees (for a total of 2,400 trees across all plots).
  - Tree selection per survey: 10 twigs per tree, each twig representing the last two years’ growth; all galls on all parts of the corresponding shoot were counted.
  - Field identification: galls identified to species and generation in the field.

- Nature and units of recorded values
  - Counts (gall counts by species and generation).

- Data structure and metadata
  - Key identifiers and fields:
    - ID, Record ID
    - ProvCode (provenance code)
    - SoilZone (1–5)
    - ParcelleID (plot identifier within soil zone)
    - YearGen (generation: S = spring; A = autumn; year: 08 = 2008; 09 = 2009)
    - TreeNo (tree identifier)
    - ShootNo / Shoot ID (the 10 shoots surveyed per tree)
    - Gall count fields by species and generation, including:
      - AfecAsex, AglanAsex, AsolAsex, NalbAsex, NantAsex, NqbAsex, NnAsex, CdivAsex, CqfAsex
      - AtestSex, NalbSex, NantSex, NnSex, NqbSex, NqbSex
  - Species and generation coverage includes Andricus foecundatrix, Andricus glandulae, Andricus solitarius, Neuroterus albipes, Neuroterus anthracinus, Neuroterus quercusbaccarum, Neuroterus numismalis, Cynips divisa, and Cynips quercusfolii (each with both sexual and asexual counts where applicable).

- Quality control and data management
  - One-to-one training of data collectors to ensure consistency.
  - Double checking for outliers during transcription and data entry.

- Relevance for data support and potential analyses
  - Rich, replicated design enabling assessment of provenance, soil-zone, plot, and year/generation effects on gallwasp abundance.
  - Structured data model facilitates self-contained data products (e.g., summarized gall counts by provenance and soil zone) and supports cross-year comparisons.
  - Clear metadata and field definitions aid data integration with other plant-behavior or herbivore datasets.
  - Limitations noted: block effects not considered for this subset; edge effects addressed by surveying internal rows only.