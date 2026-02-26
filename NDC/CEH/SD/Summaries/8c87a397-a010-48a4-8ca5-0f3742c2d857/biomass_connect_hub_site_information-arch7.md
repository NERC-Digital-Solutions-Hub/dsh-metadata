# Biomass Information and Innovation Platform Hub Site Background Information

## Summary
- Biomass Connect created a UK-wide platform to overcome barriers to large-scale domestic biomass supply by providing robust, independent information on feedstock performance, agronomy, economics and environmental benefits for landowners and managers.
- Objectives include evaluating geographic variations in biomass feedstocks, sharing knowledge and case studies, and contributing to agricultural, environmental and bioenergy policy.
- The project established eight Hub sites (up to 5 ha each) with demonstration plots (up to 11 species) and variety trials for willow, Miscanthus, and other energy grasses to enable multi-site UK-wide comparisons of biomass performance.
- The document outlines background information on site selection, establishment, and associated GIS-ready data components.

## Hub Site Network
- Site selection criteria focused on:
  - I) Biomass cultivation capacity
  - II) Monitoring infrastructure
  - III) Stakeholder engagement capability
- Eight Hub sites across the UK: Aberystwyth (ABR), Auchencruive (AUC), Bio Global Industries (BGI), Boghall Farm (BHF), Cockle Park Farm (CPF), Headley Hall (HHL), Hillsborough (HLS), North Wyke (NWK).
- Geographic distribution chosen to capture climatic variation and provide regional reach to biomass growers.
- Site data include precise coordinates (Easting/Northing, and elevations; some entries use Irish Grid for HLS), ownership, and field names.
- Land-use context: some sites are long-term arable, others grassland; nearby biomass plantings and agroforestry/intercropping activities exist at several sites.
- Environmental context includes Landscape Character classifications and designations (one site within an Area of Outstanding Natural Beauty), plus desk-based Environmental Impact Assessments and nitrate vulnerability considerations.

## Soils Overview
- Eight Hub sites dispersed across the UK with soils characterized using:
  - World Reference Base (WRB) soil classification
  - ESB Subsoil description (1:50k scale)
  - Modelled Soil Moisture Regime (SMR)
  - Modelled Soil Nutrient Regime (SNR)
- Acknowledges possible mismatches between broad national models and local soil conditions; field assessments will update site-specific soil data.
- Example soil characterizations per site include WRB type, subsoil description, SMR and SNR values (e.g., Stagnosol or Cambisol WRB, various SMR/SNR codes) to inform site planning and crop suitability.

## Climate Overview
- Regional climate profiles compiled from long-term data (1991–2020) from the nearest Met Office stations for each Hub site.
- Reported metrics include: max/min temperatures, frost days, sunshine hours, annual rainfall, days with rainfall >1 mm, and wind speed.
- Some sites show missing data in certain metrics (e.g., wind data or sunny hours).
- Existing climate monitoring infrastructure is linked to each site with nearest Met station details.

## Field Plots Overview
- Each Hub site includes diverse field plots to evaluate biomass crops:
  - Two demonstration blocks of Miscanthus giganteus (MISg) and Miscanthus Athena (MISa) and one SRC willow block (0.40–0.50 ha)
  - Three smaller demonstration blocks of SRC poplar (POP), SRF poplar, and SRF Eucalyptus (each ~0.10–0.16 ha)
  - A plot with perennial grasses (e.g., Reed Canary Grass, Switchgrass, Arundo; ~0.025 ha)
  - A plot with SRF species (e.g., Alder, Paulownia, Black Locust; ~0.031 ha)
  - Five sites include variety trials for SRC willow, Miscanthus, and energy grasses
  - A designated Reference area representing ongoing pre-existing land use
- Plot designs include consideration of shading: tall crops placed to the north, with headlands and internal aisles planned accordingly.

## Site Plot Maps
- Plot maps are generated for all eight Hub sites after field design into shapefiles and GIS-ready formats.

## Crops Overview
- Each Hub site hosts up to 11 species across demonstration blocks and plots.
- Crop types include:
  - Willows (SRC), Poplars (SRC/SRF), Eucalyptus, Alder, Black Locust
  - Miscanthus giganteus, Miscanthus Athena
  - Perennial grasses: Reed Canary Grass, Switch Grass, Arundo, Sida (as forbs)
- Planting densities, spacings, and target dates are specified; Miscanthus and SRC willow have dedicated variety trials (e.g., 6 near-commercial hybrids plus controls; 36 willow genotypes).
- Variety trials include additional test varieties from external projects (e.g., University of Surrey Lot 1).

## Instrumentation
- 8.1 Automatic Weather Stations (AWS)
  - Installed at each Hub site to capture rainfall, air temperature, humidity, wind speed/direction
  - Data downloaded monthly; installation occurred in May–June 2023
- 8.2 Ground sensors
  - TOMST TMS-4 dataloggers deployed at the same locations as AWS
  - Measure soil moisture and temperature at 6 cm, plus air temperatures at 2 cm and 15 cm height
  - Installed May–June 2023

## GIS and Data Considerations (Key Points for GIS Specialists)
- Data integration: Shapefiles created from field surveys (Trimble Geo7x, WGS84) exported via Trimble Pathfinder, then imported into Pear GIS PT Mapper and later into QGIS for map production.
- Coordinate systems: Precise site coordinates provided (E/N; some entries use Irish Grid for NI site).
- Plot design consistency: Standard headland width (12 m) and internal aisle planning to ensure consistent GIS mapping across sites.
- Data types: Site boundary geometries, plots, crop blocks, variety trial layouts, environmental designations, and landscape classifications are all GIS-relevant layers.
- Data quality and updates: Soil data will be updated post-field assessments to reflect local conditions; climate data linked to Met Office stations may have gaps in some sites.
- Accessibility: Hub Site Network-2 and related tables consolidate locational, land-use, and landscape designation data suitable for GIS cataloging and mapping.
- Environmental context: AONB and nitrate vulnerability maps are incorporated into site environmental assessments, informing restricted or sensitive mapping layers.
- Deliverables: Site-level plot maps, crop layout schemas, and associated GIS-ready shapefiles to enable cross-site comparisons and policy/research visualization.

## References and Sources
- Landscapes and reference materials include national character area profiles and landscape assessments for England, Wales, Scotland, and Northern Ireland, used to contextualize site locations and environmental designations.