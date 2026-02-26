# Susceptibility of Scots pine ( Pinus sylvestris ) to Dothistroma septosporum following natural inoculation at Torrs Warren, Galloway 2013-2015

## Overview
- A common garden trial of Scots pine transplanted from CEH Edinburgh (April 2013) to Torrs Warren forest, Galloway, to study susceptibility to Dothistroma septosporum.
- Measurements collected 2013–2015 include infection levels, tree growth, branching, chlorophyll fluorescence, and defoliation; detailed needle-level pathogen assessments were performed.
- Data are organized into multiple CSV files with raw and mean phenotype data, plus extensive metadata about populations, families, blocks, and site characteristics.
- Purpose includes supporting doctoral research and the PROTREE project, with broader relevance for forest health monitoring and policy-informed decision making.

## Dataset contents and structure
- Detailed_assessment_Sep_2013.csv
  - Needle-level data for infected trees: length of lesions (LNL), number of lesions per needle (LPN), lesion length (LL); up to 11 needles per tree sampled on 17/09/2013.
  - Block, position, needle identifiers; descriptive units and dates.
- Detailed_assessment_Oct_2014.csv
  - Needle-level data from Oct 2014: total needles examined per tree; per-needle metrics including lesion length (LL), length of needles with lesions (LNL), lesions per needle (LPN), and visible fruiting bodies on lesions (FBV) for up to 5 needles per tree (07/10/2014).
  - Additional metadata for each observation (block, position, date).
- Mean_phenotype_per_tree.csv
  - Per-tree raw data and mean values across assessments for: infection assessments (various seasons), height measurements, chlorophyll fluorescence (Fv/Fm), branching counts, defoliation, and detailed needle-derived metrics (from Sept 2013 and Oct 2014).
  - Tree-level metadata: population, family, block, position, original number, fungicide treatment in 2015, geographic coordinates (lat/long), altitude, and historical height data (2010–2015).

## Experimental design and site
- Origin: Eight Scottish Scots pine populations (Ballochbuie, Blackwood of Rannoch, Beinn Eighe, Coille Coire Chuilc, Glen Affric, Glen Loy, Glen Tanar, Rothiemurcus) with four families per population (six individuals per family; total 192 trees).
- Transplant and site: Planted in Torrs Warren adjacent to stands infected with Dothistroma needle blight; transplanted in 2013 as six-year-old saplings from six-litre pots, spaced at 0.5 m.
- Trial layout: Six randomized blocks; guard row around the edge to mitigate edge effects; annual weeding to manage brambles/bracken.
- Timing: Assessments every six months (autumn and spring) from 2013–2015; chlorophyll fluorescence measured July 2013; detailed needle assessments Sept 2013 and Oct 2014.

## Assessments and measurements
- Infection: Estimated percentage of current-year needles that are green/healthy, expressed in 5% increments; infection scores used to indicate disease presence, with 1% indicating negligible infection (<5% category threshold).
- Growth and morphology: Annual tree height at end of growing season or before new season (autumn or early spring); branching architecture recorded (March 2015).
- Physiological stress: Chlorophyll fluorescence (Fv/Fm) measured in July 2013 to identify stressed trees (values < 0.8 flagged).
- Defoliation: Estimated percentage defoliation of previous-year needles recorded October 2014.
- Needle-level pathology: In September 2013 and October 2014, leaves for infection assessment collected; detailed measurements of lesions, needle length, and, in 2014, presence of visible fruiting bodies on lesions.
- Data quality controls: Infection assessments performed by a single observer (Annika Perry); Cultures of Dothistroma septosporum isolated from needles in Sept 2013 to confirm presence of the pathogen.

## Data quality, provenance, and data handling
- Data quality and provenance:
  - Consistent infection assessments by one analyst; pathogen confirmation through culture.
  - Some data gaps due to trees dying or being removed (dead/missing list with tree identifiers and dates).
  - Some fields contain NA values where data were not available due to mortality or removal.
- Dead/missing trees:
  - Documented for several blocks/trees with dates indicating death or removal (e.g., trees 1, 2, 3, 5, 6 across various positions).
- Data transformations:
  - Infection data sometimes transformed to LOG for analysis (as noted in the detailed variable descriptions).

## Site, origin, and contextual metadata
- Tree origin and history:
  - Seeds collected in the field and germinated spring 2007; transplanted 2013 (six years old at transplant).
  - Population-level diversity across eight Scottish populations, with 192 trees in total.
- Site specifics:
  - Torrs Warren trial site, adjacent to Corsican and lodgepole stands infected with Dothistroma; raised in pots before transplant; 0.5 m spacing; surrounding guard rows; annual weeding.
- Geospatial context:
  - GPS coordinates provided for selected corner trees (lat/long) and related block/position-family identifiers.

## Governance, data sharing, and usage
- Data provenance and documentation:
  - Data collected for research contributions (Annika Perry’s PhD; PROTREE project) and shared to support policy-relevant environmental health monitoring.
- Data sharing considerations:
  - Acknowledges barriers to publicly sharing underlying datasets in some contexts; the dataset includes comprehensive metadata and detailed documentation to facilitate reuse and transparency.
- Related datasets and usage:
  - Earlier in situ chlorophyll fluorescence and needle morphology data from CEH Edinburgh share the same trial design; copper fungicide treatment applied in July 2015 as part of PROTREE for endophyte studies in some blocks.

## Relevance for monitoring frameworks and policy decision-making
- Key health indicators:
  - Dothistroma infection prevalence (seasonal), growth (height), tree architecture (branching), physiological stress (Fv/Fm), and defoliation.
- Scalable data design:
  - Combines plot-level infection trends with needle-level pathology, enabling cross-scale monitoring and risk assessment.
- Policy and management implications:
  - Data support assessment of genetic resistance across populations, inform monitoring cadence and data governance for forest health programs, and guide disease mitigation strategies (e.g., timely data sharing and transparent metadata practices).

## Limitations and caveats
- Mortality and removals reduced sample size over time; some blocks contain missing data.
- Fungicide treatment in 2015 for endophyte studies may influence later measurements in impacted blocks.
- Some data fields rely on transformations (e.g., log) for analysis, which affects interpretation without appropriate statistical handling.

## Appendix: Key data and identifiers
- Populations: Ballochbuie, Blackwood of Rannoch, Beinn Eighe, Coille Coire Chuilc, Glen Affric, Glen Loy, Glen Tanar, Rothiemurcus.
- Blocks: Six randomized blocks (1–6) with block-level descriptions matching the cottage garden design.
- Pos (within-block): 1–32 positions; trees identified by a combination of block, position, and family.
- Original tree identifiers: orig no; used for cross-referencing with earlier measurements and provenance.