# Hydroscape chlorophyll abs data

- Overview
  - A dataset of chlorophyll absorbance measurements from hydroscape studies across multiple lakes and connected water bodies, including phytoplankton bioassays (PHYT) and periphyton bioassays (PERI).
  - Aimed at understanding environmental health responses to nutrient treatments and informing monitoring decisions.

- Data collection and study design
  - Phytoplankton samples: surface dip water samples collected at the deepest point of each lake; multiple named lakes and basins listed (e.g., Bassenthwaite Lake, Esthwaite Water, Ranworth Broad, Wroxham Broad, etc.).
  - Periphyton samples: nutrient diffusing periphytometers deployed in streams for two weeks; filters retrieved and processed.
  - Sampling contexts: river bank sampling for some sites; deployment sequencing 1–4 for seasonal bioassays (0 indicates a trial deployment).
  - Nutrient treatments: PHYT and PERI samples subjected to treatments with phosphate, nitrate, ammonium, combined N+P, silica, and controls; nutrient concentrations are indicated in the DOSE field (0 = initial, 1 = control, 2 = P, 3 = N, 4 = N+P, 5 = NH4, 6 = Si).

- Laboratory processing and measurement
  - Pre-treatment: samples filtered through a fine mesh to remove grazers and debris.
  - Incubation: incubated for a defined period (temperature around 20°C) with specified nutrient additions.
  - Post-incubation processing: contents resuspended, filtered onto Whatman GF/C filters; filters frozen for later analysis.
  - Chlorophyll extraction and measurement: methanol extraction followed by absorbance readings using a spectrophotometer at wavelengths 632 nm, 652 nm, 665 nm, 696 nm, and 750 nm; dilution factors recorded (Dilution_factor).

- Data structure and content
  - Core dataset columns include:
    - System, Site, Algae (PHYT or PERI), Deployment, DateStart, DateStop
    - Vol_or_Area (volume for PHYT or area for PERI)
    - DOSE (nutrient treatment code), REPILICATE (replicate identifier)
    - Absorbance values at 632nm, 652nm, 665nm, 696nm, 750nm
    - Dilution_factor
    - Known issues flag (DataFlag: 1 = issue present, 0 = no issue)
  - Site names and locations: extensive table of site names with Eastings and Northings coordinates, covering multiple lakes, tarns, streams, and lochs (e.g., Bassenthwaite_Lake, Castle_Semple_Loch, Grasmere, Derwentwater, Wroxham_Broad, etc.).

- Quality control and data processing
  - Three replicates per treatment were analyzed.
  - Baseline wavelength scans performed and instrument auto-zero and blank corrections applied prior to measurement.
  - Blank-corrected absorbance values used for analysis.

- Metadata and governance considerations
  - Rich metadata including site locations (coordinates) and deployment details enable traceability and spatial analyses.
  - Data quality indicators (Known issues with data) supported by the DataFlag field.
  - The dataset structure supports transparency and reproducibility through explicit treatment codes, replication, and processing steps.

- Relevance for monitoring frameworks
  - Demonstrates the integration of field sampling across diverse sites with controlled nutrient manipulation to assess ecological responses.
  - Highlights the importance of standardized data structures, metadata completeness (site coordinates, deployment details), and QA procedures for policy-relevant environmental health monitoring.
  - Illustrates common barriers and considerations (data completeness, harmonization of methods, data sharing, and clear metadata) that monitoring authors must address when designing and reporting environmental datasets.