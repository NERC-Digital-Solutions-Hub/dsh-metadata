# Supporting documentation for the dataset Soil survey in England, Scotland and Wales carried out during 2013 and 2014, 2016, Toberman et al.

## Overview
- Dataset documentation for a soil survey conducted in England, Scotland and Wales during 2013 and 2014 (with related work in 2016) as part of the NERC Macronutrient Cycles LTLS project.
- LTLS aims to analyse and simulate long-term and large-scale carbon, nitrogen and phosphorus interactions in UK land, freshwater and atmosphere.
- Contains field sampling methods, extensive data dictionaries, and multiple data tables describing soil properties, chemistry, isotopes, vegetation and site metadata.

## Sampling method and field procedures
- Sampling area: at each site, soil cores collected from within a ~100 x 100 m area.
- Site layout: a central line with regular points spaced 11 m apart (for 10 cores) or 16 m apart (for 6 cores).
- Core selection: individual coring sites chosen at random distances from line points.
- Core counts: typically 10 cores for semi-natural habitats; 6 or 10 cores for agricultural fields.
- Core extraction: vegetation and loose litter removed; van Walt split corer used (Ribble sites sampled by driving the core to depth and splitting; others by driving to 15 cm then sampling deeper layers).
- Depths: up to 40 cm in some cores; in others, not all 40 cm could be sampled.
- Documentation available: depths sampled are described in the data sheet “Soil cores and depths.”

## Data structure and content
- The dataset is described through structured tables with standardized column headings, explanations, units, measurement methods, and notes.
- Key tables and example fields:
  - Locations_and_dates: Sample_ID, Catchment, site_name, OS_Grid_ref, Easting, Northing, Latitude, Longitude, Sampling_date.
  - Site_vegetation_data: Habitat_type, Habitat_type_with_detail, Vegetation; Site metadata includes Catchment.
  - Soil_cores_and_depth: Depth (shallow/deep), number of cores, mean_thickness_cm.
  - Soil_texture_data: Sample, Clay (%), Silt (%), with instrument detail and notes on high organic content (HOC).
  - Bulk_density_data: BD_T, BD_P, BD_F with definitions (bulk density by total, particulate, and fine fractions) and units (g cm-3); associated measurements include measured dry weight and core volume; methods include drying and muffle furnace procedures.
  - Soil_chemistry_and_isotope_data: thickness_cm; BD_T/BD_P/BD_F values; pH (glass electrode), C (% by mass), N (% by mass); P_tot_% (inorganic and organic fractions via Aqua regia/microwave digestion with ICP-OES or other methods); δ13C; 14C_pMC; and related measurement methods (Vario EL, ICP-OES, AMS, etc.).
  - Charcoal_and_coal_data: charcoal/coal content (% by mass), LOI, micrscopic charcoal assessment, and related fractions.
  - Radiocarbon_codes: SUERC code linking to NERC Radiocarbon Facility results.
  - Soil_classifications_England_and_Wales: NSI classification data (NSI_series, NSI_Subgroup, NSI_classification, etc.) and associated NSI survey information.
  - Soil_classifications_Scotland: site codes and associated 250K/25K soil map classifications from James Hutton Institute.
- Data quality fields include notes like ND (not determined) and NA (not available) where applicable.

## Data quality, provenance, and processing
- Provenance: data are field-derived soil measurements tied to particular sites, vegetation, and catchments; linked datasets support multi-parameter soil characterization.
- Processing: explicit protocols for sample processing and analysis (e.g., LOI by muffle furnace at 450°C for 16 hours; pH by glass electrode; elemental analysis by Vario EL; carbonates removed with HCl where appropriate; ICP-OES analyses after Aqua regia digestion).
- Metadata completeness: comprehensive data dictionaries outline column headings, explanations, units, measurements, and notes, enabling reproducibility and cross-dataset integration.
- Data quality considerations: some cores did not reach intended depths; occasional missing measurements (ND/NA); multiple formats and platforms used across properties and sites may impact interoperability.
- Documentation: explicit record of field methods, depths, sampling dates, and site-level context to support auditability and traceability.

## Data governance, access, and sharing
- Dataset is accompanied by detailed metadata and data dictionaries (including column-level explanations, units, and measurement methods).
- Sharing considerations: the documentation references “sharing limitations” and the existence of portal/catalogue uploads for dataset distribution.
- Updates and versioning: data are tied to ongoing LTLS project outputs; documentation implies updates and ongoing governance to reflect data availability and corrections.
- Embargoes and access: explicit embargo details are not provided in the text; governance reflects potential limitations on data sharing and license terms through project or institutional policies.

## Key datasets and data dictionary highlights
- Soil core and depth information: depth, number of cores, mean core thickness, and sampling details.
- Geographic and site metadata: OS grid references, Easting/Northing, latitude/longitude, catchments, site names, and sampling dates.
- Physical properties: bulk density (BD_T, BD_P, BD_F) with respective definitions and measurement methods; LOI data.
- Soil chemistry and isotopes: pH, carbon content (C), nitrogen content (N), total phosphorus (P_tot_% with inorganic and organic fractions), delta13C, pMC (percent modern), and related analytical methods (ICP-OES, Vario EL, AMS).
- Carbon and charcoal fractions: charcoal/coal content, LOI, and charcoal fraction relative to LOI.
- Soil texture: clay and silt fractions, percent clay/silt by mass; instrument used for texture analysis; notes on high organic content (HOC).
- Classifications and maps: NSI-based classifications (England & Wales) and Scottish soil map classifications with associated sources (NSI classifications, James Hutton Institute maps).
- Vegetation and habitat context: habitat types and vegetation descriptors at sampling sites.

## Challenges and considerations for Data Stewards
- Incomplete or evolving user needs may require ongoing metadata enhancement to improve discoverability and reuse.
- Timeliness of data delivery from collaborating data creators; ensure follow-up processes to obtain missing or incomplete metadata.
- Standardization across diverse datasets and formats; maintain consistent units, terminology, and controlled vocabularies where possible.
- Interoperability across systems and legacy formats; consider mapping to common schemas and ontologies for easier integration.
- Handling large datasets and depth limitations; document any bespoke handling approaches and provide guidance for data users.
- Governance practices: enforce data sharing limitations, embargo policies, and update workflows; ensure datasets are uploaded to appropriate portals and catalogues with complete documentation.

## Project context and references
- Part of the NERC Macronutrient Cycles LTLS project: LTLS – Analysing and simulating long-term and large-scale interactions of carbon, nitrogen and phosphorus in UK land, freshwater and atmosphere.
- Documentation supports data discovery, reuse, and governance by providing structured metadata, detailed field methods, and comprehensive data dictionaries across multiple related tables.