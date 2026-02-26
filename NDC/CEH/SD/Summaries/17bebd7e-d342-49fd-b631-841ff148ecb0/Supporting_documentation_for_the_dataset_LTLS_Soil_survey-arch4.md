# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

## Overview
- Describes the soil survey data collected in England, Scotland and Wales during 2013–2014 (with 2016 reference) as part of the NERC Macronutrient Cycles LTLS project, focusing on carbon, nitrogen, and phosphorus dynamics in UK soils.
- Provides a comprehensive data dictionary and data processing protocol to support long-term ecological modelling and cross-site analyses.

## Sampling and collection details
- Site sampling framework: 100 m x 100 m areas with a central line; sampling points spaced at 11 m (10 cores) or 16 m (6 cores), with cores chosen at random distances from line.
- Core allocation: 10 cores for semi-natural habitats; 6 (sometimes 10) cores for agricultural fields.
- Core extraction: vegetation and loose litter removed; depth protocols differ by location:
  - Ribble: top 20 cm sampled first, then next 20 cm.
  - Other sites: sampled to a depth of 15 cm per iteration, with multiple iterations up to 40 cm total; in some cases the full 40 cm could not be sampled.
- Depths, locations, and sampling dates are tracked across multiple data tables.

## Data structure and content
- The dataset is organized into multiple interrelated data tables, each with explicit column headings, explanations, units, and notes. Key tables include:
  - Locations_and_dates: Sample_ID, site_name, Catchment, OS_Grid_ref, Easting, Northing, Latitude, Longitude, Sampling_date.
  - Site_vegetation_data: Habitat_type, Habitat_type_with_detail, Vegetation.
  - Soil_cores_and_depth: Depth, number_of_cores, mean_thickness_cm.
  - Soil_texture_data: Clay, Silt, %clay, %silt, measurement instrument (Beckman Coulter LS200), HOC (high organic content) flag.
  - Bulk_density_data: BD_T (total), BD_P (solids <2 mm), BD_F (solids <2 mm accounting for >2 mm solids), with corresponding units and core volume.
  - Charcoal_and_coal_data: charcoal/coal content by mass (%), LOI, microscopy-based charcoal fraction, and related measurements.
  - Radiocarbon_codes: SUERC code linking to NERC Radiocarbon Facility.
  - Site_vegetation_data: additional vegetation descriptors and site Catchment linkage.
  - Soil_chemistry_and_isotope_data: thickness_cm; BD_T, BD_P, BD_F; pH; C_%, N_%; P_tot_% (inorganic and organic fractions); delta13C; 14C_pMC; P_tot_% via inorganic/organic fractions; methods include Aqua regia digestion, ICP-OES, Vario EL, AMS, LOI; pre-treatment steps (e.g., carbonate removal with HCl) where applicable.
  - Soil_classifications_England_and_Wales: NSI (National Soil Resources Institute) classifications (series, subgroup, brief, MODERN_DEF); includes NSI metadata.
  - Soil_classifications_Scotland: Site_code; association and map unit data; dominant soil map units; available 25K scale data.
  - Soil_cores_and_depth: Depth of core, number of cores, mean thickness (cm).
  - Soil_texture_data: detailed texture components per sample (clay, silt fractions) with measurement method.
- Data fields are defined with explicit units (e.g., g cm-3 for density, cm for depth, % by mass for constituents, mm for thickness).

## Laboratory methods and data processing
- Laboratory procedures are specified for soil chemistry and isotope measurements:
  - pH: measured with glass electrode in moist soil with water (pH determinations).
  - Carbonates: treated with HCl prior to certain analyses.
  - Total/organic phosphorus and inorganic phosphorus: Aqua regia or microwave digestion with ICP-OES; P_org/ P_inorg fractions computed via difference.
  - Carbon and nitrogen: Vario EL elemental analyzer; delta13C measurements.
  - 14C content: AMS measurements (pMC).
  - LOI: Loss on ignition via muffle furnace at 450°C for 16 hours.
- Data may include entries like < LOD (below detection limit) or ND (not determined) for certain measurements.
- Texture analysis uses Beckman Coulter LS200 laser granulometer; notes about high organic content (HOC) affecting texture determination.

## Data quality, provenance, and metadata
- Extensive metadata accompany each data field, enabling traceability from sample to measurement method.
- Some data gaps or limitations noted:
  - Depth sampling sometimes incomplete; not all cores reach 40 cm.
  - ND or < LOD values present for some chemical/isotope measurements.
  - Regional classifications require cross-walking between NSI (England and Wales) and Scotland classifications.
- Regional data governance includes distinct classification systems and datasets across England, Wales, and Scotland, with links to NSI and James Hutton Institute classification schemes.

## Classifications and regional differences
- England and Wales: NSI-based soil classifications with fields NSI_series, NSI_Subgroup, NSI_brief, MODERN_DEF.
- Scotland: Site_code and associations to 250K soil map units; dominance of 25K map units and related classifications.
- The dataset supports cross-region analyses but may require harmonization of classification schemes for integrated use.

## Data access, reuse, and governance considerations
- The document serves as a comprehensive data dictionary and protocol for reuse in research and modelling.
- For data leaders, priority considerations include:
  - Implementing a unified data model to link Sample_ID across all tables (Locations, vegetation, cores, chemistry, isotopes, texture, classifications).
  - Ensuring metadata completeness and consistency across regions (England, Wales, Scotland) and datasets.
  - Establishing data quality checks, documenting LOD/ND cases, and clearly flagging incomplete depth coverage.
  - Harmonizing soil classifications across NSI and Scottish classifications to enable cross-regional analyses.
  - Maintaining clear provenance: sampling methods, lab methods, dates, and instrument details to support reproducibility.
  - Enhancing discoverability and potential data sharing within the wider scientific community (persistent identifiers, standardized schemas).

## Key takeaways for Data Leaders
- The soil survey dataset is a richly documented, multi-table data resource with detailed sampling protocols, lab methods, and region-specific classifications.
- It supports integrated analyses of soil physical properties, chemical/phosphorus and carbon/nitrogen metrics, and isotopic data, across England, Wales, and Scotland.
- The primary opportunities and risks for data strategy include: harmonizing classifications, linking across tables via Sample_ID, ensuring data quality and completeness, and improving data discoverability and governance to support reuse in policy and research contexts.