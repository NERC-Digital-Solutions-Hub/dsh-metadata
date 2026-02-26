# Fish biomass and density data

## Overview
- Density of fish taxa at three chalkstreams was estimated using benthic sampling and multi-pass electrofishing.
- The mean biomass of individuals per taxon at each site and occasion was used, with density estimates, to derive biomass per m2 for each taxon.

## Data collection methods
- Benthic fish sampling: modified Hess sampler (0.12 m2) deployed 20 times per 100 m reach; substrate sealed and agitated for 30 seconds to dislodge fish; specimens identified to species and measured.
- Electrofishing: 100 m survey reach enclosed with stop nets; multiple depletion runs; fish counted, measured, and weighed; Zippin maximum likelihood method used to estimate density.
- For species poorly caught by electrofishing (e.g., bullheads, stone loach), a modified Hess sampler was used (20 deployments per date).
- If depletion criteria were not met ( fewer than 50 individuals in first run or fewer than 100 total in all runs), a second 100 m reach upstream was surveyed with the same depletion procedure.

## Study sites and timing
- Sites: Nine Mile River, River Till, River Wylye (three chalkstream sites reflecting a gradient of landscape integrity).
- Sampling occasions: five between October 2012 and October 2013.
- Sampling avoided the salmonid breeding season (December–March) to prevent disturbance of redds.

## Data processing and biomass estimation
- Biomass per taxon per site per occasion derived by applying length–mass regressions to measured individuals and multiplying by the density estimate.
- Result: biomass per m2 for each taxon and site on each occasion.

## Data structure
- Key fields include: RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, OS_NGR, OS_EASTING, OS_NORTHING, SURVEY_DATE, REACH, TAXON_NAME, Biomass_mgperm2, Density_Noperm2, 2SD (where present).

## Data governance and authorship
- Data collected, processed, analyzed, interpreted, and managed by the Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.

## Completeness and quality assurance
- Five sampling occasions across three sites; no sampling during Dec–Mar.
- No formal quality assurance procedure (e.g., repeat survey within the same period); protocols followed.
- Electrofishing conducted by experienced biologists (Bill Bellamy and Luke Scott) using standard procedures.

## Limitations and caveats
- Electrofishing may under-sample certain benthic species, affecting density estimates.
- Absence of 2SD for some taxa indicates insufficient data to estimate variability.
- Lack of formal QA and potential sampling gaps may affect data reliability for some taxa or dates.

## References
- Zippin C. 1958. The removal method of population estimation. Journal of Wildlife Management 22:82-90.