# Countryside Survey vegetation plots 2019

## Overview
- Countryside Survey is a long-running audit of the UK countryside, conducted since 1978, enabling comparisons over time to detect gradual changes.
- It adopts a rolling, ecosystem-based monitoring approach (focusing on soils, vegetation, headwater streams, habitats, and landscape features) to capture multi-scale data.
- The 2019 phase marks the start of UKCEH-Countryside Survey (UKCEH-CS) rolling program, continuing the tradition with standardized methods and updated design.

## Design and rolling program
- Rolling program: repeats on a five-year cycle or after surveying 500 squares, initiated in 2019.
- Sampling frame: 500 x 1km squares randomly selected for survey, stratified by the Land Classification of Great Britain (ITE framework).
- Annual coverage: 100 squares visited each year to balance national coverage with year-to-year monitoring.
- Continuity and justification: the 1978 squares (256 total) form the backbone for the longest time series; additional squares from the 1990 cohort are included to extend the series.
- Exclusions: any square with more than 75% urban land or more than 90% sea is excluded.
- Rationale: the design provides robust national and sub-national indicators and buffers against climate-year extremes while maximizing site coverage.

## Methods and quality assurance
- Data collection: field surveys conducted by trained botanical survey teams following standardized protocols (Smart et al., 2019).
- Training and consistency: intensive pre-survey training for field teams; ongoing supervision and monitoring by experienced project staff.
- QA and validation: 10% of plots re-surveyed and assessed; QA activities conducted by the same assessor since 1990 to ensure consistency, detect detection rate variation, and validate plot locations and habitat classifications (JNCC broad and priority habitats).

## Data products and file structure
- Data coverage: vegetation data for 2019, with two CSV files:
  - Vegetation plots: plot information (location, square, plot type, habitat classifications, environmental zone, land classification, county, country, etc.).
  - Vegetation plot species: species list for each plot, including species identifiers, names, nest level, and cover metrics.
- Key fields in Vegetation Plots file (UKCEHCS_VEGETATION_PLOTS_2019.csv):
  - YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, PLOT_BH (Broad Habitat), PLOT_PH (Priority Habitat), COUNTRY, COUNTY, ENV_ZONE_2007, EZ_DESC_07, LC07, LC07_NUM.
- Key fields in Vegetation Plot Species file (UKCEHCS_VEGETATION_PLOT_SPECIES_2019.csv):
  - YEAR, SQUARE_ID, PLOT_ID, BRC_NUMBER, BRC_NAMES (species name), NEST_LEVEL, TOTAL_COVER, FIRST_COVER, etc.
- Nomenclature and standards:
  - Species nomenclature follows Stace (1997); data are aligned with established classifications (BAP habitats, JNCC broad habitats, LC07 land classes).
- Documentation and lineage:
  - Field handbook and methodological references provided (e.g., Smart et al., 2019; UK-SCAPE Field Survey Handbook 2019).

## Data standards, metadata, and provenance
- Design documentation and supporting readings underpin the dataset (e.g., Bunce et al. on land classification; Jackson 2000 on habitat interpretation; Maddock 2008 on UK Biodiversity Action Plan contexts).
- The dataset references and links to the Countryside Survey methodology, land classification schemes, habitat classifications, and associated technical reports.
- Data quality controls are embedded in the collection and QA process, with consistent validation of plot locations and habitat classifications.

## References and further reading
- Foundational methodological and background sources include: Bunce et al. (ITE Land Classification), Jackson (JNCC habitat guidance), Maddock (UKBAP descriptors), Norton et al. (policy-relevant measures), Scott (statistical reporting), Smart et al. (field handbook), Stace (nomenclature).
- Key reports and data centers: CEH/NERC publications, Countryside Survey website, and related datasets (e.g., 2007 UK results, land classification documentation).

## Implications for data leaders
- Long-term continuity with standardized procedures supports reliable trend analysis and cross-year comparability across GB and constituent countries.
- The rolling design optimizes site coverage while mitigating climate-year biases, providing timely insights for policy and management.
- Rich metadata, controlled vocabularies, and explicit classifications (habitats, land classification, environmental zones) enhance discoverability, interoperability, and integration with wider data networks.
- The data are designed for reuse across partners and networks, with transparent sampling design, QA processes, and detailed data dictionaries that support governance, stewardship, and co-ownership of data products.