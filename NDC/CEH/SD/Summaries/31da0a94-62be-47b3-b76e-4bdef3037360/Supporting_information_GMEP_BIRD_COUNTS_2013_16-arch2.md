# Glastir Monitoring & Evaluation Programme (GMEP)

## Aim and context
- Welsh Government monitoring programme (GMEP) established in 2013 to assess Glastir scheme effects on biodiversity, woodland creation, and management in Wales.
- Data used to track progress toward reversing native biodiversity decline and meeting the Convention on Biological Diversity 2020 obligations.
- Provides an independent estimate of semi-natural habitat change at Broad Habitat level; contributes to the Wales Well-Being Act 2015 indicator for Area of Healthy Ecosystems.

## Survey design and scope
- 4-year rolling survey cycle (first cycle: 2013–2016) to maximise site coverage while detecting year-on-year changes.
- Two components:
  - Wider Wales Component: baseline estimation and national trends/reporting.
  - Targeted Component: focuses on Glastir priority areas.
- Common spatial unit: 1 km squares; 300 squares sampled over the cycle.
- Sampling strategy aligned with the Countryside Survey of Great Britain to enable future data integration.
- Exclusion/replacement: squares with >75% urban land or >90% sea replaced.
- Stratified sampling: half the squares randomly sampled within Land Classification strata; the other half targeted at Glastir priorities.

## Data collection methods (bird surveys)
- Coordinated by the British Trust for Ornithology (BTO).
- Objective: robust estimates of breeding pairs per species per square and habitat associations; finer-scale habitat use than larger-scale schemes.
- Field effort: 60–90 squares per year (not hundreds/thousands as national surveys).
- Visit structure: four visits per square (three from 2015–16 onward), evenly spaced, mid-March to mid-July.
- Survey window: start around 06:00, up to five hours per visit; routes cover within 50 m of all accessible parts of the square.
- Data collection: record all birds seen/heard using standard CBC notation; map territories; log weather conditions; differentiate territorial, flight, nest, and other behaviors.
- Route documentation: exact route mapped; identify areas with poor coverage or no coverage; ensure consistent repeat coverage across visits.

## Data documentation and file structure
- GMEP_BIRD_COUNTS_2013_16.csv: contains bird sightings across 300 1 km squares (Visit, Date, Species, Count, Location, Observer, etc.).
- GMEP_BTO_SPECIES_CODES.csv: lookup table for BTO two-letter species codes with English and Latin names and status.
- Additional fields: anonymised observer codes, 10 km grid coordinates, square IDs, Land Classification codes.

## Quality Assurance (QA) and standards
- Surveys conducted by experienced ornithological teams; rigorous pre-survey training and standardised data recording.
- Field data are collated in the BTO Wales office, then digitised (ArcMap up to v10.5); cross-checks between field observers and digitizers.
- Quality control includes verification of uncertain counts, species codes, and identifications; post-processing checks for unrecognised codes or implausible counts.
- DEFRA Joint Codes of Practice (JCoPR) followed to ensure robustness, repeatability, auditability, and high-quality scientific standards.

## People and collaboration
- UKCEH (UK Centre for Ecology & Hydrology) staff: lead scientist, data management, QA, statistical input, project management, field coordination.
- BTO (British Trust for Ornithology) staff: lead scientist, field survey coordination, spatial data processing.
- Field survey team: list of named surveyors and coordinators supporting data collection.

## Relevance to policy and evidence
- Outputs support monitoring of Glastir impacts and biodiversity indicators.
- Enables integration with broader GB-level surveys due to harmonised sampling and methodology, facilitating future analyses and cross-border comparisons.

## References and publications
- Foundational methodology and sampling framework: Bunce et al. 2007 (ITE Land Classification); O’Connor 1990 (Common Birds Census).
- Key GMEP outputs and field handbooks: Glastir Monitoring & Evaluation Programme Bird Survey Field Handbook (Siriwardena & Taylor, 2014); The Breeding Bird Survey reports; GMEP annual/final reports and website (gmep.wales).
- DEFRA JCoPR standards and related quality-control references.