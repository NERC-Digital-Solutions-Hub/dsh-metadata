# Ecosystem services variables from the UK Environmental Change Network (ECN)

## Overview and aim
- Describes the ECN, the UK’s long-term environmental monitoring and research programme that measures air, soil, water, and a range of fauna and flora across multiple sites to track environmental change.
- Uses a Millennium Ecosystem Assessment (MA) framework to define and identify ecosystem services and corresponding variables.
- Provides standardized ecosystem services variables for cross-site and long-term monitoring, enabling assessment of environmental health and policy performance over time.
- Data are intended to be reusable, comparable, and stored in appropriate data portals.

## The Environmental Change Network
- ECN conducts regular measurements across a network of sites to understand how and why the natural environment is changing.
- MA (2005) is used as the theoretical framework to define ecosystem services and select proxy/variable definitions.
- Dataset creation involved standardizing definitions and ensuring comparability across sites and time.

## Site selection and boundaries
- Eleven ECN sites were selected for this dataset.
- Boundary definition focuses on biogeophysical features and social discontinuities, with land ownership and land management boundaries guiding data collection and analysis; boundaries were aligned with human decision-making scales (MA, 2005).
- Land ownership and land management boundaries coincide with ECN site boundaries at several sites; some sites are embedded within a larger management unit (e.g., a whole farm), and three sites include entire water basins.
- Site details (area in hectares): Alice Holt (ALI) 850; Cairngorm (CAI) 1000; Drayton (DRA) 200; Glensaugh (GLE) 1125; Moor House (MOO) 3500; North Wyke (NOR) 248; Porton Down (POR) 1564; Rothamsted (ROT) 341; Snowdon (SNO) 544; Sourhope (SOU) 1120; Wytham (WYT) 770. Total area across sites: 11,262 ha.
- Boundary characteristics recorded per site include water basin presence, land management, ECN site boundary status, and land ownership characteristics.

## Data sources
- Three data types used to create ecosystem services variables at each ECN site:
  - (i) Data collected according to the ECN protocol.
  - (ii) Site managers’ data from other sources.
  - (iii) Expert knowledge of site managers.

## Variables and dataset structure
- A site managers’ workshop (January 2010) standardized variable selection and definitions.
- Variables cover a broad range of ecosystem services, aligned with MA categories, and include both provisioning and regulating services, as well as cultural, educational, and heritage values.
- Data are annual or single-year (commonly 2009) to reduce temporal variability; area-dependent variables are scaled by site area.
- Categories include (but are not limited to): Food, Fibre, Fuel, Genetic resources, Biochemicals and pharmaceuticals, Ornamental, Air quality regulation, Climate regulation, Water regulation, Erosion, Human diseases, Biological control, Pollination, Natural hazards, Other hazards, Cultural diversity, Spiritual and religious values, Educational values, Aesthetic values, Social relations, Heritage, and Ecotourism.
- Example variable types and units range from production metrics (e.g., Meat produced as live weight, tonnes per hectare) to presence/absence indicators (e.g., Vegetables, Fruits, Ornamental) and quantitative ecosystem service indicators (e.g., Net CO2e flux per hectare year, N/S flux per hectare, butterfly counts, etc.).
- Variables are defined in tables (e.g., table 2 for variable definitions) and dataset structure is described (table 3), with annual indicators stored as a CSV file for long-term storage.
- Data are area-scaled and standardized to support cross-site comparisons and temporal analysis.

## Format, storage, and availability
- The dataset was originally created in Excel 2007 and has been converted to a text file (CSV) for long-term storage.
- Dataset structure includes service type, service definition, indicator units, a Variable_ID, Variable_Number, and site-specific columns (ALI, CAI, DRA, GLE, MOO, NOR, POR, ROT, SNO, SOU, WYT).
- Data are available via the UK NERC Environmental Information Data Centre (EIDC); citation includes a DOI: 10.5285/2c5f823d-0dca-4e66b021-de3e81131979.
- The dataset and its associated metadata were used in the 2011 Environmetrics paper: A comparison of ecosystem services delivered by 11 long-term monitoring sites in the UK Environmental Change Network (Environmetrics, 22(5), 639–648).

## References and usage
- Millennium Ecosystem Assessment (2005) as the foundational framework.
- Data and methodology described for the 11 ECN sites and their ecosystem services variables.
- The dataset supports cross-site comparison of ecosystem services and long-term monitoring to inform environmental health and policy performance analyses.