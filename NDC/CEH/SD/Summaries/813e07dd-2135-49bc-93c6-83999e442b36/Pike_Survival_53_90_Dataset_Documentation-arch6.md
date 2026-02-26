# Pike Survival Data 1953-1990

## Description
- A data file used in Vindenes et al. (2013) American Naturalist describing survival (binary) data derived from capture-mark-recapture of Pike (Esox lucius) from Windermere Lake, UK.
- Data collection began in 1944; the dataset focuses on survival during 1953-1990.
- Initially collected by the Freshwater Biological Association (FBA); since 1989 by CEH and predecessors.
- Includes both sexes and individuals of unknown sex.

## Data format and size
- Format: CSV
- Size: 68 KB
- Columns (variables available in this dataset):
  - YEAR: Year of first capture of the individual fish
  - LENGTH: Length of the individual at capture (cm)
  - SURVIVAL: 1 if the individual was recorded again (survived the first period after capture), 0 otherwise

## Sampling site and location
- Windermere Lake, Cumbria, Great Britain
- Approximate grid reference: SD393960; coordinates ~54.360193, -2.935836

## Fish species measured
- Esox lucius (Pike)

## Experimental design and sampling regime
- Pike monitored in the north and south basins via gill netting with variations in early years; later standardized (since 1982) using a mark-and-release program with individually numbered tags.
- Sightings of tagged fish by catch-and-release anglers also recorded.
- Sex determined from dissection; age estimated from opercular bone; birth date assumed 1 April.

## Collection methods and fieldwork
- Pre-1982: varied gill-netting methods (mesh size, net dimensions, and sampling effort).
- Since 1982: standardized protocol
  - 64 mm bar mesh multifilament gill nets
  - Each net: 40 m long, 3 m deep
  - Set on the lake bottom, typically Oct–Dec, at depths ~4–5 m
  - 10 sites per basin (north and south), five nets in water at a time
  - Sites rotated; each site fished for two weeks per season
  - Annual sampling effort: ~348 net days (1982–1989), ~240 net days since 1990
  - All pike captured are killed, measured, weighed, and processed in the lab

## Analytical methods
- In the lab, each pike is measured (fork length to 1 mm), weighed (to 100 g), and sexed.
- Age determined from left opercular bone with a nominal birth date of 1 April.
- The SURVIVAL indicator is calculated by combining physical measurements with sightings of tagged fish (catch-and-release data) following methods described in Haugen et al. (2007).

## Quality control
- Measurements are validated by permutations of three individuals to check accuracy.

## Related datasets and metadata
- Metadata record for Pike 1944-2002: http://data.ceh.ac.uk/metadata/58357e70-d79b-4149-aa02-762c20b01198
- Pike - Fecundity Data 1963-2002: http://data.ceh.ac.uk/metadata/b8886915-14cb-44df-86fa-7ab718acf49a
- Pike - Growth Data 1944-1995: http://data.ceh.ac.uk/metadata/637d60d6-1571-49af-93f7-24c1279d884d
- Windermere Lake Temperature 1944-2002: http://data.ceh.ac.uk/metadata/9520664c-eb4d-4700-b064-5d215d23e595
- Key references for methods and context:
  - Le Cren (2001) on Windermere perch and pike project
  - Winfield, James, & Fletcher (2008) on pike in warming lakes
  - Frost & Kipling (1959) on age and growth estimation from scales and opercular bones
  - Haugen et al. (2007) on density dependence in demography and dispersal

## Practical notes for data support and reuse
- The dataset provides a binary survival outcome linked to the first post-capture interval; consider aligning Year and LENGTH with any longitudinal analyses or integrating with age, sex, and growth data from related Pike datasets.
- Be aware of methodological differences prior to 1982 when comparing with post-1982 data due to standardization.
- The data are suitable for demographic analyses, survival modeling, and cross-dataset integration (e.g., with Fecundity or Growth data) to study trait-based dynamics in pike populations.