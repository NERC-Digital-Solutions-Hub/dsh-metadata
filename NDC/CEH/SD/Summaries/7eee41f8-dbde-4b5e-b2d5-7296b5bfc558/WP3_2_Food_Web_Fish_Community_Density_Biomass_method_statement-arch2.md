# Fish biomass and density data

- Objective and outputs
  - Estimate density of fish taxa at each of three streams using benthic sampling and multi-pass electrofishing.
  - Derive biomass per m2 for each taxon by applying mean biomass (from length-mass regressions) to density estimates; provide biomass per m2 per site per occasion.
  - Data intended to inform quantified food webs and standing stocks and support environmental health assessments over time.

- Where data were collected
  - Sites: Three chalkstreams in the Wessex chalk area — Nine Mile River, River Till, and River Wylye.
  - Site characteristics: Streams varied in catchment land-use intensity, reflecting a landscape integrity gradient.

- When data were collected
  - Five sampling occasions between October 2012 and October 2013.
  - Sampling avoided the salmonid breeding season (December–March) to minimize disturbance to redds.

- How data were collected
  - Methods:
    - Multi-pass electrofishing for population density estimates using the Zippin maximum likelihood method.
    - Modified Hess sampler (0.12 m2) to sample benthic species poorly captured by electrofishing (e.g., bullheads, stone loach), 20 deployments per date in a stratified-random design.
  - Sampling protocol:
    - Benthic fish sampling conducted along a 100 m reach with 20 locations; substrate disturbed for 30 seconds per location; captured fish identified to species and measured.
    - Electrofishing conducted along the same 100 m reach with stop nets; fish counted, measured, and weighed; depletion criteria applied (fewer than 50 individuals in first run or fewer than 100 total may trigger sampling of an upstream 100 m reach).
  - Data processing:
    - Biomass for each taxon per site per occasion calculated by multiplying density estimates by length-mass derived biomass.
    - All measurements aligned to standardized survey geometry and timing.

- Data structure and fields
  - Key columns include:
    - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
    - OS_NGR, OS_EASTING, OS_NORTHING
    - SURVEY_DATE, REACH
    - TAXON_NAME
    - Biomass_mgperm2, Density_Noperm2
    - 2SD (standard deviation around density; may be absent if data are insufficient)

- Data provenance and responsibility
  - Data collection, processing, and initial interpretation conducted by Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.
  - Quality assurance:
    - Strict adherence to established benthic fish sampling and electrofishing protocols.
    - No formal within-period repeat-survey QA; electrofishing performed by experienced biologists (Bill Bellamy and Luke Scott) from the Game and Wildlife Conservation Trust.

- Completeness and limitations
  - Complete five-sample occasions across three sites.
  - No sampling during Dec–Mar breeding season.
  - Limitations noted: absence of formal QA via repeat sampling within the same period; SD values may be missing when data are sparse.

- References
  - Zippin C. 1958. The removal method of population estimation. Journal of Wildlife Management 22:82-90.

- Relevance to monitoring aims
  - Uses standardised methods and outputs suitable for time-series comparisons and policy performance assessments.
  - Facilitates data sharing and integration with other environmental datasets to increase the value of monitoring data.