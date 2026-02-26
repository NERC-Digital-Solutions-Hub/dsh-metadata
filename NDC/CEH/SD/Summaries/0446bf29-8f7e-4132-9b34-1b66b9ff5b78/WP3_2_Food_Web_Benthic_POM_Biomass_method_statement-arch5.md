# Benthic particulate organic matter biomass

## What the dataset contains
- Ash-free dry mass (AFDM) of three size fractions of organic matter:
  - woody debris (>1 cm)
  - coarse particulate (>1 mm)
  - fine particulate (>0.250 mm)
- Measurements are recorded as means with standard deviations, derived from up to 10 replicate Surber samples per site per sampling occasion.

## Where the data were collected
- Three chalkstream sites in the Wessex chalk area:
  - Nine Mile River
  - River Till
  - River Wylye
- Sites chosen to reflect a gradient of landscape integrity and river invertebrate diversity.

## When the data were collected
- Timeframe: October 2012 to October 2013
- Sampling frequency:
  - Wyse (Wy) and Nine Mile River: seven occasions
  - Till: five occasions
- Note: River Till was not sampled during December–March to avoid disturbing salmonid redds.

## How the data were collected
- Up to 10 Surber samples per site per occasion (0.25 x 0.25 m, net mesh 0.025 mm) across a 100 m reach.
- In the lab:
  - Invertebrates sorted from mineral/organic material
  - Fractions retained, dried, and ashed to derive AFDM per fraction
  - Samples dried at 80°C for at least 24 hours, weighed
  - Fractions incinerated at 560°C for 8–12 hours, weighed again
- Units: AFDM in mg per m² of stream bed

## Why the data were collected
- To construct quantified food webs detailing mass and nutrient fluxes between nodes.
- To quantify standing stocks of benthic detritus resources.

## Who collected and interpreted the data
- Queen Mary University of London River Communities Group
- Led by Dr J. Iwan Jones
- Responsibilities included sample collection, processing, analysis, interpretation, and data management

## Completeness and sampling considerations
- Replication:
  - 10 replicate samples processed for Oct 2012, Feb 2013, Mar 2013, and May 2013
  - 5 replicate samples processed for Jul 2013, Aug 2013, and Oct 2013
- Notable limitation:
  - Till was not sampled during Dec–Mar due to salmonid breeding season

## Quality assurance
- Standard laboratory procedures for AFDM were followed
- No formal QA procedure (e.g., repeat analysis within a replicate) documented
- Final values checked for marked outliers (none found)

## Data structure and fields (column definitions)
- RIVER_ID: Unique river identifier in Britain
- SITE_ID: Unique sampling site identifier along each river
- RIVER_NAME: River name (from OS map)
- SITE_NAME: Site name
- NGR: Ordnance Survey National Grid Reference
- EASTING: OS Easting
- NORTHING: OS Northing
- SAMPLE_DATE: Date of sampling
- POM_Fraction: Fraction measured (woody debris >1 cm; coarse particulate >1 mm; fine particulate >0.250 mm)
- Mean_AFDM_mgperm2: Mean ash-free dry benthic biomass (mg m⁻²)
- SD_AFDM_mgperm2: Standard deviation of AFDM (mg m⁻²)
- AFDM_n: Number of benthic samples processed per site

## Data governance, sharing, and caveats (for data stewards)
- Documentation includes clear provenance: responsible group, sampling methods, and laboratory processing details.
- Metadata should be standardized across sites and years (units, fractions, coordinates) to ensure interoperability.
- Notable limitations to note when sharing or reusing:
  - Incomplete temporal coverage for River Till (no Dec–Mar data)
  - Absence of formal QA procedures beyond outlier checks
  - No explicit dataset repository or publication DOI indicated in the record
- Recommended actions for stewardship:
  - Attach a persistent identifier and licensing to the dataset
  - Include detailed method notes ( Surber, fractionation, AFDM calculation) in metadata
  - Provide data in a machine-readable portal-compatible format with the defined fields and units
  - Document any potential biases due to seasonal gaps or site-specific conditions for reuse in ecological modelling or food-web analyses