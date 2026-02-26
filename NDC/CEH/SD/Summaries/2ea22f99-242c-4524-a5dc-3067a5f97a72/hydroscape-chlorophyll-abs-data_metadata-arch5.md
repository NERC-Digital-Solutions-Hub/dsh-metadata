# Hydroscape chlorophyll abs data

## Overview
- Dataset of chlorophyll absorbance measurements from phytoplankton bioassays (PHYT) and periphyton samples (PERI) across multiple sites in the Hydroscape network.
- Sampling includes surface water from deepest lake points and river-bank locations, plus periphyton samples collected with nutrient-diffusing devices.
- Experiments involve nutrient enrichment treatments to assess responses, with subsequent filtration, extraction, and spectrophotometric measurement of chlorophyll absorbance.

## Data collection and methods
- Sites include Bassenthwaite Lake, Bishop Loch, Castle Semple Loch, Church Bend, Codale Tarn, Decoy Broad, Derwentwater, Esthwaite Water (inflow/middle/south/outflow), Grasmere, Loch Libo, Ranworth Broad, Rydal Water, Strathclyde Loch, Swan Bend, Wroxham Broad, and Woodend Loch, with river sites such as u_s_Codale, u_s_Decoy, u_s_Easedale, u_s_Ranworth, and u_s_Wroxham_Bridge.
- Sampling approaches:
  - Surface water at deepest point of each main basin; river samples from bank edges.
  - Periphyton samples collected via nutrient-diffusing periphyton samplers deployed for two weeks.
  - PHYT samples incubated in test tubes with varying nutrient additions; PERI samples receive corresponding nutrient treatments.
- Processing steps:
  - Initial filtration to remove grazers/debris.
  - Incubation for several days at ~20°C.
  - Post-incubation samples filtered onto GF/C filters, frozen, then chlorophyll extracted in hot methanol.
  - Absorbance readings obtained with a spectrophotometer at multiple wavelengths.

## Data types, units, and structure
- Measured values: absorbance at 632 nm, 652 nm, 665 nm, 696 nm, and 750 nm.
- Data units: absorbance values (optical density) from spectrophotometry.
- Data organization: data stored as a table with 16 fields, including:
  - System (site group)
  - Site (site name)
  - Algae (PHYT or PERI)
  - Deployment (deployment order, 1–4; 0 for trial)
  - DateStart, DateStop (incubation window)
  - Vol_or_Area (volume in ml for PHYT or area in cm2 for PERI)
  - DataFlag (known issues indicator; 1 = issue, 0 = no issue)
  - DOSE (nutrient treatment code, 0 for initial value; 1–6 for various nutrient additions)
  - REPILICATE (replicate identifier, typically A–C; sometimes A–D in trials)
  - 632nm, 652nm, 665nm, 696nm, 750nm (absorbance values)
  - Dilution_factor (1 = no dilution, 2 = 50% dilution)
- DataFlag is used to flag records with known issues.

## Quality control and processing notes
- Three replicates analyzed per treatment.
- Baseline wavelength scans performed with methanol; instrument auto-zeroing and blank correction applied to all wavelengths.
- Absorbance values corrected using blank measurements prior to interpretation.

## Site locations and mapping references
- Site names with precise coordinates provided (Eastings/Northings) for mapping and reproducibility.
- Included a mix of lakes, lochs, tarns, and inflows/outflows to cover diverse hydroscape environments.

## Usage notes and considerations for data stewardship
- The dataset uses standardized headers and explicit coding for treatments (DOSE) and deployments, aiding discovery and interoperability.
- The presence of a DataFlag and detailed site coordinates supports data quality assessment and geospatial analyses.
- Metadata completeness (deployment order, dates, sample volumes/areas, dilution factors, and replicate IDs) is essential for reuse and traceability.