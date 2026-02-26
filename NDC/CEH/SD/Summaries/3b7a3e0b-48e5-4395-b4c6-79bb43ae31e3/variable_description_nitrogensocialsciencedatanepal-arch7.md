# DESCRIPTION: The data was collected primarily to assess differences in nitrogen use efficiency (NUE) and sustainable nitrogen practices between households.

## Overview of the dataset and aims
- Captures differences in NUE and sustainable nitrogen practices across farming households.
- Also includes households’ attitudes, information sources, decision-making, and adoption drivers/barriers related to NUE in crop production.
- Part of SANH WP 1.3 Harmonised Household Survey across multiple South Asian countries (Bangladesh, India, Maldives, Pakistan, Sri Lanka).
- Data are cross-sectional with two seasonal observations, featuring extensive variable descriptions and season-specific plot and crop modules.

## Geographic scope and data structure
- Geographic identifiers: COUNTRY, STATE/PROVINCE, DISTRICT, VILLAGE to enable spatial analysis.
- Core structure: Household-level data linked to multiple plots and seasons; rich per-plot and per-season agronomic details (crops, soil, slope, area, tenure).
- Spatially-enabled design intended for integration with GIS layers (e.g., soils, irrigation networks, administrative boundaries).

## GIS-relevant data domains and variables (representative)
- Spatial and administrative geography
  - COUNTRY, STATE/PROVINCE, DISTRICT, VILLAGE
- Household and demographics (contextual for mapping socio-economic layers)
- Plot-level and season-level characteristics
  - Plot code, area/size, tenure, distance to homestead, slope, soil type
  - Crop codes per season, target crops, rotation, and season alignment
- Labor, wages, and mechanization (key for spatial labor intensity mapping)
  - Labor hours by activity (land preparation, seed/seedling, weeding, planting, fertilizing, transplanting, water management, harvesting, others) across seasons S11–S26
  - Worker types: HOUSEHOLD MEMBERS (HM) and HIRED LABOUR (HL); counts of males/females per season
  - Average wages by activity and season; total labor costs
  - Mechanization levels for land preparation, seed sowing, fertilizer application, irrigation, harvest (fully mechanized, partially, fully manual)
  - Costs associated with land preparation and machinery usage
- Inputs, inputs management, and subsidies
  - Synthetic fertilizers, organic fertilizers, seeds; sources, quantities, units, timing
  - Pesticide use (types, frequency, costs) and IPM adoption
- Irrigation, water management, and costs
  - Source of irrigation water; pricing mechanisms; water used by crop; season-specific values
  - Water management practices for rice (e.g., flooding, drainage, alternate wetting and drying)
- Decision support and information access
  - Use of agro-guides, leaf colour charts, manure/fertilizer decision processes, and training/demonstrations
- Household assets and broader socio-economic indicators (for GIS layering)
  - Ownership of land, dwellings, assets, expenditures, access to services, and connectivity (internet, mobile)

## Data quality, standards, and GIS preparation needs
- Standardization
  - Harmonize crop codes, tenure statuses, unit definitions across countries and seasons
  - Align seasonal naming and repeated-section structures to enable seamless joins
- Data cleansing
  - Validate and deduplicate household and plot records; reconcile missing/inconsistent entries
  - Geospatial validation: verify geographic fields against boundaries; geocode plots using coordinates or village centroids if needed
- Geospatial readiness
  - Build a clean relational schema: households, individuals, plots, plots_by_season, crops, inputs, subsidies, information sources
  - Establish privacy controls and anonymization as needed for geospatial outputs
- Privacy and governance
  - Map outputs at appropriate aggregation levels to protect privacy; document access controls

## GIS-ready outputs and visualization ideas
- Spatial distributions and map products
  - NUE indicators by district/municipality/village (choropleth)
  - Fertilizer usage patterns (synthetic vs organic) by region and season
  - Adoption/subsidy hotspots and information source reach
  - Crop diversity and target crops across space with seasonal overlays
  - Soil type, slope, and irrigation features overlaid with cropping patterns
- Plot- and farm-level visualizations
  - Interactive maps showing plot area, tenure, distance to homestead, slope alongside NUE metrics
  - Temporal exploration across two seasons to observe changes in inputs and outcomes
- Ancillary integrations
  - Overlay with administrative boundaries, soil maps, climate/irrigation data, infrastructure
  - Linking plot data to raster/vector GIS layers for risk/suitability analyses

## Practical GIS implementation guidance
- Data modeling and pipeline
  - Design a robust relational schema separating households, plots, and season-level crop/inputs data to enable efficient GIS joins
  - Normalize and standardize codes, units, and tenure statuses; ensure consistent field naming across seasons
- Geospatial baselines
  - Establish village boundaries as baselines; geolocate plots via collected coordinates or village centroids
- Metadata and documentation
  - Produce a comprehensive data dictionary; document geocoding, joins, and validation rules; track data provenance and versioning
- GIS ingestion and visualization workflow
  - Ingest raw data, normalize/clean, geocode, join with GIS layers, produce initial NUE maps, then refine with richer plot-level attributes
- Privacy-first distribution
  - Aggregate outputs for public sharing; apply anonymization where required; maintain access controls

## Challenges and limitations to anticipate
- Fragmented data across sections and seasons requiring careful integration
- Cross-country standardization gaps (codes, units, tenure terms)
- Data quality issues due to large, complex datasets and potential missing values
- Geographic precision limitations if plot coordinates are unavailable
- Capacity needs for advanced data wrangling, schema design, and GIS integration

## Takeaways for GIS-focused data product development
- Build a scalable, GIS-friendly relational data model connecting households, plots, and seasons
- Establish clear geospatial baselines and robust geocoding strategies
- Create standardized dictionaries and validation rules before GIS integration
- Implement an incremental GIS pipeline to generate NUE and related spatial visualizations
- Prioritize privacy in mapping through aggregation and controlled access
- Leverage the rich labor, mechanization, irrigation, and input data to produce nuanced spatial analyses of NUE, adoption patterns, and resource use across space and time