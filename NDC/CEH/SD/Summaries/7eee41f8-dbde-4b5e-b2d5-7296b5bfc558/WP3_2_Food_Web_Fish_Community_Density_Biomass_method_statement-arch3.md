# Fish biomass and density data

## Overview
- Records density and biomass of fish taxa across three chalk streams in the Wessex chalk area.
- Purpose: inform quantified food webs and standing stocks for environmental monitoring and policy assessment.
- Temporal coverage: five sampling occasions between October 2012 and October 2013.
- Sites: Nine Mile River, River Till, and River Wylye, chosen to reflect a gradient in landscape integrity.

## Data collected and methods
- Population density estimation via multi-pass electrofishing; density estimates derived using the Zippin maximum likelihood method.
- For benthic species less catchable by electrofishing (e.g., bullheads, stone loach), a modified Hess sampler (0.12 m2) used, deployed 20 times per date in a stratified-random regime.
- Biomass estimation: mean biomass per taxon per site per occasion calculated from length–mass regressions and multiplied by density estimates to yield biomass per m2.
- Field procedure: 100 m survey reach with benthic sampling at 20 locations; electrofishing conducted within reach with stop nets and depletion sampling.
- If initial runs yielded too few fish ( fewer than 50 in first run or fewer than 100 total), an upstream 100 m reach was sampled with the same depletion approach.
- Taxa identified to species; individuals measured and weighed.

## Study sites and timing
- Three chalkstreams selected to represent a gradient of landscape integrity and biodiversity.
- Sampling avoided the salmonid breeding season (December–March) to prevent disturbance to redds.

## Data processing and outputs
- Data generated: Biomass_mgperm2 and Density_Noperm2 per taxon per site per occasion; 2SD values provided where calculations were possible.
- Primary use: construction of quantified food webs detailing fluxes of mass and nutrients between nodes; assessment of standing stocks of fish.

## Data structure and provenance
- Managed by: Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.
- Data table structure (columns):
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, OS_NGR, OS_EASTING, OS_NORTHING, SURVEY_DATE, REACH, TAXON_NAME, Biomass_mgperm2, Density_Noperm2, 2SD.

## Quality, governance, and limitations
- Adherence to established benthic fish sampling and electrofishing protocols.
- No formal quality assurance procedure documented (e.g., repeat surveys of the same reach within the period).
- Sampling conducted by fully qualified, experienced fish biologists from recognized institutions.
- Metadata and method details are documented to support data reuse, including precise location identifiers and measurement units.

## Implications for monitoring frameworks
- Demonstrates integration of field survey methods, density/biomass estimation, and data for network-based ecological analyses (food webs).
- Highlights the importance of metadata completeness (locations, dates, taxon names, measurements) for data usability in monitoring programs.
- Illustrates potential data limitations relevant to monitoring planning, such as gaps during breeding seasons and QA considerations.