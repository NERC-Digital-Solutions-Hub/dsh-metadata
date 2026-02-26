# Elemental meta-data

## Overview
- Defines the elemental data accompanying plant or soil samples analyzed by CEH laboratories.
- Focuses on identifiers, sampling context, taxonomic information, and a comprehensive set of elemental concentration measurements.
- Measurements are produced using ICPMS and ICPOES, with distinctions between quantitative and semi-quantitative data and detection limits.

## Key data fields (sample-level identifiers and context)
- Laboratory_ID: CEH centralised chemistry laboratory unique sample identifier.
- Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
- Collection_Site: Sampling site.
- Sampling_date: Date plant species or soil was sampled (dd/mm/yyyy).
- Species: Latin name of the plant species (n/a if soil sample).
- Common_name: Common name of the plant species (n/a if soil sample or no common name).
- Taxonomy: Order, Family, Genus (n/a if not applicable).

## Element concentration data (measurement details)
- Numerous element-specific columns (e.g., Li_, Be_, Na_, Mg_, Al_, Si_, K_, Ca_, Fe_, Cu_, Zn_, Se_, Pb_, U_, etc.) representing concentrations.
- Columns vary by measurement type and unit:
  - Quantitative measurements (e.g., mg per kg, mg/kg dry weight; some columns specify dry weight vs fresh weight).
  - Semi-quantitative measurements (e.g., mg/kg, sometimes specified as semi-quantitative by method).
  - Some measurements labeled as “per kg dry weight” or “mg per kg dry weight”; others indicate “mg per kg” or similar.
- Measurement methods:
  - ICPMS: Inductively Coupled Plasma Mass Spectrometry (quantitative and semi-quantitative data across elements).
  - ICPOES: Inductively Coupled Plasma Optical Emission Spectrometry (quantitative and semi-quantitative data across elements).
- Data quality indicators:
  - “<” in a column indicates the concentration is below the limit of detection (LOD) for that sample/element.
  - “n/a” indicates data not available for that column.
- Column naming conventions are diverse (e.g., Li_mg_kg_quantitative_mg_kg_dry, Be_<, Na_ICPOES_mg_kg_quantitative_m_g_kg_dry, etc.), reflecting different measurement types and units.

## Spatial and GIS readiness
- Collection_Site provides spatial context for mapping, enabling point-based GIS representations.
- Each record includes sampling date and taxonomic context (Species, Common_name, Genus, Family, Order), supporting layered thematic maps by species or taxa.
- Element concentration attributes can be visualized as:
  - Single-element maps (e.g., distribution of a specific element).
  - Multivariate maps or heatmaps (across several elements).
  - Temporal maps by mapping concentrations across sampling dates if time-series data exist.

## Data quality, standardization, and preprocessing considerations
- Data are drawn from multiple measurement methods and may require harmonization:
  - Unify units (e.g., all to mg/kg dry weight or all to mg/kg) for consistent comparison.
  - Resolve inconsistent column names and ensure consistent naming for GIS schemas.
- Handling below-LOD data:
  - Decide a policy (e.g., substitute with LOD/2, LOD/sqrt(2), or keep as a separate flag) for accurate GIS visualization.
- Missing data:
  - Manage “n/a” entries; determine whether to exclude records from certain maps or to display as missing data.
- Data packaging:
  - Large/complex datasets may need to be split into manageable chunks (e.g., by element groups, by measurement type, or by study site) for efficient GIS ingestion.
- Data provenance and metadata:
  - Maintain metadata on measurement method (ICPMS vs ICPOES), data type (quantitative vs semi-quantitative), and LOD handling for transparent GIS interpretation.

## Practical guidance for GIS specialists
- Data model recommendations:
  - Treat each sampling event as a point feature with attributes:
    - Collection_Site (and optional spatial coordinates or a site polygon link)
    - Sampling_date
    - Species / Common_name / Genus / Family / Order
    - For each element: concentration value, unit, data type (quantitative/semi-quantitative), method (ICPMS/ICPOES), and LOD indicator if applicable.
- Data preparation steps:
  - Normalize units to a single standard (e.g., mg/kg dry weight) where feasible.
  - Convert or flag LOD-related values consistently.
  - Resolve naming inconsistencies and derive a clean attribute schema suitable for GIS joins and queries.
- Visualization tips:
  - Use graduated symbols or choropleth/heatmap styles for single-element maps.
  - Create facet maps by element groups or by species to reveal patterns.
  - Combine spatial maps with taxonomic filters (e.g., by Genus or Species) for targeted analyses.
- Metadata and documentation:
  - Include measurement methods, LOD policies, data availability notes, and any data gaps in the GIS project metadata.

## Use cases and visualization ideas
- Environmental and ecological monitoring:
  - Map spatial distribution of trace elements in plant tissues across sites.
- Comparative studies:
  - Compare element profiles between species or taxonomic groups at different locations.
- Temporal analyses:
  - Track changes in concentrations over sampling dates if time-series data exist.
- Risk assessment and soil-plant interactions:
  - Identify hotspots of heavy metals or elements of interest and correlate with site characteristics.

## Challenges and recommendations
- Challenges:
  - Data scattered across multiple sources and formats.
  - Inconsistent data standards and units.
  - Large, complex datasets not readily packaged for GIS workflows.
  - Missing data and LOD handling complicate visualization and interpretation.
- Recommendations:
  - Develop a standardized GIS-ready schema with unified units and clear data-type flags.
  - Partition large datasets into manageable chunks for analysis and visualization.
  - Establish clear LOD handling rules and document them in metadata.
  - Maintain comprehensive metadata linking each record to measurement method and data quality notes.