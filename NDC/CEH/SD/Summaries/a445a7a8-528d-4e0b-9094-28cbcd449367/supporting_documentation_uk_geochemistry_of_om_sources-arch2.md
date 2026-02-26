# Supporting documentation for data resource UK_geochemistry_of_OM_sources.csv

## Overview
- Documents bulk elemental and stable isotope composition of organic matter across terrestrial, intertidal, and marine environments in the UK (2016–2021).
- Contains 491 samples intended to constrain organic carbon sources (terrestrial vs marine) when used with isotope mixing models.
- Includes metadata on locations, sampling contexts, and intended data uses.

## Datasets described
- UK_geochemistry_of_OM_sources.csv
  - Scope: bulk elemental (organic carbon and nitrogen) and stable isotope (δ13C_org, δ15N) composition.
  - Sampling: terrestrial (soil, peat, living/dead biomass), intertidal (saltmarsh components, seagrass, mudflat, faecal matter), and marine (macroalgae, microalgae, zooplankton, finfish aquaculture waste) across the UK.
  - Variables: δ13C_org (‰), δ15N (‰), OC_content (%), N_content (%), C/N ratio, N/C ratio.
  - Methods: sampling in coastal catchments; storage at -20°C; drying at 40°C for 72 h; milled to fine powder; carbonate removal via acid fumigation; EA-IRMS analysis; calibration with high OC sediment standard (B2151).
  - QA/QC: lab calibration per University of St Andrews practices; repeat analyses for QA.
  - Format: .csv; dataset designed to support isotope-based source attribution.
  - Purpose: to anchor isotopic mixing models for environmental source apportionment.

- Aboveground_Biomass_Carbon_UK.csv
  - Description: metadata table detailing sample identification and classification for aboveground biomass carbon across UK ecosystems.
  - Structure: Sample_id, Sample_class with categories such as Terrestrial Vegetation, Soil, Wetland Vegetation, Zooplankton, Seagrass (Vegetation/Soil), Saltmarsh (Vegetation/Roots), Phytoplankton, Mudflat, Mix, Microalgae, Macroalgae, Faecal Matter, Aquaculture, Analytical Standard.
  - Additional fields: Detailed sample descriptions, National Vegetation Classification (NVC), Location, Nation (England, Scotland, Wales).
  - Purpose: supports contextualization of carbon data within vegetation/biomass types and national classifications.

## Methods and quality assurance
- Field and lab procedures
  - Field descriptions provided by experts; sampling across coastal catchments.
  - Sample handling: stored at -20°C; dried (40°C, 72 h); milled to fine powder.
  - Isotopic and elemental analyses: ~12 mg processed sediment in tin capsules for OC and δ13C_org; ~12 mg in silver capsules with acid fumigation for carbonate removal and δ13C_org; N and δ15N from tin capsules.
  - Instrumentation: EA-IRMS for stable isotope measurements.
- Calibration and quality control
  - Isotopic values QC’d via repeat analyses of standard high-OC sediment (B2151) with known reference values.
  - Laboratory practices aligned with established protocols (University of St Andrews).

## Data standards and formats
- File formats: .csv for both datasets.
- Key variables and units:
  - δ13C_org: per mil (‰)
  - δ15N: per mil (‰)
  - OC_content: percent (%)
  - N_content: percent (%)
  - CN: dimensionless (C/N ratio)
  - NC: dimensionless (N/C ratio)
- Descriptive fields in the Aboveground_Biomass_Carbon_UK.csv include sample_class, Description, NVC, Location, Nation.

## Geographic scope and context
- United Kingdom-wide data (terrestrial, intertidal, and marine environments).
- Nations represented: England, Scotland, Wales.
- Location descriptions emphasize coastal catchments and diverse UK habitats to capture broad organic matter diversity.

## Use cases and applications
- Enables standardized assessment of environmental health indicators through geochemical and isotopic data.
- Supports isotope-based modelling to apportion organic carbon sources (terrestrial vs marine) in environmental systems.
- Provides a transparent data backbone for monitoring outcomes and policy performance over time.
- Datasets are designed for deposition into appropriate data portals and for reuse in downstream environmental analyses.

## How this aligns with the Analysts Monitoring the Environment archetype
- Data verification and quality assurance are foregrounded (standardised sampling, QA with reference standards, consistent lab practices).
- Analyses rely on standardised methods to produce outputs suitable for reports, maps, and charts.
- Datasets are curated (clear metadata, sample classifications, national context) and prepared for storage/upload to data portals.
- Encourages data integration by highlighting opportunities to combine these datasets with other environmental data to enhance value and accessibility.

## Challenges and opportunities
- Increasing dataset value through integration with additional relevant data sources (beyond single-use applications).
- Improving access to underlying data to enable re-use, replication, and broader scrutiny by stakeholders.

## References
- Harris, D., Horwáth, W.R., and Van Kessel, C., 2001. Acid fumigation of soils to remove carbonates prior to total organic carbon or carbon-13 isotopic analysis. Soil Science Society of America Journal, 65(6), pp.1853-1856.
- Rodwell, J.S., 2000. Maritime communities and vegetation of open habitats. vol. 5: Maritime communities and vegetation of open habitats.