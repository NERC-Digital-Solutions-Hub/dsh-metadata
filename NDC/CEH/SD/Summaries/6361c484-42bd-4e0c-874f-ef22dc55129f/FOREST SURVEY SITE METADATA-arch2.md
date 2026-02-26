# Forest Planting and Harvest Records

## Overview
- A large multi-site dataset recording forest planting, second planting, and felling events across numerous locations (sites labeled A1, A2, A7, B3, C17, D32, E44, etc.).
- For each site, contains geospatial coordinates (Easting, Northing), planting history (year of first planting, species, soil type), felling history (year felled, and whether a second planting occurred), second planting details (year and species), and start/end date components (day, month, year).
- Dominant data theme is monitoring timber stands over time to assess environmental health and policy performance.

## Data fields and structure
- Site identifiers (e.g., A1, A2, B3, C17, D32, E44, etc.)
- Spatial coordinates: Easting and Northing
- First planting: year, species, soil type
- Year felled: year or status (e.g., Standing crop)
- Year of second planting and second planting species
- Start date and End date: day, month, year components
- Some fields include NA (missing) values or placeholders (e.g., Year of second planting = NA)

## Temporal and spatial coverage
- Temporal span of first plantings ranges from early 20th century (e.g., 1914 at C17) to mid-20th century (e.g., 1961 entries such as A58/A59 area).
- Felling and second-planting events mainly occur in the 1990s (with many entries showing felled years around 1994–1997) or ongoing standing crops.
- Spatial scope covers numerous grid-like coordinates (Easting/Northing) indicative of a mapped region, with varied soil types and species.

## Key patterns and observations
- Species distribution: Sitka spruce is the most frequent species; other species include Norway spruce, Western hemlock, Scots pine, Japanese larch, Noble fir, Douglas fir, Lodgepole pine, and others.
- Soil types represented: Gley, Podzol, Brown earth, and Bog, indicating diverse site conditions.
- Planting history: Many sites show a sequence of first planting, sometimes followed by a second planting (often a year or more later), with some sites recording repeated planting events.
- Felling status: A mix of “Standing crop” (not yet felled) and actual felled years, suggesting ongoing harvest cycles at several sites.
- Data gaps: Numerous NA values for second planting fields and some dates, and some two-digit year representations (e.g., 95, 97) that require interpretation for full temporal clarity.

## Data quality and limitations
- Numeric years are sometimes stored as two digits (e.g., 95 for 1995), requiring normalization to four-digit years for accurate longitudinal analyses.
- Missing values and inconsistent formatting (e.g., Start date/End date components split across fields) may complicate automated processing.
- Some sites lack second-planting data or felled status, which may limit understanding of full stand histories without inferential assumptions.

## How this dataset supports environmental monitoring
- Enables tracking of plantation age structures, species distributions, and soil-type associations across the landscape.
- Supports temporal analyses of forest development, harvesting cycles, and the impact of management decisions on stand composition.
- Facilitates comparative assessments of environmental health indicators (e.g., diversity of species, forest age classes) over time and space.

## Data access, sharing, and use considerations
- To maximize value, standardize date formats (convert two-digit years to four-digit years with a consistent rule), harmonize soil-type labels, and fill or flag missing second-planting data where possible.
- Link with ancillary datasets (climate records, soil maps, biodiversity inventories, harvest records) to enrich environmental health assessments and policy evaluations.
- Ensure metadata documents data provenance, variable definitions, and any transformations applied to support transparency and reuse.

## Implications for analysts monitoring the environment
- Combine this dataset with climate and soil data to analyze how site conditions influence species choice and stand development over time.
- Use standardized outputs (e.g., age since planting, duration to felled status, second-planting intervals) to assess policy performance on sustainable harvesting, replanting efficiency, and habitat renewal.
- Prioritize data quality improvements and data portal accessibility to enable broader access and secondary use by researchers and decision-makers.