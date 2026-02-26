# Supporting documentation for data resource UK_geochemistry_of_OM_sources.csv

## Overview
- Describes bulk elemental and stable isotope composition of organic matter from terrestrial, intertidal, and marine environments in the UK (2016–2021).
- Sample set of 491 across terrestrial (soil, peat, living/dead biomass), intertidal (saltmarsh vegetation, roots, seagrass, mudflat, faecal matter), and marine environments (macroalgae, microalgae, zooplankton, finfish aquaculture waste).
- Purpose: support constraining organic carbon sources (terrestrial vs marine) when used with isotope mixing models.

## Data content and scope
- Geographic coverage: United Kingdom (locations described with specific coordinates and location descriptions).
- Observed variables (primary): δ13C_org (‰), δ15N (‰), OC content (%), N content (%), C/N ratio, N/C ratio.
- Sampling and storage: coastal catchments; field descriptions recorded; samples stored at -20°C prior to analysis.
- Analytical scope: bulk elemental composition and stable isotopes analyzed after sample preparation and isotope ratio mass spectrometry.

## Sampling, preparation, and analysis methods
- Sample preparation: oven drying (40°C for 72 hours), milled to fine powder.
- Stable isotope analysis: ~12 mg processed sediment in tin capsules and ~12 mg in silver capsules; acid fumigation for carbonate removal; analyses performed with EA-IRMS.
- Calibration and QA: isotopic values quality controlled via repeat analysis of high OC sediment standard (B2151) with reference C and N values; laboratory calibrations conducted at the University of St Andrews.
- Notes on data and statistics: Statistical treatment field marked as NA; data checks are tied to standard lab practices.

## Data structure and variables
- File format: .csv.
- Variables observed: δ13C_org (‰), δ15N (‰), OC (%), N (%), CN (C/N), NC (N/C).
- Location metadata includes varied descriptive fields and geographical coordinates as part of the UK sampling framework.
- Metadata handling: sampling locations described in field by experts; materials and standards referenced (e.g., lignin, humic acid, cellulose, glucose, protein; standard reference B2151).

## Data resource description for Aboveground_Biomass_Carbon_UK.csv
- Description: includes sample_id and sample_class (e.g., Terrestrial Vegetation, Soil, Wetland Vegetation, Zooplankton, Seagrass Vegetation/Soil, Seagrass, Saltmarsh vegetation, saltmarsh roots, Phytoplankton, Mudflat, Mix, Microalgae, Macroalgae, Faecal Matter, Aquaculture, Analytical Standard).
- Additional fields: NVC (National Vegetation Classification), Location, Nation (Scotland, England, Wales).
- Isotopic and elemental data: delta_13C_org (‰), delta_15N (‰), OC (%), N (%), CN, NC.
- Data format and usage: stored as .csv with detailed sample descriptions and classifications to support integration with isotope-based source attribution.

## Data quality, provenance, and usage notes
- Provenance: data produced by UK researchers; analyses conducted at specialized labs (e.g., James Hutton Institute; University of St Andrews).
- References for methods: Harris et al. (2001) on acid fumigation for carbonate removal; Rodwell (2000) for maritime vegetation classification context.
- Use cases: data suitable for constraining terrestrial vs marine OC sources when combined with isotope mixing models; integration with other datasets via provided metadata (NVC, nation, location).

## Potential applications and considerations for analysts
- Use to identify and quantify contributions of terrestrial vs marine organic matter in UK environments.
- Can support ecosystem carbon budgeting, watershed-to-coast carbon flow analyses, and environmental management decisions.
- Be mindful of data scope (UK-wide 2016–2021) and the NA markers for some statistical treatments when planning analyses.
- Consider data access pathways and metadata richness when unifying with other datasets that may have different formats or scales.