# Pike Growth Data 1944-1995

## Overview
- Dataset of growth (length) data for Pike (Esox lucius) from net sampling.
- Focus: females only.
- Collected starting in 1944; data currently maintained by CEH and its predecessor IFE/FBA.
- Part of a set used in Vindenes et al. (2013) American Naturalist study on climate-change effects in freshwater ecosystems.
- File: PikeGrowthData1944_1995.csv (CSV, 675 KB).

## Data structure and contents
- Columns: YEAR (year of capture), LENGTH (fork length in cm, to 1 mm), IND (individual fish identity, 1 is the ID).
- Location: sampling at Windermere Lake, Cumbria, Great Britain.
- Spatial reference: approximate grid center SD393960 (OS Grid), OSGB36 Easting/Northing 339385,496080; coordinates in WGS84 are 54.360193, -2.935836.
- Species: Esox lucius (Pike).

## Spatial and temporal coverage
- Spatial: Windermere Lake, two basins (north and south); sites fished across the lake with systematic coverage.
- Temporal: data span from 1944 to 1995 for the recorded growth measurements (sampling regime and methods described for various periods).

## Sampling methodology and collection details
- Sampling method: gill netting; nets used since 1982 standardized (64 mm bar mesh, 40 m x 3 m nets).
- Sampling seasons: October to December; sites sampled in the north and south basins.
- Site coverage: five nets in the water at any time; sites rotated to cover the lake; each site fished for about two weeks per season.
- Annual sampling effort: approximately 348 net days (1982–1989) and about 240 net days since 1990, distributed roughly equally between basins.
- Historical methods prior to 1982 varied; standardization implemented from 1982 onward.

## Measurements and processing
- In-lab measurements: each pike assigned an IND ID; measured for fork length (LENGTH) to 1 mm and weighed to 100 g; sex determined.
- Aging: opercular bone exam used to age fish, with a nominal birth date of 1 April.
- Quality control: measurements verified through permutations involving three individuals.

## Quality control and data quality
- Standardization of methods since 1982 to improve comparability.
- Quality checks tied to multiple-individual permutations to ensure measurement reliability.
- Documentation references key supporting methods and age determination (Frost & Kipling 1959; Le Cren 2001; Winfield et al. 2008).

## Related datasets and references
- Related metadata: Pike 1944-2002 (metadata record)
  - http://data.ceh.ac.uk/metadata/58357e70-d79b-4149-aa02-762c20b01198
- Pike - Fecundity Data 1963-2002
  - http://data.ceh.ac.uk/metadata/b8886915-14cb-44df-86fa-7ab718acf49a
- Pike - Survival Data 1953-1990
  - http://data.ceh.ac.uk/metadata/813e07dd-2135-49bc-93c6-83999e442b36
- Windermere Lake Temperature 1944-2002
  - http://data.ceh.ac.uk/metadata/9520664c-eb4d-4700-b064-5d215d23e595
- Core analytical references for Pike data:
  - Winfield, James & Fletcher (2008) on pike population dynamics in a warming lake.
  - Frost & Kipling (1959) on aging methods from scales and opercular bones.

## Data provenance and access
- Custodians: Natural Environment Research Council (NERC) – Centre for Ecology & Hydrology (CEH) and Freshwater Biological Association (FBA).
- Document version: 1 (29-08-2013).
- File format: CSV with explicit year-length-individual records and site-level context.

## GIS considerations and integration tips
- Use coordinates to georeference Windermere Lake area; OS Grid references enable precise localization.
- IND identifies individual fish across years; can be used to track length trends over time by year.
- Length data can be joined with other Lake Windermere datasets (e.g., temperature, fecundity, survival) to build multi-layer GIS analyses.
- Data resolution varies historically due to non-standardized methods before 1982; rely on 1982 onward standardization for spatial-temporal analyses.
- When integrating with other datasets, maintain consistent temporal windows and accounting for female-only sampling.
- Potential to aggregate by basin, year, or site for spatial trend analyses within the lake.