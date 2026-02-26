# Hydroscape chlorophyll abs data

## Overview
- A dataset describing chlorophyll a absorbance from hydroscape bioassays, including two bioassay types:
  - PHYT: phytoplankton incubations in filtered water
  - PERI: periphyton samples from streams
- Sampling scope covers multiple UK water bodies (lakes and streams), including Bassenthwaite Lake, Derwentwater, Grasmere, Wroxham Broad, and others; sites include inlet/outlet points and various lake edges.
- Data capture includes nutrient manipulation experiments with multiple treatments and replicates, followed by spectrophotometric absorbance measurements at several wavelengths to derive chlorophyll a indicators.
- Outputs are structured data with detailed metadata and site coordinates, enabling cross-site comparisons and self-serve analysis.

## Sampling and data collection methods
- Water samples were collected from the deepest points of lakes using long-handled sampling poles (specific lakes listed).
- Periphyton samples (PERI) were taken from nutrient-diffusing periphytometers deployed in streams for two weeks.
- Phytoplankton samples (PHYT) were prepared by filtering to remove grazers and large debris, then aliquoted into incubation tubes.
- Nutrient treatments applied to samples in triplicate across a range of doses (including controls and various nutrient additions such as phosphorus, nitrogen, ammonium, and silica).
- Incubation period conducted under controlled conditions (described in the protocol; temperature and duration are specified generally in the text).
- After incubation, contents were filtered onto Whatman GF/C filters and frozen for later analysis.

## Experimental design and treatments
- Treatments coded by DOSE with values representing:
  - 0: initial values (phytoplankton baseline)
  - 1: control (no nutrient addition)
  2: P addition
  3: Nitrate addition
  4: N + P addition
  5: Ammonium addition
  6: Silica addition
- For PERI samples, dose codes follow a similar scheme with corresponding nutrient additions.
- Replicates: typically triplicate measurements per treatment (PHYT and PERI).
- Post-treatment processing includes extraction of chlorophyll from samples for absorbance measurement.

## Data structure and variables
- The dataset contains a structured table with 16 data headers describing each observation. Key headers and descriptions include:
  - System: group of sites where data was collected
  - Site: site name
  - Algae: bioassay type (PHYT or PERI)
  - Deployment: order number of seasonal deployments (1–4; 0 for a trial deployment)
  - DateStart / DateStop: incubation start and stop dates
  - Vol_or_Area: volume (ml) for PHYT or area (cm2) for PERI, used to derive chlorophyll extraction
  - DataFlag (Known issues): indicator (1 for known issues, 0 otherwise)
  - DOSE: nutrient treatment code (0–6) with meanings as above
  - REPILICATE: replicate identifier (mostly a–c; sometimes a–d)
  - 632nm, 652nm, 665nm, 696nm, 750nm: absorbance measurements at specified wavelengths
  - Dilution_factor: dilution factor (1 = no dilution, 2 = 50% dilution)
- Site names table provides coordinates (Eastings/Northings) for each location, enabling spatial analyses.

## Quality control and data processing
- Three replicates per treatment were analyzed.
- Baseline wavelength scans were performed on the spectrophotometer using methanol as reference before measurement; instrument auto-zero and blank corrections applied per wavelength.
- Blank values at each wavelength used to correct sample absorbance readings.
- Samples were stored and processed under controlled conditions (cool storage, dark incubation for PHYT; periphyton processing for PERI as described).

## Site locations
- The dataset includes a comprehensive set of site names with precise coordinates (Eastings and Northings in a regional coordinate system), for example:
  - Bassenthwaite_Lake, Bishop_Loch, Castle_Semple_Loch, Church_Bend, Codale_Tarn, Decoy_Broad, Derwentwater, Grasmere, Ranworth_Broad, Wroxham_Broad, among others
- Coordinates are provided to support spatial mapping and site-specific analyses.

## How to use and caveats
- Use to analyze chlorophyll a responses to nutrient amendments across multiple freshwater systems and both phytoplankton and periphyton communities.
- The presence of the Known issues flag (DataFlag) helps identify observations with potential quality concerns.
- The dataset supports cross-site comparisons of nutrient effects, seasonality through deployment numbering, and wavelength-based chlorophyll assessments.
- Be mindful of garbled or missing textual details in the original method notes (e.g., exact mesh sizes, incubation durations, and specific concentration values); rely on the structured data headers and the quality-control indicators for robust analyses.