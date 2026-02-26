# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

## Overview and context
- Soil survey results from England, Scotland and Wales conducted in 2013–2014 (with 2016 reference) as part of the NERC Macronutrient Cycles LTLS project: Analysing and simulating long-term and large-scale interactions of carbon, nitrogen and phosphorus in UK land, freshwater and atmosphere.
- Purpose: provide standardized soil property data to enable assessment of environmental health, carbon/nutrient stocks, and policy-relevant environmental monitoring over time.
- Outputs are structured as multiple interrelated datasets with detailed metadata and unit definitions to support reproducibility and interoperability.

## Sampling design and field methods
- Sampling area: at each site, soil collected within an area of roughly 100 × 100 m.
- Core layout: a central line with regular points spaced 11 m apart (10 cores) or 16 m apart (6 cores); cores randomized relative to line points.
- Number of cores: typically 10 cores for semi-natural habitats; 6 cores (sometimes 10) for agricultural fields.
- Core collection: vegetation and loose litter removed; van Walt split corer used; depth sampling varied by site:
  - Ribble sites: top 20 cm sampled first, then the next 20 cm.
  - Other locations: sampled to 15 cm depth, then to an additional 25 cm; total depths often 40 cm or slightly more, with occasional shortfalls.

## Data structure and key datasets
The documentation defines multiple datasets with standardized column headings and detailed field definitions, including but not limited to:
- Locations_and_dates
  - Sample_ID, catchment, site_name, OS_Grid_ref, Easting, Northing, Latitude, Longitude, Altitude_metres, Sampling_date.
- Bulk_density_data
  - BD_T, BD_P, BD_F (bulk densities for different size fractions); units in g cm-3; includes measurement descriptions (e.g., core volume, dry weight).
- Charcoal_and_coal_data
  - Charcoal/coal fractions, >2 mm solids, loss on ignition (LOI), charcoal fraction of LOI, etc.
- Radiocarbon_codes
  - SUERC code, radiocarbon facility code, and related identifiers for samples requiring AMS dating.
- Site_vegetation_data
  - Habitat_type, Habitat_type_with_detail, Vegetation, and associated site classification fields.
- Soil_chemistry_and_isotope_data
  - Thickness of sampled layer (cm); bulk densities (BD_T, BD_P, BD_F); pH; organic and inorganic phosphorus (P_tot_%); carbon (C_%); nitrogen (N_%); delta13C; 14C pMC; methods (e.g., Aqua regia digestion, ICP-OES, Vario EL); notes on detection limits.
  - Secondary metadata: sample identifiers, depth indicators (surface vs deeper soil), and method-specific details (e.g., digestion and analysis technique).
- Soil_classifications_England_and_Wales
  - NSI_series, NSI_Subgroup, NSI_classification, MODERN_DEF, and related NSI source data.
- Soil_classifications_Scotland
  - Site_code, association with 250K soil maps, dominant soil map unit, and other Scotland-specific classification details; linked to James Hutton Institute data.
- Soil_cores_and_depth
  - Depth (shallow/deep), number of cores, mean thickness (cm), and related core statistics.
- Soil_texture_data
  - Clay (%), Silt (%), % clay and silt by mass; particle-size fractions measured with Beckman Coulter LS200 laser granulometer; HOC flag indicating high organic content where texture not determined.

## Measurements, processing, and methodologies
- Field sampling
  - Standardized core collection with explicit depth horizons and core counts by habitat type.
- Laboratory analyses (representative examples)
  - Bulk density (BD_T, BD_P, BD_F) based on core volumes and dry weights.
  - Soil chemistry and isotopes: pH (glass electrode), C%, N%, P_tot_% (inorganic and organic via digestion and ICP-OES), delta13C, and 14C pMC.
  - Elemental analyses: Vario EL for C and N; ICP-OES for P after acid digestion; LOI determined by ignition at 450°C.
  - Charcoal and coal content: microscopy and oxidation treatments; LOI and charcoal fraction calculations.
  - Texture: clay and silt fractions by mass; laser granulometry for particle-size distribution; HOC flag when texture not determinable.
- Data quality and provenance
  - Extensive metadata and column definitions accompany each dataset to ensure consistent interpretation and reproducibility.
  - Some samples may lack full depth data or measurements (ND), and some soils have no texture determination (HOC flag).

## Usage and relevance for environmental monitoring
- Enables standardized, time-consistent assessment of soil physical, chemical, isotopic, and texture properties across England, Scotland and Wales.
- Supports researchers and policymakers in evaluating carbon and nutrient stocks, soil health, and responses to land use or management changes.
- Facilitates integration with other LTLS data to model long-term biogeochemical cycles and interactions between soil, land, water, and atmosphere.

## Key considerations and caveats
- Depth coverage varied by site; not all cores reached 40 cm, and occasional exceedances beyond 40 cm occurred.
- Texture determinations may be unavailable for some samples (HOC flagged).
- Some fields are ND (not determined) or rely on indirect classifications (NSI, MODERN_DEF) that depend on external classifications and sources.
- Data are organized as interrelated datasets requiring careful cross-referencing via Sample_ID, Site_code, and related identifiers.

## Access and provenance
- Datasets are compiled under Toberman et al. within the LTLS framework, intended for long-term monitoring and analysis of carbon, nitrogen, and phosphorus cycles in UK soils.
- Metadata and data dictionaries are provided to support data reuse and integration with other environmental monitoring data platforms.