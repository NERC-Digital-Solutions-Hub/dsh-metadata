# Long-term multisite Scots pine trial, Scotland: field phenotypes, 2013-2020

## Overview
- Seed collection: 10 trees from each of 21 native Scottish P. sylvestris populations (March 2007); germinated at James Hutton Institute, Aberdeen (latitude 57.133214, longitude -2.158764).
- Experimental progression: seeds dormancy break, nursery growth in three nurseries, then transplantation to field sites in 2012.
- Field sites: Yair (FS, southern Scotland), Glensaugh (FE, eastern Scotland), Inverewe (FW, western Scotland).
- Design aims: represent native range and include three populations from each of seven seed zones; randomised blocks, guard rows, and representation of multiple families per site.

## Experimental design and sampling
- Populations and families: 21 populations; 168 trees per field site (one tree from each of eight of the 10 families per population per site, with some replacements when insufficient individuals were available).
- Nurseries and origins: trees raised in three nurseries (NW, NG, NE); field site allocations include cohorts raised locally or at other nurseries.
- Planting layout: randomised blocks (4 blocks at FS and FE; 3 at FW); 3 m x 3 m spacing with guard rows.
- Tree measurements: height measured annually 2013-2020 (FE and FW); 2014-2020 (FS); basal stem diameter measured annually (FE and FW 2013-2020, FS in 2020).
- Phenology: spring assessments 2015-2019; 2020 assessments not possible due to COVID-19.

## Data collected and structure
- File: FieldTraits.txt
- Core variables include:
  - PopulationCode and Description; Family; FieldSite (FE, FS, FW); FieldCode (unique tree code; NA if not transplanted); Block.
  - Growth measures by year:
    - Height (HA13–HA20) in mm (by year 2013–2020, site-specific).
    - Height increments (HI13–HI20) in mm (year-to-year growth).
    - Base stem diameter (DA13–DA20) in mm.
    - Base stem diameter increments (DI13–DI20) in mm.
  - Budburst and phenology:
    - Duration of budburst in various years (BD15–BD20) in days (4 to 6 budburst stages).
    - Time to reach budburst stages BT15_4 to BT19_6 (days since 31 March of respective year) for multiple years.
- Temporal coverage: phenotypic data across multiple growing seasons (2013–2020 for height/diameter; 2015–2019 for phenology; 2020 limited by COVID-19).

## Spatial and temporal scope
- Field sites with approximate location data:
  - FS (Yair): southern Scotland.
  - FE (Glensaugh): eastern Scotland.
  - FW (Inverewe): western Scotland.
- Each site contains cohorts from multiple nurseries/origins and a structured block design; data include coordinates embedded in site descriptions.

## Uses and potential analyses for analysts
- Cross-site and cross-population comparisons of growth trajectories (height, diameter) and their year-to-year increments.
- Genetic or maternal lineage effects: analysis by PopulationCode, Family, and planting origin (nursery) to assess heritability and maternal family performance.
- Genotype-by-environment interactions: site as environment, population/family as genotype.
- Phenology relationships: budburst timing and duration related to growth metrics and site conditions.
- Predictive modelling: growth curves, growth-direction predictions, and phenology-based risk assessment under climate variation.
- Data governance: potential to publish and make datasets discoverable with metadata; track data sources and provenance.

## Limitations and considerations
- COVID-19 impact: 2020 phenology assessments not possible; some measurements for 2020 may be incomplete.
- Replacement of some families at certain sites (e.g., FS) due to insufficient trees, which can affect balanced designs.
- Complex data structure with many derived fields (increment and stage variables) requiring careful handling and consistent year alignment.
- Not all measurements are available at every site for every year (e.g., height data availability varies by FE, FW, FS).