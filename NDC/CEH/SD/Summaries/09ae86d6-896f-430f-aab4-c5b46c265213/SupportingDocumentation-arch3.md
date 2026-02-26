# Stable isotope values for 108 water samples collected in the Gandak River Basin, in Bihar, India

## Overview
- Dataset presents stable isotope values (d18O and dD) for 108 water samples from the Gandak River Basin, Bihar, India, plus specific electrical conductivity (SEC) for most samples.
- Sample types include surface water, groundwater, and rainfall; collected between February 2017 and February 2019.
- Sampling sources span rivers, boreholes/wells (groundwater), canals, and rainfall collectors; many groundwater samples come from boreholes or wells in regular daily use.
- Sampling was unfiltered, bottled at source, and SEC measured on-site; stable isotopes analyzed at British Geological Survey laboratories (UK).
- Data collected as part of the CHANSE (Coupled Human And Natural Systems Environment) project.
- Data interpretation relies on linking isotopic signatures with water sources and hydrological processes; requires clear metadata and traceability.

## Data structure and variables
- Core measurements:
  - Sample date (sample_date)
  - d18O VSMOW2 (‰): Oxygen-18 isotope ratio relative to VSMOW
  - dD VSMOW2 (‰): Deuterium isotope ratio relative to VSMOW
  - SEC (uS/cm): Specific electrical conductivity
- Dataset organization references to BGS LIMS or lab codes for samples
- Missing values are recorded as blank
- Variable descriptions indicate standard units and the relative per mil reporting basis for isotopes; samples were analyzed in a centralized lab (BGS)

## Site locations and sampling notes
- Entries use a broad set of sample IDs (e.g., 13965-0001 to 1A, 2A, etc.) with:
  - sample_date (dates spanning 2017–2019)
  - source_type (River Gandak, groundwater boreholes/wells, canals, rainfall, etc.)
  - source_water_type (Groundwater, River Gandak, Canal, Rainwater)
  - geographic coordinates (lat, long) and, where available, surface_elevation (mOD)
  - source_use (domestic, irrigation, temple, hotel, etc.)
  - source_depth (depth to water table or well depth; many entries show depths in meters)
  - Notes capturing sampling context (pump conditions, proximity to canals, well age, presence of bubbles, taste comments, etc.)
- Many sites provide rich contextual details (pump timing, canal interactions, nearby water uses). Some entries contain incomplete fields or inconsistent formatting, reflecting variable metadata completeness across sites.

## Data quality, governance and accessibility considerations
- Data integrity relies on consistent metadata, precise geolocation, and standardized unit conventions; the dataset shows substantial heterogeneity in fields (depths, elevations, notes) across entries.
- Data governance challenges highlighted by monitoring-framework literature include data sharing barriers, metadata sufficiency, and data standardization; this dataset demonstrates:
  - The need for robust metadata (e.g., standardized source_type, source_use, and depth descriptors)
  - Clear provenance and data lineage (origin of isotopic analyses and field measurements)
  - Openness and accessibility (public sharing of underlying data and metadata)
  - Metadata curation to reduce silos and ensure interoperability across datasets

## Relevance for monitoring frameworks and policy decisions
- Strengths for policy-relevant monitoring:
  - Provides baseline isotopic signatures to distinguish groundwater vs. surface water sources and to infer infiltration and mixing processes
  - Coupled isotopic data with SEC offers insights into water quality and salinity-related processes
  - Temporal span (2017–2019) enables assessment of hydrological changes and potential impacts of irrigation practices
- Potential policy applications:
  - Groundwater sustainability and aquifer management decisions
  - Water resource planning in mixed-use landscapes (domestic, agricultural, industrial)
  - Evaluation of river-aquifer interactions and child policies around canal water use and groundwater pumping
- Limitations for decision-making:
  - Incomplete or inconsistent metadata across sites may hinder rapid cross-site comparability
  - Requires standardized reporting to maximize usability in multi-dataset monitoring frameworks

## Recommendations for monitoring-framework authors
- Data standardization
  - Adopt uniform metadata templates (minimum fields: sample_id, sample_date, source_type, source_water_type, lat, long, depth, elevation, source_use, notes)
  - Harmonize units and nomenclature for isotopic measurements and conductivity
- Metadata quality and completeness
  - Ensure complete field coverage or clearly annotate missingness; provide controlled vocabularies for source_type and source_use
- Data provenance and governance
  - Document data provenance (sampling methods, lab analysis, quality control steps)
  - Establish data-sharing policies and open-access licenses; provide machine-readable metadata (e.g., XML/JSON, Dublin Core)
- Data usability and accessibility
  - Create centralized, queryable dashboards or repositories linking isotope data with site metadata
  - Include data quality indicators and transformation steps (calibrations, corrections) in the metadata
- Future enhancements
  - Add temporal coverage to assess trend and seasonal variability
  - Integrate with complementary water-quality parameters to strengthen interpretability for policy analysis

## Conclusion
- The dataset offers valuable isotopic and conductivity measurements across a diverse set of water sources in the Gandak River Basin, with rich site-specific context. It supports monitoring and policy analysis related to water resource management, groundwater-surface water interactions, and irrigation impacts. To maximize utility for monitoring frameworks, emphasis should be placed on standardized, complete metadata, transparent data provenance, and open, interoperable data sharing.