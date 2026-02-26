# Countryside Survey vegetation plots 2022_23

## Overview
- Countryside Survey is a long-running audit of the UK's countryside, enabling comparison across time to detect gradual changes.
- The program adopted a rolling design in 2019 to maintain year-to-year monitoring while maximizing site coverage and handling climate variability.
- The current focus for UKCEH Countryside Survey (UKCEH-CS) is on soil and vegetation measurements at 1 km squares, forming part of a national-scale ecosystem monitoring effort.
- The dataset for 2022–2023 contributes to a continuous 5-year rolling cycle, with 500 randomly selected 1 km squares surveyed across GB, stratified by Land Classification.

## Design and rolling program
- Rolling program repeats surveys every five years or after 500 squares are completed, allowing detection of spatial and temporal changes with cost-effective fieldwork.
- Sample selection:
  - Based on the Countryside Survey of Great Britain method; includes all 1978 squares (256) for longest time-series continuity, extended by adding other squares first surveyed in earlier years (1990).
  - Approximately 100 squares are visited annually.
  - Excludes squares with >75% urban land or >90% sea coverage.
- Multi-metric, ecosystem-wide approach: data are collected to analyze soils, vegetation, headwater streams, habitats, and landscape features in an integrated manner.

## Sampling frame and site details
- Selection aims to provide robust national and subnational indicators across GB and its constituent countries.
- Original 1 km squares from 1978 remain core for long-term continuity; additional squares chosen to extend coverage and maintain representativeness.

## Field methods and data collection
- Data collected by trained field surveyors following standard protocols (Smart et al., 2020).
- Field surveys involve teams of botanical surveyors, preceded by intensive training to ensure consistency in identification and recording.
- Quality assurance:
  - 10% of plots re-surveyed by QA assessors.
  - QA efforts and analyses have been conducted by the same assessor since 1990 to ensure comparability and validate plot locations and habitat classifications (JNCC broad/priority habitats).
- Confidentiality: spatial distribution maps may be withheld at scale to protect data confidentiality.

## Data products for 2022–2023
- Two CSV files comprising vegetation data:
  - UKCEHCS_VEGETATION_PLOTS_2022_23.csv: Plot-level information
    - Key fields: YEAR, SQUARE_ID (1 km square), PLOT_ID, PLOT_TYPE, X/XX (plot area in m²), PLOT_BH (Broad Habitat), PLOT_PH (Priority Habitat), COUNTRY, COUNTY, ENV_ZONE_2007 and related descriptors, LC07 (Land Classification) and LC07_NUM.
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2022_23.csv: Species list per plot
    - Key fields: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, Species name and identifier (BRC_NAMES), NEST_LEVEL (nesting context), and cover metrics (ZERO_COVER, FIRST_COVER, TOTAL_COVER) with potential sums >100% in some cases.
- Nomenclature and references:
  - Species names follow Stace (1997); habitat classifications reference JNCC definitions (BAP and related classifications).

## Data quality, governance, and provenance
- Data collection adheres to rigorous field protocols and training (Smart et al., 2020).
- Independent validation and QA are designed to maintain high data quality and comparability across years.
- Data governance includes sharing underlying data where appropriate, with attention to metadata quality and data accessibility constraints.
- The dataset supports national and subnational indicators important for policy and environmental monitoring.

## Context and usage for monitoring frameworks
- Provides a unique, long-term time series enabling measurement of stock and change in GB countryside from a policy-relevant perspective.
- Supports monitoring of multi-scale, ecosystem-level changes in soils and vegetation, linked to habitat classifications and land-use context.
- The rolling program design buffers against annual climate fluctuations and enhances the resilience and usefulness of indicators for informing future decisions.
- Data can inform policy-relevant indicators related to vegetation composition, habitat distribution, and landscape-scale change, with results expected to be presented through reports, charts, or dashboards.

## Practical notes for users
- The 2022–2023 dataset captures vegetation plots across two consecutive years within the rolling cycle and aligns with the broader Countryside Survey methodologies and field handbooks (e.g., UK-SCAPE Field Survey Field Handbook 2020).
- A map illustrating square distribution is provided with confidentiality considerations (not all details are shown at scaled levels).
- Datasets are designed to be integrated with broader Countryside Survey outputs and related statistical reports (e.g., UK results and policy-focused analyses).