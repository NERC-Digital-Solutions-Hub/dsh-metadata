# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

## Project aim and context for monitoring frameworks
- Four-year Historic Droughts project (2014–2018) funded by UK Research Councils to develop cross-disciplinary understanding of past UK droughts and to improve tools for drought management.
- Recognizes droughts as complex events influenced by hydrometeorological, environmental, agricultural, regulatory, and social factors; aims to link hydrological data with socio-economic drivers to inform policy and future decisions.

## Inventory and outputs
- Historic Droughts Inventory: a knowledge base of past drought characteristics, impacts, and responses.
  - Part 1: hydro-meteorological timelines (rainfall, river flows, groundwater) with drought indicators extended back to the 19th Century.
  - Part 2: references to droughts from newspapers, legislation, agricultural media, and oral histories.
- Groundwater-related datasets within the Inventory include reconstructed groundwater levels (GWL) and the Standardised Groundwater level Index (SGI).

## Dataset description (key content and scope)
- Reconstructed groundwater levels for 54 observation boreholes across the UK, relative to Ordnance Datum (maOD).
- Time period: 1891 to 2015 (monthly time steps after reconstruction).
- For each site, 90% and 10% confidence bounds are provided.
- Site distribution: located on Principal Aquifers; majority on Chalk aquifers; Annex 1 lists site details.
- Primary motivation: extend groundwater records prior to the late 20th century to support drought case studies and management planning (e.g., reference events for Drought Management Plans).

## Data sources and inputs
- Groundwater level data: National Groundwater Level Archive (NGLA, BGS).
- Precipitation data: extended UK Climate Projections (UKCP09) grid-cell data used for model inputs.
- Temperature data: used to estimate potential evapotranspiration (PET) via temperature-based methods.
- Modeling backbone: AquiMod lumped conceptual model (BGS) used to reconstruct monthly GWL time series.

## Methodology for reconstruction and uncertainty
- Reconstruction method: 1) interpolate irregular NGLA records to monthly time steps; 2) run AquiMod to generate monthly GWL time series.
- Calibration and uncertainty quantification: Monte Carlo simulations generating ~1,000,000 parameter sets; GLUE framework used to assess behavioural parameter sets (Nash-Sutcliffe Efficiency > 0.5).
- Confidence bounds: 10th and 90th percentiles derived from the distribution of behavioural parameter runs for each date.

## Data formats and metadata
- Data files: CSV format, one file per site.
  - Columns include Date (YYYY-MM-DD, monthly start), GWL (maOD), Cl90_GWL (90th percentile), Cl10_GWL (10th percentile).
  - File naming follows a project/model/run/input/output/time/variable/catchment/borehole/version scheme.
- Metadata: a separate CSV (Metadata_forGWLandSGI_reconstructions.csv) with site-level metadata (Site_name, Easting, Northing, BGS_WellMaster_ID, Full_BGS_site_name, Aquifer, MORECS_ID, etc.).

## Governance, accessibility, and data governance considerations
- The dataset is part of a broader, publicly documented Inventory designed for transparency and reproducibility.
- Data provenance relies on originator datasets (NGLA, UKCP09) and state-of-the-art groundwater modeling (AquiMod).
- Publication emphasizes open data stewardship, documentation of methods, and clear data formats to enable reuse and verification.
- Challenges highlighted in related monitoring contexts include data gaps, access delays, silos, metadata inadequacy, data transformation needs, and governance requirements for data sharing and upkeep.

## Relevance for policy, planning, and future decisions
- Provides long-term groundwater context to inform drought preparedness, water resource planning, and utility risk assessments.
- Supports development of drought reference events and scenario analyses for policy instruments (e.g., drought plans and regulatory frameworks).
- Demonstrates a framework for integrating hydrometeorological and socio-economic information to improve environmental health monitoring and decision-making.

## Key references and acknowledgments
- Project funded by NERC (Historic Droughts, NE/L010151/1).
- Foundational references to aquifer properties, drought indicators, GWL reconstruction methods (AquiMod, GLUE, Nash-Sutcliffe, etc.).
- Acknowledges eight UK institutions contributing to the Historic Droughts Inventory and associated datasets.