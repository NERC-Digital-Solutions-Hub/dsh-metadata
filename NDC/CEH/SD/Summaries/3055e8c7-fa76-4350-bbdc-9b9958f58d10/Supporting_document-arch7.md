# Supporting Document for 'A systematic review of common measurement methods of global soil protease activity between 1970-2020' dataset

## Overview
- Purpose: Describes the dataset supporting a systematic review of global soil protease activity (1970–2020) and guides how to use the two raw data files.
- Context: Proteases are key in soil nitrogen cycling; robust, comparable measurement methods are needed; the dataset compiles methods and results from many studies.
- Dataset structure: Two raw-data CSV files capturing methods and results from colorimetric and fluorimetric assays, plus accompanying tables describing variables and units.
- Coverage: Based on 680 studies included in the review; data extracted directly from studies.

## Geospatial and environmental context
- Location data: Each record includes the location where soil was collected to analyze protease activity.
- Spatial indicators: Altitude (m.a.s.l), soil type (FAO 1990 or World Reference Base), and soil depth are recorded where available.
- Climate context: Mean annual temperature (MAT) and mean annual precipitation (MAP) are included to support spatial analyses.
- Limitations for GIS use: The dataset provides textual location information rather than precise coordinates; integration with GIS layers would require georeferencing or supplementary spatial data.

## Data structure and variables
- Files: 
  - Fluorimetric_methods.csv
  - Colorimetric_methods.csv
  - Both share the same layout but contain different measurement modalities (raw data extracted from studies).
- Dataset layout notes:
  - Variables described in Table S6; cells marked "not stated" indicate missing data.
  - Variables include: ID, author, date, title, DOI, soil_type, location, altitude, MAT, MAP, soil_depth, pH (mean and sd), SOC (soil organic carbon) with units, clay content, protease activity (mean, unit, sd, reps), methodCited, description, substrate, substrate_conc, assay_buffer, assay_buffer_conc, assay_ph, assay_time, assay_temp, termination, and wavelength (fluorimetric includes excitation/emission; colorimetric uses nm).
  - Substrate list and assay details reflect the range of methods used across studies.
- Key notes:
  - Protease activity is reported with study-specific units; descriptor fields indicate how activity was measured.
  - The dataset is raw data extracted from the studies (no harmonization applied within these files).

## Data quality, standardization, and challenges
- Heterogeneity: Wide variety of protease assays, substrates, and reporting units across studies.
- Standardization needs: To enable cross-study comparisons or GIS-driven analyses, units, substrates, and assay conditions would require harmonization.
- Missing data: Many variables have missing values (not stated); location details are textual rather than precise coordinates.
- Data quality considerations for GIS: Users should account for methodological differences (substrate, buffer, pH, time, temperature) when mapping or modeling protease activity globally.

## GIS-focused use and best practices
- Mapping opportunities:
  - Create site-level maps of measured protease activity by location, overlayed with soil type, MAT, MAP, and soil depth.
  - Visualize distributions by substrate type (colorimetric vs fluorimetric) and by assay protocol.
  - Combine with global soil and climate layers to explore spatial patterns and potential drivers.
- Data preparation recommendations:
  - Georeference textual locations to obtain coordinates for GIS analyses.
  - Normalize protease activity units or convert to a common metric where feasible.
  - Group or stratify by substrate, assay type, and method cited to compare across methodologies.
- Quality and interpretation:
  - Document assay conditions (pH, temperature, incubation time) as metadata when presenting maps or models.
  - Acknowledge data sparsity in certain regions due to non-uniform sampling and reporting.

## Practical notes and references
- Data are described as raw extraction from studies, with explicit notes on unit definitions and the meaning of "not stated."
- The study references established soil classification resources (e.g., FAO World Reference Base) and soil science manuals for context.
- Table S6 provides the full set of variables and their units used in the dataset, enabling transparent data interpretation and reuse.

## Potential GIS outputs and next steps
- Create global choropleth or point-based maps of protease activity by site, linked to environmental covariates.
- Develop dashboards showing spatial patterns by substrate and method, with filters for year, location, and soil type.
- Conduct spatial analyses to identify regions with higher or lower measured protease activity and explore associations with climate and soil properties.