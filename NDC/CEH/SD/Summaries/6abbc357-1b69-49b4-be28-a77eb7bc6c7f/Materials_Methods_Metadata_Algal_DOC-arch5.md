# Materials and methods, and metadata for Measured and modelled DOC concentrations, and chlorophyll concentration, for UK freshwaters and freshwater mesocosms, 2014-2015. Data taken from 'The contribution of algae to freshwater dissolved organic matter: implications for UV spectroscopic analysis', Adams et al, 2018 Inland Waters

## Overview
- Presents measured and modelled DOC concentrations and chlorophyll-a for UK freshwaters and freshwater mesocosms during 2014–2015.
- Data originate from field sites and controlled mesocosm experiments, linked to algae-driven DOM production and UV-Vis analysis.
- Includes both direct measurements (DOC by TOC, chlorophyll-a) and modelled values (DOC via UV-Vis Carter model), plus related absorbance and basic water chemistry.

## Study sites and mesocosm experiments
- Field sampling locations include:
  - Shropshire-Cheshire meres in the North West Midland outwash plains (diverse small catchments).
  - Ten samples from small lakes in the Lake District National Park.
  - Four samples from reservoirs in West Yorkshire.
  - Ten additional sites comprising farm ponds in the Fylde area and rivers/streams draining lowland farmland and urban areas in Yorkshire.
- Mesocosm experiments:
  - Conducted within the CEH aquatic mesocosm facility (CAMF) with 32 mesocosms (2 m diameter, 1 m deep).
  - Four mesocosms selected for a multiple-stressor experiment (tanks 4, 7, 15, 20) to achieve a range of chlorophyll-a concentrations.
  - Treatments included heating (+4 °C) and intermittent nutrient additions (N and/or P-free nutrient amendments).
  - Sampling occurred on seven occasions between February and August 2015.
  - Aim: attribute DOM production to algal CO2 fixation and subsequent DOM release under different stressors.

## Data products and metadata structure

- Table S1a: Shropshire-Cheshire meres field data
  - Variables include site code (SCM), site name, sample ID, date, latitude, longitude, DOC measured (TOC, mg/L), DOC modelled (mg/L, Carter model), absorbance at 270 nm and 350 nm (Au), chlorophyll-a concentration (µg/L), pH, conductivity (µS cm-1).
  - Column definitions, units, and notes provided to facilitate reuse.

- Table S1b: Other field sites
  - Site types include LD (Lake District), PR (reservoirs), FP (farm ponds), YR (Yorkshire rivers).
  - Same core variables as Table S1a (DOC measured/modelled, absorbance, chlorophyll-a, pH, conductivity), with additional notes for measured pH on new samples.
  - Column headings include site code, site name, sample ID, date, location coordinates, DOC and absorbance values, chlorophyll-a, pH, and conductivity.

- Table S1c: Mesocosm time-series data
  - Mesocosm tank number, date, [DOC] measured (mg/L), [DOC] modelled (mg/L), absorbance at 270 nm and 350 nm, [chl-a] (µg/L), pH, and conductivity (µS cm-1).
  - Documentation includes notes on conductivity columns (e.g., Conductivity, 1; Conductivity, 2) and timing of time-series sampling.

- Table S2: Time-series [DOC] and [Chla] data for mesocosms
  - Includes [DOC] and [chl-a] values with log-transformed representations (Log [DOC], Log [chl-a]), plus formatting for time-series analyses.
  - Columns cover tank identification, date, measured values, and transformed metrics as applicable.

- Modelling and measurement details
  - [DOC] measured by TOC analysis; [DOC] modelled using UV-Vis absorbance via the Carter model.
  - Absorbance measurements at 270 nm and 350 nm accompany DOC and chlorophyll data.
  - Chlorophyll-a concentrations provided where available; pH and conductivity captured as basic water chemistry context.
  - For some sites, pH values are drawn from Fisher et al. 2009 rather than new measurements.

## Data provenance, quality, and governance

- Provenance
  - Data tied to the study of algae contributions to freshwater DOM and UV spectroscopic analysis, with explicit references to Adams et al., 2018 (Inland Waters) and Fisher et al., 2009.
  - Supplementary tables (S1a–c, S2) provide structured metadata and column definitions to support reuse.

- Metadata and standards
  - Detailed column heading explanations, units, and notes accompany each data table to ensure consistent interpretation and interoperability.
  - Clear documentation of measurement methods (TOC for DOC, UV-Vis for modelled DOC, absorbance wavelengths) and modelling approach (Carter model).

- Accessibility and stewardship considerations
  - Data are organized for upload to data portals/catalogues; appropriate for broad sharing while noting potential data restrictions (e.g., embargo or licensing not specified here).
  - They support reproducibility and future synthesis by providing site codes, coordinates, sample IDs, dates, and full metadata.

- Limitations and considerations for reuse
  - Some pH values are sourced from prior studies; users should note potential differences in measurement context.
  - Multiple site types and data sources necessitate careful harmonisation if merged with other datasets.
  - The datasets span 2014–2015, with reference data and analyses published in 2018; versioning and provenance trails should be maintained for updates.

## Implications for data governance and reuse (Data Stewards perspective)

- Ensure consistent data curation across Tables S1a–c and Table S2, preserving column definitions and units.
- Maintain provenance links to Adams et al. 2018 and Fisher et al. 2009 for contextual metadata and any legacy pH values.
- Implement a publishable data package with clear metadata, licensing, and access controls suited for portals.
- Harmonise site identifiers and coordinate systems to enable cross-dataset interoperability (e.g., match site codes, lat/long formats).
- Track updates or corrections to measurement methods (TOC, absorbance, Carter model) and reflect changes in versioned data releases.
- Provide guidance on using Log [DOC] and Log [Chla] transforms for analysis, including any handling of zero or negative values.