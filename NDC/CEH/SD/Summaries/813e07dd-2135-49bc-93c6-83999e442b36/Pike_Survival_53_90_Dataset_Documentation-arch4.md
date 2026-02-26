# Pike Survival Data 1953-1990

## Overview
- Long-running survival (binary) dataset from capture-mark-recapture of Pike (Esox lucius) in Windermere Lake, Great Britain.
- Data cover 1953-1990, with collection beginning in 1944; originally by the Freshwater Biological Association (FBA) and later by CEH and its precursor IFE.
- Includes individuals of known and unknown sex; used in analyses such as Vindenes et al. (2013) American Naturalist.
- Dataset is part of a broader set of related Pike datasets and metadata records.

## Dataset Details
- Format and size: CSV file; approximately 68 KB.
- Columns: YEAR (year of first capture), LENGTH (fork length in cm at capture), SURVIVAL (1 if recaptured later, 0 otherwise).
- Sampling site: Windermere Lake, Cumbria; approximate lake-centre coordinates provided in OS grid and WGS84.
- Taxon: Pike (Esox lucius).

## Experimental Design and Sampling Regime
- Continuous monitoring of pike in north and south basins via gill netting with variations over time (1944–present).
- Since 1982, standardized sampling: 64 mm bar-mesh multifilament gill nets, 40 m x 3 m, set on the lake bottom, Oct–Dec, at ~4–5 m depth across 10 sites per basin.
- Typical schedule: five nets fished at five sites weekly, with rotation to cover the basin; two-week site coverage per sampling season.
- Annual effort: around 348 net days (1982–1989) and around 240 net days since 1990, distributed roughly equally between basins.
- Tagging and sightings: individually numbered tags used; catch-and-release sightings by anglers added to data.

## Collection Methods & Fieldwork
- In the lab: measure fork length (to 1 mm), weigh (to 100 g), determine sex; age determined from opercular bone (birth date assumed 1 April).
- Data integration: combine physical measurements with tag sightings to compute survival as described by Haugen et al. (2007).

## Data Processing and Quality Control
- Quality control involves measurements checked by permutations of three individuals to ensure accuracy.
- Survival (SURVIVAL) is derived using established methods that incorporate growth, weight, age, and recapture data.

## Metadata, Access, and Related Data
- Metadata and data lineage:
  - Metadata record for the series: Pike 1944-2002 and related datasets.
  - Related datasets include Pike Fecundity Data (1963-2002) and Pike Growth Data (1944-1995); Windermere Lake Temperature (1944-2002).
- Data licensing and rights: Database Right/Copyright © NERC - Centre for Ecology & Hydrology / Freshwater Biological Association (FBA).
- Access notes: data and metadata links provided for discoverability and reuse.

## Notable References and Context
- Methodology and age estimation references:
  - Frost & Kipling (1959) on aging pike using opercular bones.
  - Le Cren (2001) on Windermere pike project.
  - Winfield, James, & Fletcher (2008) on pike population dynamics in warming lakes.
  - Haugen et al. (2007) on density-dependent demography and dispersal.
- Analytical context: data were used to model trait-based dynamics and long-term population processes; dataset is part of a broader ecosystem analysis framework.

## Data Leadership Considerations (for Data Leaders)
- Demonstrates robust long-term data stewardship: standardized methods, detailed metadata, and clear data lineage across multiple decades.
- Highlights importance of documenting sampling designs, measurement protocols, and data processing steps to ensure reproducibility and reuse.
- Emphasizes the value of integrating measurement data with capture-mark-recapture and sighting information to derive meaningful survival metrics.
- Illustrates handling of evolving methodologies (e.g., standardization from 1982) and maintaining continuity for longitudinal analyses.