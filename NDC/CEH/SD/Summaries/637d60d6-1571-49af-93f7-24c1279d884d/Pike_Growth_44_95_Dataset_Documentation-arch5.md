# Pike Growth Data 1944-1995

## Overview
- Dataset of growth (length) data on Pike (Esox lucius) from net sampling in Windermere Lake, Cumbria, Great Britain.
- Data collection began in 1944; initially collected by the Freshwater Biological Association (FBA) and since 1989 by CEH and its predecessor IFE.
- Contains only female pike in this dataset.
- Used in Vindenes et al. (2013) American Naturalist as part of a set of data files.
- Related datasets and metadata records exist for Pike growth (1944-2002), Pike fecundity (1963-2002), Pike survival (1953-1990), and Windermere lake temperature (1944-2002).

## Data and file details
- File: PikeGrowthData1944_1995.csv
- Format: CSV (comma separated values)
- Size: 675 kb
- Columns: YEAR (year of capture), LENGTH (fork length in cm), IND (individual fish identity number)
- Sampling site: Windermere Lake, Cumbria, UK
- Location coordinates provided (OS Grid Reference and WGS84)

## Dataset content and metadata
- Species measured: Esox lucius (Pike)
- Data lineage: datasets originate from long-term netting programs and lab processing of captured fish.
- Related metadata records:
  - Pike growth data series (1944-2002)
  - Pike fecundity data (1963-2002)
  - Pike survival data (1953-1990)
  - Windermere lake temperature data (1944-2002)

## Sampling design and collection methods
- Basins: northern and southern basins of Windermere Lake; monitoring by gill netting.
- Pre-1982: sampling varied; post-1982: standardized protocol implemented.
- Standardized methodology (since 1982):
  - Nets: 64 mm bar mesh multifilament gill nets
  - Net size: 40 m length x 3 m depth
  - Deployment: single nets, bottom-set, Oct to late Dec, ~4-5 m depth
  - Sites: 10 sites per basin
  - Schedule: five nets in the water at a time; sites fished over two weeks per season; weekly rotation with settlements around a Monday–Friday cycle
  - Effort: ~348 net days per year (1982–1989) distributed between basins; ~240 net days per year since 1990
- Catch processing: all pike killed on capture; lab processing includes measuring fork length to 1 mm and weighing to 100 g; sexing performed; age determined from left opercular bone with birth date set as 1 April
- Birth dating and aging references: Frost & Kipling (1959) method for age estimation

## Data handling and quality control
- Individual-level identification: each pike assigned an IND number
- Measurements and verification: quality control conducted via permutations involving three individuals to check measurements
- Documentation of methods and references to supporting literature:
  - Le Cren (2001) on Windermere perch and pike project
  - Winfield, James & Fletcher (2008) on pike population dynamics in warming lakes
  - Frost & Kipling (1959) on aging pike from scales and opercular bones

## Analytical context
- Analytical references associated with dataset:
  - Winfield, James & Fletcher (2008) on pike population size and condition relative to prey
  - Frost & Kipling (1959) on age and growth estimation methodology

## Data stewardship considerations
- Provenance and access: dataset originates from a long-running, standardized monitoring program; copyright remains with NERC - CEH / FBA
- Data governance: clearly documented sampling methods, site coordinates, and measurement protocols to support reproducibility and reuse
- Limitations and considerations for reuse:
  - Dataset represents only female pike
  - Temporal changes in sampling effort prior to 1982 may introduce comparability considerations; standardization applied from 1982 onward
  - Data primarily focused on length and identity; weight and age data are described but may require referencing linked publications for full methodological context
- Use case relevance: suitable for longitudinal growth analyses, age-structured studies, and integration with related datasets (fecundity, survival, temperature) for broad ecological inferences.