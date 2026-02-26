# Coastal Biodiversity and Ecosystem Service Sustainability (CBESS) surface sediment chlorophyll concentrations in saltmarsh and mudflat habitats

## Overview
- Dataset of surface sediment chlorophyll concentrations (chlorophyll a, b, and c1+c2) in saltmarsh and mudflat habitats.
- Measurements expressed as micrograms per gram of sediment (µg g⁻¹) from the top 2 mm of sediment.
- Seasonal sampling: winter and summer 2013; five replicates per quadrat.
- Sites across Essex (Abbotts Hall, Fingringhoe Wick, Tillingham Marshes) and Morecambe Bay (Cartmel Sands, Warton Sands, West Plain) representing contrasting habitats and sediment types.
- Purpose aligned with monitoring of microphytobenthos (MPB) and habitat health within the CBESS program.
- Lead staff: Jack Maunder.

## Spatial and site information
- Essex sites chosen for cohesive clay mudflats and saltmarsh with clay soils; Morecambe Bay sites represent sandy soils.
- Saltmarsh and mudflat habitats chosen to reflect differences in inundation frequency, creek structure, and vegetation.
- Geographic coordinates provided for each observation location.
- 22 randomly allocated 1 m x 1 m quadrats per mudflat and per saltmarsh site, with four spatial scales (A–D).

## Measurements and variables
- Primary variables: 
  - Chlorophyll a concentration (µg g⁻¹)
  - Chlorophyll b concentration (µg g⁻¹)
  - Chlorophyll c1+c2 concentration (µg g⁻¹)
- Dataset fields also include: season, location, site, habitat, quadrat number, and scale.

## Methods and laboratory procedures
- Sampling: surface sediment (top 2 mm) collected with a contact corer; samples flash-frozen in liquid nitrogen and stored below -80°C.
- Preparation: samples freeze-dried (Edwards EF4 Modulyo).
- Extraction and analysis: chlorophyll extracted with acetone; quantified with Cecil CE3021 spectrophotometer at 630, 647, 664, and 750 nm; concentrations derived via standard equations.
- Quadrats: randomly allocated using R; 22 quadrats per site; four spatial scales defined for sampling design.
- Calibration and quality control:
  - Scale calibrations following laboratory protocols.
  - Spectrophotometer accuracy checked with standard chlorophyll solutions.
  - Data checks include manual entry verification of readings into spreadsheets.

## Data formats and structure
- Primary format: comma-separated values (CSV).
- Metadata fields include:
  - Chl a, Chl b, Chl c1+c2 (average and standard deviation)
  - Row numbers and header information
  - Season (Winter, Summer)
  - Location (Morecambe, Essex)
  - Site (e.g., CS, WS, WP, AH, FW, TM)
  - Habitat (Mudflat, Saltmarsh)
  - Quadrat Number (1–22)
  - Scale (A–D with descriptive ranges)
- Note: some sections of the provided metadata appear duplicated or reformatted, but the key data columns are the chlorophyll concentrations and their statistics, site/habitat metadata, and sampling design details.

## Data management and governance
- Data are generated under a structured CBESS field campaign with explicit sampling design and replicates.
- Metadata describe sampling strategy, lab procedures, and calibration steps to support reproducibility and quality assurance.
- Data governance considerations include the need for clear data provenance, data quality checks, and the potential for data sharing or public release in line with CBESS data governance.

## Temporal and data availability considerations
- Temporal coverage limited to winter and summer 2013; no repeat sampling planned within the described campaign.
- The dataset provides detailed field and lab methodologies to enable secondary use and comparability with other CBESS datasets and monitoring programs.

## Relevance for monitoring frameworks and policy
- Provides a robust, site-specific measure of MPB-associated chlorophyll concentrations across contrasting coastal habitats.
- Useful for cross-site comparisons, trend analyses (where longitudinal data exist), and evaluating environmental health of saltmarsh and mudflat ecosystems.
- Rich metadata and standardized methods support integration into dashboards, reports, or governance-driven monitoring frameworks.
- Potential barriers to data sharing are mitigated by explicit data handling and quality control steps described, though actual public access policies are not stated.