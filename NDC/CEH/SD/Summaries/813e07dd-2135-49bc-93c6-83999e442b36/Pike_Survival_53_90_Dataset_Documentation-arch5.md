# Pike Survival Data 1953-1990

## Overview
- Binary survival data for Pike (Esox lucius) derived from capture-mark-recapture.
- Collected by the Freshwater Biological Association (FBA) and later by CEH (Centre for Ecology & Hydrology) and its predecessors since 1989.
- Part of a larger set of Pike datasets; metadata links and related datasets provided.

## Data Content
- Dataset: PikeSurvivalData1953_1990.csv (CSV, 68 KB).
- Columns:
  - YEAR: Year of first capture of an individual fish.
  - LENGTH: Fork length at capture (cm).
  - SURVIVAL: 1 if the individual was recorded again (survived the first period after capture), 0 otherwise.
- Sampling site: Windermere Lake, Cumbria, Great Britain. Approximate center coordinates provided (OS Grid Reference, Easting/Northing, and latitude/longitude).
- Species: Esox lucius (Pike).
- Sampling includes males, females, and individuals of unknown sex.
- Data sources include both net-catch data and sightings from catch-and-release tagging.

## File Details and Format
- File name: PikeSurvivalData1953_1990.csv
- Format: Comma-separated values (CSV)
- Size: 68 KB

## Geographic and Temporal Coverage
- Location: Windermere Lake, Cumbria, Great Britain.
- Time frame: Data collected from 1944 onward; survival data in this file covers 1953–1990.
- Spatial reference: OS Grid Reference SD393960; alternative coordinates provided (OSGB36 Easting/Northing; WGS84).

## Sampling Design and Collection Methods
- Gill netting used to monitor Pike in north and south basins; methodology evolved over time.
- Since 1982, standardized method:
  - 64 mm bar mesh multifilament gill nets.
  - Each net: 40 m long, 3 m deep; set on the bottom.
  - Sampling Oct–Dec at ~10 sites per basin; five nets in water at any time.
  - Sites fished for two weeks per season; annual effort ~348 net days (1982–1989) and ~240 net days since 1990, distributed roughly equally between basins.
- Tagging: Individually-numbered tags; sightings by catch-and-release anglers maintained.
- Older methods (pre-1982) varied; standardization implemented from 1982 onward.

## Data Processing and Quality Control
- In-lab processing:
  - Measure fork length (to 1 mm) and weigh (to 100 g).
  - Determine sex; age fish using the left opercular bone with a nominal birth date of 1 April.
  - Integrate tagging sightings to compute survival (as defined in SURVIVAL).
- Quality control:
  - Measurements validated by permutations involving three individuals.
- Analytical basis:
  - Survival derived from combined capture data and tagged fish sightings (referenced methods by Haugen et al. 2007).

## Provenance, Rights, and Metadata
- Copyright: Database Right/Copyright © NERC - Centre for Ecology & Hydrology / Freshwater Biological Association (FBA).
- Document version: 1. 29-08-2013.
- Part of a data series with related metadata records and datasets (e.g., Pike 1944-2002 metadata; Pike Fecundity Data; Pike Growth Data; Windermere Lake Temperature).
- Metadata includes sampling regime, coordinates, and data lineage to support discovery and reuse.

## Related Datasets and References
- Related metadata: Pike 1944-2002 data series metadata.
- Related Pike datasets:
  - Pike - Fecundity Data 1963-2002
  - Pike - Growth Data 1944-1995
  - Windermere Lake Temperature 1944-2002
- Key references for methods and aging:
  - Aging method (Frost & Kipling, 1959)
  - Standardization and sampling descriptions (Le Cren, 2001; Winfield et al., 2008)
  - Survival calculation methodology (Haugen et al., 2007)

## Governance Considerations for Data Stewards
- Ensure metadata remain up-to-date and linkable to related datasets.
- Maintain documentation of methodological changes (pre-1982 vs post-1982 standardization) to support reproducibility.
- Preserve original data rights and attribution to NERC CEH/FBA; manage any reuse constraints implied by copyright.
- Support discoverability by cataloguing precise geographic coordinates and sampling details.
- Plan for updates or extensions (e.g., incorporating later data beyond 1990) while preserving historical context.