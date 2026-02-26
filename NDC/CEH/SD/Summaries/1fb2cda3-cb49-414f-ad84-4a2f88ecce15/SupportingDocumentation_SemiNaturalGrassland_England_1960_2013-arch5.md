# Fate of semi-natural grassland in England between 1960 and 2013: a test of national conservation policy

## Overview
- Dataset created to quantify changes in semi-natural grassland in England from 1960 to 2013 by linking historic grassland surveys with contemporary habitat spatial data.
- Supports understanding of national conservation policy outcomes and dataset usability for researchers and policymakers.

## Data provenance and scope
- Source data: historic quadrat surveys conducted 1960–1981 at grassland sites in England; some data contributed to the Nature Conservation Review (1977).
- Sampling: at each site, vascular plant cover was recorded from 2–6 randomly placed 1m x 1m (mostly) quadrats; some sites used 2m x 2m quadrats.
- Locational accuracy: quadrat positions recorded to six-figure British National Grid with ±100 m spatial accuracy.
- Classification: quadrats assigned to British National Vegetation Classification (NVC) communities using TABLEFIT; quadrats further categorized into four grassland types (calcareous, lowland heath/dry acid, mesotrophic, wet) with BAP/priority habitat mappings.

## Data structure and metadata
- Core fields (example): Unique quadrat ID, survey date, Easting/Northing, grassland category, NVC group, sub-community, and a set of percentage cover metrics for surrounding landscape features within a 100 m buffer (e.g., coastal & floodplain habitats, woodlands, various grassland types, and other land cover).
- Derived metrics: percent of buffer classified as priority habitat and percent overlap with Site of Special Scientific Interest (SSSI) boundaries.
- Column headings are defined to support reproducibility and interoperability, including precise definitions for each percentage metric within the 100 m buffer around each quadrat.

## Analytic methods and processing
- Spatial workflow: quadrat locations imported into ESRI ArcGIS v10; a 100 m buffer created to reflect location accuracy and represent a grassland site context.
- Habitat comparison: used Natural England’s Priority Habitats Inventory (2013) to quantify the presence/extent of priority habitats within each buffer.
- SSSI overlap: intersected grassland site buffers with Natural England’s SSSI boundary data (2014) to determine SSSI coverage.
- Processing tools: tabulate intersection (Spatial Analyst) to compute percentages of habitat types within each buffer.

## Data quality, limitations, and governance considerations
- Strengths: standardized historic survey methodology; explicit spatial context via 100 m buffers; integration with authoritative habitat and protection boundary datasets; clear metadata for reproducibility.
- Limitations and considerations for stewardship:
  - Historic data have variable quadrat sizes (1 m x 1 m predominantly; some 2 m x 2 m) and spatial accuracy tied to older survey practices.
  - NVC classification relies on TABLEFIT and historical typologies; potential changes in classification schemes over time.
  - Uses contemporary layer inventories (Priority Habitats, SSSI) to contextualize historic sites; requires attention to changes in boundaries or classifications over time.
  - Data may require accompanying documentation of data lineage, transformations, and any updates to classifications or boundary datasets.
- Data stewardship implications:
  - Ensure dataset remains discoverable and properly catalogued; consider publishing alongside metadata and data processing scripts.
  - Document any assumptions, quality checks, and updates to habitat inventories or boundary layers.
  - Be explicit about sharing constraints, data availability, and any embargoes or access restrictions.

## Usage, sharing, and interoperability
- Aimed at facilitating reuse by researchers and conservation practitioners to assess grassland changes and policy effectiveness.
- Encourages uploading to appropriate data portals and thorough documentation of work performed on datasets to support reuse and traceability.

## References and standards
- TABLEFIT, Version 10 (Hill, 1996) for identifying vegetation types.
- Natural England Priority Habitats’ Inventory (2013) and SSSI boundary data (2014).
- Ratcliffe, D. (1977) Nature Conservation Review.
- Rodwell, J. S. (1992) British Plant Communities: Grasslands and Montane Communities.