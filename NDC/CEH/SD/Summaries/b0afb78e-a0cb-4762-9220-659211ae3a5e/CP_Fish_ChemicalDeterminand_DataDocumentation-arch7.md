# Fish abundance, habitat, water quality, flow and climate in English Rivers from 1975-2017

## Overview
- Compiled dataset of fish abundance, habitat, water quality, flow and climate variables for English rivers, covering 1975–2017.
- Derived from Environment Agency water quality data (Water Quality Archive, Beta) and CHEMPOP project data integration.
- Aimed at supporting map-based analyses and GIS-driven exploration for policy, clients, and public audiences.

## Data contents and structure
- File format and organization:
  - Region_FISHWIMSStats_DET.csv: contains WIMS statistics for each fish sample location (Fish_SiteID) in regional subsets (Region RR*), for chemical determinands.
  - One file per chemical; file named Region_FISHWIMSStats_DET.csv; 18 variables per file; variable counts and names described below.
- Key identifiers and relationships:
  - Fish_SiteID: unique identifier for each fish site (used to join with Fish_SiteID in DataTable, Hydrology, and chemical determinand datasets).
  - 41 chemicals: determinands extracted from EA Water Quality data; list available in supporting documentation.
- Data coverage and exclusions:
  - England (geographic focus).
  - Some sites omitted due to licensing restrictions on sensitive data.
- Versioning:
  - No multiple versions indicated; dataset published with citation (2024) from NERC EDS.

## Methods and processing
- Determinand site selection and matching:
  - ArcGIS Near Table Generator used to identify the three nearest chemical determinand sites to each fish site.
  - Manual checks against predefined criteria:
    - Determinand sites must have at least 25 samples.
    - Proximity and river-order compatibility (same river or similar order).
    - Timeframe overlap with fish sampling dates (2-year allowance if needed).
  - Distance considerations: unsuitable if only very distant determinand sites are available.
- Data extraction and aggregation:
  - Extracted from EA Water Quality portal for the selected determinands.
  - Anteceding period defined as the 12 months immediately prior to the fish survey date.
  - Temporal aggregation performed after extraction.
  - For some determinands (notably metals), a maximum threshold of 10 mg/l applied; values above discarded for statistics.
- Handling below LoQ (limit of quantification):
  - Three treatment options considered: LoQ, 0, or LoQ/2.
- Statistics computed per fish site:
  - Basic statistics: minimum, maximum, median, mean, standard deviation.
  - Additional counts: total number of samples, number below LoQ, number above LoQ.
- Software and standards:
  - GIS: ArcGIS (10.7+ or Pro) for site matching.
  - Scripting: Python 3 (modules: math, pandas, numpy, itertools, datetime, dateutil, os, time, shutil) for data extraction and calculation.
- Quality assurance:
  - Subset chemical matching checked by Monika Jurgens.
- Personnel:
  - Monika Jurgens, Rachel Ainsworth, Virginie Keller, Nuria BachellerJareno.

## Data quality, restrictions and access
- Licensing:
  - Data derived from Environment Agency water quality data; copyright and/or database rights held by Environment Agency.
  - Some determinand data cannot be included in the final published dataset due to licensing restrictions.
- Access points:
  - Public data portal: https://environment.data.gov.uk/water-quality/view/landing
- Citation:
  - Ainsworth et al. (2024). Fish abundance, habitat, water quality, flow and climate data from English rivers, 1975-2017. NERC EDS Environmental Information Data Centre. DOI: 10.5285/b0afb78e-a0cb-4762-9220-659211ae3a5e

## GIS considerations and usage tips
- Data join and integration:
  - Use Fish_SiteID to join Region_FISHWIMSStats_DET.csv (per chemical) with corresponding fish site records, hydrology, and chemical determinand datasets.
- Data fields and interpretation:
  - Key variables per determinand file (per chemical):
    - W1_SMPT_REF: determinand sampling point reference.
    - WQ_Min_LOQ1/2/3, WQ_Max_LOQ1/2/3, WQ_Median_LOQ1/2/3, WQ_Mean_LOQ1/2/3, WQ_STD_LOQ1/2/3: statistics for anteceding period with LOQ handling variants.
    - WQ_Count: total chemical samples in anteceding period.
    - WQ_COUNT_L_LOQ, WQ_COUNT_G_LOQ: counts of samples below/above LOQ.
  - 18 variables per file; overall structure supports comparing fish-site metrics with nearby determinand measurements across multiple chemicals.
- Scope and resolution considerations:
  - Temporal scope centered on 12-month antecedent period prior to each fish survey date.
  - Spatial scope limited to England; requires careful regional aggregation if cross-regional analysis is needed.
- Practical notes for GIS analysts:
  - Expect regional groupings (Region RR*) and per-chemical files; plan data joins accordingly.
  - Be mindful of licensing-restricted sites when interpreting or visualizing the dataset; some sites may be omitted from mapping.