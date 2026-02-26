# Fish biomass and density data

- Purpose: Record density and biomass of fish taxa across three chalkstream sites to support quantified food webs and standing stock assessments.

- What is recorded:
  - Taxon-level biomass per square metre (Biomass_mgperm2) and density per square metre (Density_Noperm2) for each taxon at each site and sampling occasion.
  - 2 standard deviations around density estimates (2SD) when available.

- Study area and locations:
  - Three chalkstreams in the Wessex chalk area: Nine Mile River, River Till, and River Wylye.
  - Each site captured within a 100 m survey reach (REACH).

- Data collection methods:
  - Benthos sampling:
    - Modified Hess sampler (0.12 m2) used at 20 locations per date, deployed in a downstream direction with 30-second substrate agitation to dislodge benthic fish.
    - Fish identified to species, measured (tip of head to fork in tail).
  - Electrofishing:
    - 100 m reach enclosed with stop nets and electrofished for all species/sizes to depletion using the Zippin method (1958).
    - If initial run yielded fewer than 50 individuals (and total fewer than 100 across repeats), a second 100 m reach upstream was electrofished with the same depletion approach.
  - Biomass estimation:
    - Mean biomass per taxon at each site/occasion computed from length-mass regressions and then multiplied by density estimates to obtain biomass per m2.

- Temporal scope:
  - Data collected on five occasions between October 2012 and October 2013.
  - Sampling did not occur during the salmonid breeding season (December–March) to avoid disturbing redds.

- Data purpose and use:
  - Used to construct quantified food webs detailing mass and nutrient flux between nodes.
  - Provides standing stock estimates of fish across sites and times.

- Provenance and responsibilities:
  - Collected, processed, and analyzed by the Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.
  - Data interpretation and management conducted by the same group.

- Data structure and metadata:
  - Key fields include:
    - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
    - OS_NGR, OS_EASTING, OS_NORTHING
    - SURVEY_DATE, REACH
    - TAXON_NAME
    - Biomass_mgperm2, Density_Noperm2, 2SD

- Quality assurance and limitations:
  - Protocols and standard procedures for benthic sampling and electrofishing were strictly followed.
  - No formal QA procedure (e.g., repeat surveys on different days within the same period) was implemented.
  - Electrofishing performed by qualified, experienced biologists (Bill Bellamy and Luke Scott) from the Game and Wildlife Conservation Trust.

- References:
  - Zippin, C. 1958. The removal method of population estimation. Journal of Wildlife Management 22:82-90.