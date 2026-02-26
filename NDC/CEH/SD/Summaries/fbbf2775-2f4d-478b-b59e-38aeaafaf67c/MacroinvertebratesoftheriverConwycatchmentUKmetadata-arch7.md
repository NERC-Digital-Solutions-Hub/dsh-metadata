# Macroinvertebrates of the Conwy catchment

## Overview
- Dataset describing macroinvertebrate communities in the Conwy catchment, Wales, UK, sampled over 2008–2010 (three-year span).
- Provides species-level taxonomic descriptions, plus supporting habitat and geographic data.
- Sampling followed the RIvPACS protocol; includes site variables (depth, width, velocity, substrate cover, macrophyte cover) and specimen preservation/analysis details.
- Data are organized into three CSV files: taxon data, environmental variables, and supporting information.
- Map-derived variables were created using the Intelligent River Network (IRN) version 17.

## Datasets and structure
- Taxon data (Macroinvertebrates of the Conwy catchment - taxon data.csv)
  - Columns include: Site code, Year, Sample date, Taxon code, Taxon name, Life stage, Abundance.
- Environmental variables (Macroinvertebrates of the Conwy catchment - environmental variables.csv)
  - Columns include: Site code, Year, Wetted width, Water depth, Velocity, % cover of rock pavement, % cover by substrates (rocky components, sand/silt/clay), % cover by macrophytes.
- Supporting information (Macroinvertebrates of the Conwy catchment - supporting information.csv)
  - Site-level geographic and catchment attributes: Easting, Northing, OS grid reference, Distance from source, Altitude, Slope, River/Stream order, Upstream catchment area, and site names.
- Sample identifiers are defined by a unique combination of site code and year; a key to site codes is provided in the supporting information.
- Taxon names and codes follow Davies & Edwards (2011); life stages use standard codes (L, N/A, etc.).
- Data validation: entries cross-checked against laboratory sheets; taxonomic names mapped to a formal code list.

## Spatial data and GIS readiness
- Study area comprises tributary streams of the Conwy, with precise site locations recorded as Easting/Northing and OS grid references.
- Geographic coordinates and site attributes enable GIS mapping, spatial joins, and spatial analysis of macroinvertebrate communities.
- Map variables derived via IRN v17 support GIS analyses of environmental context and river classification.
- Spatial resolution is tied to site-level observations rather than continuous raster data; suitable for point-based mapping and site-level comparisons.

## Provenance, methodology, and quality
- Sampling occurred in November of 2008, 2009, and 2010 using a 1 mm kick net.
- Methodology described in the RIvPACS protocol; site variables recorded accordingly.
- Laboratory processing included washing and identifying macroinvertebrates to the lowest possible taxonomic level; validation against the Davies & Edwards code list (2011).
- Data entry validated through cross-checks with laboratory records.
- Map-variable derivation and associated literature: Dawson et al. (2002) for automated extraction of environmental variables; RIvPACS source protocol and Davies & Edwards (2011) taxonomy code list.

## Access and usage notes
- Version: 1.0; date: 28/06/2016; author: F. Edwards.
- Contributors: field sampling (Gearóid Webb, Peter Scarlett, John Davy-Bowker); lab analysis (Gearóid Webb, Helen Vincent, François Edwards); supporting information and planning/management (Peter Scarlett, François Edwards, David Cooper).
- Files to consult:
  - Macroinvertebrates of the Conwy catchment - taxon data.csv
  - Macroinvertebrates of the Conwy catchment - environmental variables.csv
  - Macroinvertebrates of the Conwy catchment - supporting information.csv
- Useful for GIS workflows such as:
  - Creating point layers of sampling sites with attribute data (taxa abundance, life stages).
  - Joining environmental variables to sites for spatial analysis of habitat and macroinvertebrate patterns.
  - Linking site geographic attributes (Easting/Northing, Altitude, Slope, Catchment area) to analyses of environmental drivers.
  - Producing map visuals of species distributions and site-level environmental context.

## How to integrate into GIS workflows
- Join taxon data to environmental data and supporting information on Site code and Year to create a comprehensive per-site, per-year dataset.
- Convert Easting/Northing or OS grid references to desired coordinate reference system for mapping and spatial analysis.
- Use taxon codes and names to categorize biodiversity indicators; leverage life-stage information for species assemblage studies.
- Incorporate map-derived variables (from IRN v17) as additional spatial attributes or as predictors in spatial models of macroinvertebrate communities.