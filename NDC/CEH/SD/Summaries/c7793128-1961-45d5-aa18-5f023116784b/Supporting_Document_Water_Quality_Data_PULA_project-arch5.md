# PULA water quality data folder

## Overview
- Contains 25 CSV files, each representing one water quality indicator (total of 25 indicators) from groundwater and surface water samples.
- Indicators include major anions/cations and trace metals, plus stable water isotopes (δD and δ18O).
- Collected Feb 2017 – May 2018 by Botswana Department of Water Affairs, with collaboration from Botswana International University of Science and Technology and University of Aberdeen.
- Part of the NERC-funded PULA project to assess effects of extreme rainfall and flooding on water quality across a spatially variable catchment.

## Experimental design and sampling regime
- Sample types: groundwater (GW) and surface water (SW) from the Gaborone Reservoir catchment area, SW streams and reservoir water, GW pumped grab samples after flushing.
- Sampling effort: 287 sampling occasions across 41 days, concentrated in ~15 campaigns aligned to flood-drought-flood cycles.
- Location strategy aimed to cover spatial variability and practical accessibility.
- Sampling approach: three analyses per occasion, with duplicate samples per analysis (two samples per analysis; one for analysis and one for re-runs).
- Field labeling and a detailed data collection log maintained for each campaign.

## Collection, generation, and transformation methods
- For each occasion:
  - 2 × 30 ml for P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb (acidified in field with HNO3).
  - 2 × 15 ml for TOC.
  - 2 × 10 ml for Al, Ca, Fe, K, Mg, Na (stable isotopes for δD and δ18O noted separately).
- Samples stored refrigerated and shipped to University of Aberdeen in four batches; analyses conducted promptly upon arrival.
- Timeline for analyses spanned multiple periods from mid-2017 to mid-2018, with specific batches handled in June–July 2017, August–November 2017, and January–May 2018.
- Instrumentation:
  - ICP-MS (Agilent 7900) for P, Cr, Mn, Co, Ni, Cu, Zn, As, Se, Mo, Cd, Pb.
  - MP-AES for Al, Ca, Fe, K, Mg, Na.
  - LABTOC for TOC.
  - TWIA-45-EP LGR for δD and δ18O.

## Calibration, units, and data limits
- Units and parameter codes provided per indicator (e.g., TOC in mg/L; Cl in mg/L; P in μg/L; etc.), with explicit detection limits and calibration ranges documented (vary by analyte and collection period).
- Notable calibration details:
  - Detection limits and calibration ranges differ across data periods (pre- and post-Dec 2017 for several elements).
  - δD and δ18O are reported in ‰VSMOW with calibration specifics noted.
- Some results exceeded calibration ranges; Pb data particularly problematic and deemed unsuitable for reliable analysis; several elements recorded as <LOD when below detection limits.
- Acknowledgement that for some elements (Cu, Zn, Cd, Pb, Al, Fe, F, Br) more than one-third of samples were below detection limits.

## Data structure and metadata
- Each of the 25 CSV files has a top row with column information in a consistent order:
  - Sample type (SW or GW), sampling location name, longitude, latitude, elevation (if available), and dates of sampling.
  - Sampling date format: dd/mm/yy.
- Location names correspond to Botswana Department of Water Affairs nomenclature.
- Coordinates provided in UTM; latitude/longitude in decimal degrees; elevation in metres.
- Blank cells denote missing values.
- Data organization supports traceability from field collection to laboratory analysis and eventual sharing.

## Data quality and limitations
- Quality control notes:
  - Occasional results fall beyond maximum calibration; interpret with caution.
  - Some data points are below detection limits (reported as <LOD) for several elements.
  - Pb data were largely incomplete and considered unsuitable for inclusion.
- Data completeness varies by analyte and period; users should account for potential gaps, non-detects, and calibration-bound occurrences in analyses.

## Governance, storage, and sharing considerations for Data Stewards
- Clear provenance: linkage from field sampling to laboratory analyses and instrument specifics.
- Standardized metadata: consistent indicators, units, coordinates, and sampling dates across all files to facilitate discovery and reuse.
- Data quality management: document detection limits, calibration ranges, and any data exclusions (e.g., Pb issues) to inform end-users.
- Access considerations: dataset includes sensitive measurement data; note any limitations due to calibration or non-detects; ensure appropriate caveats accompany data releases.
- Update and versioning: multiple sampling campaigns with re-runs; maintain logs or data collection sheets to support reprocessing or audit trails.
- Interoperability: data uses a mix of instruments and units; maintain unit consistency and provide clear method references to enable combining datasets or comparing across indicators.