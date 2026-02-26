# Hydroscape chlorophyll abs data

## Overview
- Dataset of absorbance-based chlorophyll measurements for phytoplankton (PHYT) and periphyton (PERI) from multiple lakes, rivers, and lochs in the Hydroscape study area.
- Includes bioassay experiments with nutrient additions (phosphorus, nitrogen forms, silica) and corresponding controls.
- Provides detailed methodological notes on sampling, incubation, extraction, spectrophotometric measurement, and quality control.
- Contains a structured data schema and extensive site metadata with geographic coordinates.

## Data collection and field methods
- Sample types
  - Phytoplankton (PHYT): surface water samples collected from deepest points in lakes/basins or lake edge for various sites.
  - Periphyton (PERI): filters obtained from nutrient-diffusing periphytometers deployed in streams for multi-week periods.
- Sampling locations
  - Lakes: Bassenthwaite Lake, Decoy Broad, Derwentwater, Grasmere, Malthouse Broad, Ranworth Broad, Rydal Water, Wroxham Broad, Esthwaite Water (North, Middle, South), plus Bishop Loch, Castle Semple Loch, Codale Tarn, Easedale Tarn, Loch Libo, Strathclyde Loch, Woodend Loch.
  - Rivers/edges: sampling from specified river banks and lake edges (examples include Church Bend, Decoy, Ranworth Broad, Wroxham Bridge, etc.).
- Field procedures
  - Phytoplankton samples filtered initially through a 0.45 µm mesh to remove grazers and debris.
  - Periphyton: deployment of periphytometer filters in streams for approximately two weeks; filters retrieved and frozen.
  - Incubations: bioassays started within hours of sampling; samples kept cool in the dark during handling.
- Nutrient bioassays
  - Treatments include combinations such as phosphorus (P), nitrogen (N), NP (P + N), ammonium, silica, and control (no addition).
  - Treatments applied at specified µM levels (phosphorus, nitrogen, silica) with triplicate replicates.
  - Incubation period runs over several days at around 20°C (exact duration per deployment detailed in dataset notes).
- Sample processing
  - After incubation, contents are resuspended, filtered onto Whatman GF/C filters, and frozen for later analysis.
  - Phytoplankton and periphyton samples undergo separate extraction steps prior to absorbance measurement.

## Analytical methods
- Extraction and measurement
  - Filters defrosted and extracted in hot methanol; absorbance readings obtained with a UV-Vis spectrophotometer.
  - Measurements used to quantify chlorophyll a absorbance at multiple wavelengths.
- Wavelengths measured
  - 632 nm, 652 nm, 665 nm, 696 nm, 750 nm.
- Instrument and measurement specifics
  - Measurements performed using a Hitachi UV-Visible spectrophotometer with a 1 cm cuvette.
- Quality control
  - Three replicates per treatment.
  - Baseline wavelength scan performed with methanol as reference prior to sample measurement.
  - Instrument auto-zero and blank values corrected at each wavelength.

## Data structure and fields
- Data schema (columns)
  - System: group of sites where data were collected.
  - Site: site name.
  - Algae: either PHYT (phytoplankton) or PERI (periphyton).
  - Deployment: deployment order (1–4); 0 indicates a trial deployment.
  - DateStart: incubation start date.
  - DateStop: incubation stop date.
  - Vol_or_Area: volume (ml) for PHYT or area (cm2) for PERI, from which chlorophyll a was extracted.
  - DataFlag: known issues with data; 1 = issues present, 0 = no issues.
  - DOSE: nutrient treatment code (0 = initial values for PHYT; 1 = control; 2 = P; 3 = N; 4 = N+P; 5 = Ammonium; 6 = Silica for PHYT; for PERI, codes are slightly different but include controls and nutrient additions).
  - REPLICATION: replicate identifier (mostly a–c; in deployment 0 at Esthwaite Water, a–d).
  - 632nm, 652nm, 665nm, 696nm, 750nm: absorbance values at corresponding wavelengths.
  - Dilution_factor: dilution factor (1 = no dilution; 2 = 50% dilution).
- Site metadata
  - A comprehensive table lists site names with corresponding Eastings and Northings (grid coordinates) for geographic reference.
  - Examples of site groupings include Bassenthwaite_Lake, Bishop_Loch, Castle_Semple_Loch, Decoy_Broad, Derwentwater, Esthwaite_Inflow, Esthwaite_Middle, Grasmere, Ranworth_Broad, Wroxham_Broad, etc.

## Data quality and governance notes
- Replication and QC measures in place (triplicates, baseline scans, blanks, auto-zero corrections).
- Known issues flag indicates data quality concerns for specific rows or treatments.
- Detailed metadata supports data discovery, provenance, and re-use across projects and data ecosystems.

## Practical implications for data leadership
- Provides a robust, well-documented data pipeline from field collection to laboratory analysis and digital encoding.
- Supports governance around data quality, metadata completeness, and traceability of nutrient treatment experiments.
- Enables cross-site comparisons of chlorophyll absorbance responses under varied nutrient regimes, aiding strategy for data integration, standardization, and community data practices.