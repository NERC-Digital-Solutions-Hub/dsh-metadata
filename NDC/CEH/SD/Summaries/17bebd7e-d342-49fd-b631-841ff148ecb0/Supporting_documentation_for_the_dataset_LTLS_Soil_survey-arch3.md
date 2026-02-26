# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

- Purpose and scope
  - Documentation for a soil survey across England, Scotland and Wales conducted in 2013–2014, with data linked to the LTLS project on long-term carbon, nitrogen, and phosphorus interactions in UK land, freshwater, and atmosphere.
  - Supports environmental health monitoring by providing standardized soil physical, chemical, isotopic, and texture measurements across multiple sites and habitats.

- Sampling design and collection
  - Sites cover approximately 100 x 100 m areas; a central line with sampling points spaced 11 m apart for 10 cores or 16 m for 6 cores.
  - At each site: 10 cores for semi-natural habitats; 6 (or sometimes 10) cores for agricultural fields.
  - Core collection methods vary: van Walt split corer or direct insertion; typical depth sampling to 40 cm (top 20 cm/next 20 cm in some protocols); some cases could not reach full 40 cm.
  - Habitat type abbreviations used (e.g., AG = Acid grassland, Ar = Arable, CG = Calcareous grassland, etc.) and notes on high organic content (HOC).

- Core depths and sampling details
  - Depths sampled and sampling dates recorded in the data sheets; some cores sampled to 15 cm, others to 40 cm, with occasional deviations.
  - Depth-related metadata include thickness and whether the layer sampled is surface or deeper soil (in isotope data).

- Data tables and key variables (structure)
  - Locations_and_dates: Sample_ID, catchment, site_name, OS_Grid_ref, Easting, Northing, Latitude, Longitude, Sampling_date.
  - Bulk_density_data: BD_T (bulk density total), BD_P (bulk density mineral matter), BD_F (bulk density LOI-related), plus corresponding measured dry weights and core volumes.
  - Charcoal_and_coal_data: charcoal/coal content (% by mass), LOI, charcoal fraction of LOI, and related measurements (e.g., kiln/oxidation methods).
  - Radiocarbon_codes: SUERC code linking to radiocarbon measurements for samples.
  - Site_vegetation_data: Habitat_type, Habitat_type_with_detail, Vegetation descriptors.
  - Soil_chemistry_and_isotope_data: thickness_cm; pH; C_tot_% (total carbon), N_tot_% (total nitrogen); P_tot_% (total phosphorus, including inorganic and organic fractions), delta13C; 14C_pMC; isotopic and elemental measurements performed via ICP-OES and AMS, with digestion methods noted.
  - Soil_classifications_England_and_Wales: NSI classifications, NSI_series, NSI_Subgroup, NSI_brief, and related NSI survey information.
  - Soil_classifications_Scotland: Site_code and associations to 250K/25K soil maps, dominant soil map units, and available 25K map series data; associated with James Hutton Institute.
  - Soil_cores_and_depth: Depth category (shallow/deep), number of cores, mean thickness (cm).
  - Soil_texture_data: Clay and Silt fractions (% by mass) with laser granulometry method (Beckman Coulter LS200); HOC note for high organic content where texture not determined.

- Measured properties and methods
  - Physical: Bulk density measurements (BD_T, BD_P, BD_F) with core-volume-based calculations.
  - Chemical and isotopic: pH (glass electrode), carbon and nitrogen contents, total and inorganic phosphorus (and organic P by difference), delta13C, 14C-based pMC; P measured via Aqua regia digestion with ICP-OES.
  - Organic matter and charcoal: LOI (loss on ignition) and charcoal content as a fraction of LOI.
  - Isotopes and radiocarbon: Radiocarbon codes linked to SUERC facility; delta13C and 14C-based indicators.
  - Texture: Clay and Silt percentages derived from laser granulometry; notes on high organic content where texture was not determined.

- Data quality, metadata, and governance
  - Extensive field and lab metadata per data table (column headings, explanations, units, measurement methods, and notes).
  - Clear sample identifiers, site codes, and geographic coordinates to enable data linkage and cross-site comparisons.
  - Method descriptions for core sampling, processing, and analyses to support reproducibility and auditability.
  - Some ND/not available values indicated; depth and thickness fields provide essential QA context for interpretation.

- Relevance for monitoring frameworks
  - Provides a standardized, multi-parameter soil health dataset across UK regions suitable for assessing carbon storage, nutrient status, and soil physical properties.
  - Enables cross-site trend analyses and policy evaluation related to soil quality, land management, and nutrient cycling.
  - Rich metadata and standardized classifications (NSI) facilitate integration with national soil resources information and habitat classifications.
  - Supports long-term environmental monitoring with explicit sampling designs, measurement protocols, and data governance considerations.

- Limitations and considerations for use
  - Depth coverage sometimes limited by field constraints; not all samples reach the full 40 cm depth in every instance.
  - Some texture determinations labeled as HOC or not determined in certain samples; ND values exist for some fields.
  - Regional classifications and mappings may require alignment with current NSI schemes or map updates for time-series analyses.

- Bottom line
  - The documentation outlines a comprehensive, well-structured soil survey dataset (2013–2014, with 2016 reference) that underpins environmental health monitoring and policy evaluation through standardized measurements of soil physical, chemical, isotopic, and texture properties across the UK, with robust metadata and governance to support data sharing and comparability.