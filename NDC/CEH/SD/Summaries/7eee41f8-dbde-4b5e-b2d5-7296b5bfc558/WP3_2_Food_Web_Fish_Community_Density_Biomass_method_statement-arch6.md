# Fish biomass and density data

- This dataset records the density and biomass of fish taxa across three chalkstream sites in the Wessex chalk area (Nine Mile River, River Till, River Wylye) collected between October 2012 and October 2013, over five occasions.
- Data were used to construct quantified food webs detailing mass and nutrient fluxes and to quantify standing stocks of fish.

## Data collected

- Taxa-level data: biomass per square metre (mg m^-2) and population density per square metre for each taxon at each site and date.
- Site-level and location metadata: river and site identifiers, river name, site name, OS grid references (NGR, Easting, Northing).
- Temporal data: survey date for each sampling occasion.
- Spatial unit within sites: 100 m reach (REACH) sampled per site.

## Study sites and timing

- Sites: Nine Mile River, River Till, River Wylye (within the Wessex chalk stream region).
- Sampling occasions: five dates between Oct 2012 and Oct 2013.
- Seasonal note: sampling avoided the salmonid breeding season (Dec–Mar) to minimise disturbance to redds.

## Data collection methods

- Fish population assessment:
  - Multi-pass electrofishing for most fish species and sizes.
  - Modified Hess sampler (0.12 m^2) used to sample benthic species poorly captured by electrofishing (e.g., bullheads, stone loach).
  - 20 Hess sampler deployments per date in a stratified-random regime.
- Density estimation:
  - Zippin maximum likelihood method used to estimate population densities.
  - If fewer than 50 individuals were captured in the first run or fewer than 100 in total across runs, a second 100 m reach upstream was electrofished, with additional repeat runs to achieve satisfactory depletion.
- Biomass estimation:
  - Biomass per taxon per site per date derived by applying length-mass regressions to individual measurements, then multiplying by density estimates to obtain biomass per m^2.
- Field protocol:
  - 100 m reach surveyed per site; sampling conducted downstream to upstream.
  - Benthos sampling involved disrupting substrate to induce fish to enter the catch, then identification to species, measuring (tip of head to tail fork), and weighing.

## Derived metrics and data fields

- Key fields:
  - RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME
  - OS_NGR, OS_EASTING, OS_NORTHING
  - SURVEY_DATE
  - REACH (100 m segment identifier)
  - TAXON_NAME (scientific name)
  - Biomass_mgperm2 (mg per m^2)
  - Density_Noperm2 (number per m^2)
  - 2SD (two-standard-deviation around the density estimate; may be absent if not calculable)
- Source references for methods:
  - Zippin, 1958 (population estimation method)
  - Field procedures for benthic sampling and electrofishing as described in the study

## Data completeness and quality assurance

- Completeness:
  - Five sampling occasions across three sites; no sampling during salmonid breeding season.
- Quality assurance:
  - Strict adherence to established protocols for benthic sampling and electrofishing.
  - No formal QA procedure such as repeated surveys of the same reach within the same period.
  - Electro fishing conducted by fully qualified, experienced biologists.
- Limitations:
  - Some taxa may have insufficient data to calculate SD (2SD may be missing).
  - Potential under-sampling of certain species due to method limitations (e.g., electrofishing effectiveness biases).

## Provenance and intended use

- Data collection and analysis led by Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.
- Purpose: support construction of quantified food webs and assessment of standing stock of fish; enable downstream analyses of mass and nutrient flux between food-web nodes.

## Data reference and terminology

- The dataset includes a defined schema of identifiers and measurements (RIVER_ID, SITE_ID, RIVER_NAME, SITE_NAME, OS_NGR, OS_EASTING, OS_NORTHING, SURVEY_DATE, REACH, TAXON_NAME, Biomass_mgperm2, Density_Noperm2, 2SD).
- Primary methodological references include Zippin (1958) for population estimation and standard field sampling protocols for benthic fish and electrofishing.