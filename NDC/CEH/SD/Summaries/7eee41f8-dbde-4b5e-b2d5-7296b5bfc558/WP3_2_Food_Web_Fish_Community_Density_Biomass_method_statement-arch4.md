# Fish biomass and density data

## Overview
- A study estimating fish taxa density and biomass across three chalk streams in the Wessex chalk area (Nine Mile River, River Till, River Wylye).
- Data collected to support quantified food webs and standing stocks, reflecting landscape integrity gradients.
- Timeframe: five sampling occasions between October 2012 and October 2013.
- Managed by the Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.

## Data collected and scope
- Data types:
  - Density estimates (per m2) for each taxon at each site and occasion.
  - Biomass per taxon per site and occasion, derived by applying mean biomass per taxon to density estimates.
  - 2SD values around estimated densities where available.
- Sites and sampling scope:
  - Three streams with varying land-use intensity; three sites within a 100 m reach per site.
  - Five occasions; sampling avoided the salmonid breeding season (Dec–Mar).

## Methods
- Field methods:
  - Multi-pass electrofishing for fish populations.
  - Zippin maximum likelihood depletion method used to estimate population density.
  - For benthic species poorly captured by electrofishing (e.g., bullheads, stone loach), a modified Hess sampler (0.12 m2) used, with 20 deployments per date in a stratified-random design.
- Biomass estimation:
  - Species-specific mean biomass calculated from length-mass regressions.
  - Biomass per m2 derived by multiplying mean biomass by density estimate.
- Sampling procedure:
  - 100 m survey reach used for benthic sampling and electrofishing; stop nets deployed during electrofishing.
  - If depletion suggested insufficient fish (fewer than 50 in first run or fewer than 100 overall), a second 100 m reach upstream was sampled with similar depletion runs.

## Data structure and metadata
- Data columns (example):
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, OS_NGR, OS_EASTING, OS_NORTHING, SURVEY_DATE, REACH, TAXON_NAME, Biomass_mgperm2, Density_Noperm2, 2SD.
- Purpose of metadata:
  - Enables mapping, cross-site comparisons, and integration with broader datasets or systems.
- Data management:
  - Responsibility for collection, processing, interpretation, and management assigned to QMUL River Communities Group.

## Data completeness and quality
- Completeness:
  - Samples collected on five separate occasions across the three sites.
  - Excluded December–March to avoid disturbing salmonid redds.
- Quality assurance:
  - Adherence to established protocols for benthic sampling and electrofishing.
  - No formal QA procedure reported (e.g., no repeat surveys within the same period); electrofishing conducted by highly qualified, experienced biologists.

## Data use and integration
- Purpose supports construction of quantified food webs and assessment of standing fish stocks.
- Data are structured to enable integration with other variables (e.g., habitat data, invertebrates) for broader ecosystem analyses and cross-site collaboration.

## References
- Zippin C. 1958. The removal method of population estimation. Journal of Wildlife Management 22:82-90.