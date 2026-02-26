# Benthic particulate organic matter biomass

## Overview
- Dataset of ash-free dry mass (AFDM) for three benthic particulate organic matter (POM) fractions, collected from Surber samples.
- Data are presented as means with standard deviations across replicate samples.

## Where and when data were collected
- Location: three chalkstream sites in the Wessex chalk area — Nine Mile River, River Till, and River Wylye.
- Timeframe: October 2012 to October 2013.
  - Wylye and Nine Mile River: seven sampling occasions.
  - River Till: five sampling occasions.
- Sampling restrictions: no sampling during December–March salmonid breeding season to avoid disturbing redds.

## How data were collected and processed
- Field collection: up to 10 Surber samples per 100 m survey reach (0.25 x 0.25 m, mesh 0.025 mm).
- Laboratory processing: after removing invertebrates, retained fractions dried and ashed to determine AFDM:
  - Fractions: coarse woody debris (>1 cm), coarse particulate (>1 mm), fine particulate (>0.250 mm).
  - Procedures: dried at 80°C for at least 24 h, weighed; incinerated at 560°C for 8–12 h, weighed again.
- Data handling: samples per site/date summarized as mean AFDM per m² and standard deviation.

## Purpose and use
- Used to construct quantified river food webs and to quantify standing stocks of benthic detritus resources.
- Data collected by the Queen Mary University of London River Communities Group, led by Dr J. Iwan Jones.

## Data structure and definitions
- Key columns (examples):
  - RIVER_ID: unique river identifier in Britain
  - SITE_ID: unique site identifier along each river
  - RIVER_NAME / SITE_NAME: names
  - NGR / EASTING / NORTHING: geographic coordinates
  - SAMPLE_DATE: date of sampling
  - POM_Fraction: fraction category (coarse woody debris >1 cm; coarse particulate >1 mm; fine particulate >0.250 mm)
  - Mean_AFDM_mgperm2: mean AFDM (mg m^-2)
  - SD_AFDM_mgperm2: standard deviation of AFDM (mg m^-2)
  - AFDM_n: number of samples processed from each site
- Unit: mg m^-2 for AFDM measurements.

## Data completeness and quality
- Completeness varies by river:
  - 9 Mile River and Wylye: seven occasions each
  - River Till: five occasions
- Replicate counts per occasion:
  - 10 replicate samples processed on Oct 2012, Feb 2013, Mar 2013, May 2013
  - 5 replicates processed on Jul 2013, Aug 2013, Oct 2013
- Quality checks:
  - Follow standard laboratory procedures for AFDM
  - No formal quality assurance (e.g., no repeat analysis within a replicate Surber sample)
  - Final values checked for outliers (none found) before calculations

## Governance and provenance
- Data collection and analysis conducted by QMUL River Communities Group, led by Dr J. Iwan Jones.
- Documentation includes detailed table fields and definitions to support discovery and reuse. Coordinates and site identifiers facilitate geospatial discoverability.

## Considerations for data management and reuse
- There is variability in sampling frequency across rivers and limited QA procedures; consider implementing formal QA-like checks and replication validation in future work.
- Metadata is comprehensive for location, timing, and data structure, aiding integration with other datasets and GIS applications.
- The dataset supports user-focused outputs like food-web modeling and detritus standing stock assessments, aligning with systems-thinking data management goals.