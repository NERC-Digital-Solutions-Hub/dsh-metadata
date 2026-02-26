# LOCATE

## Overview
- Multidisciplinary NERC project involving the National Oceanography Centre, British Geological Survey, UK Centre for Ecology and Hydrology, Plymouth Marine Laboratory, with help from several universities and the Environment Agency.
- Aim: improve understanding of carbon flow from land into the ocean; rivers were selected to reflect diverse land-use types and to be representative of Great Britain.
- This document describes Part 2 of the river dataset, which contains ICP-MS analyses of river water collected alongside Part 1 (which covers river water parameters). Part 1 has a companion estuary dataset and is accessible via DOIs and BODC/EIDC.
- Part 2 focuses on the geographical and seasonal variation of cations, based on monthly samples from 41 rivers across England, Scotland, and Wales during 2017 (plus earlier samples in November 2016).

## Data scope and structure
- Contains results of ICP-MS analyses for major and trace elements in river waters.
- Dataset includes:
  - 41 rivers with monthly sampling (Jan–Dec 2017) and some samples in Nov 2016 (trial run); Dorset Stour DSTO excluded in some months and first sampled from April 2017.
  - Metadata on sampled rivers is provided in locate_river_info.txt.
  - Data file format: CSV with 61 columns, including variables such as river name, month, and concentrations for numerous elements (e.g., Ca, Mg, Na, K, P, S, Si, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, lanthanides, transition metals, etc.). Units are mg/L or μg/L; missing values are denoted as n/a.
- Data quality and reporting:
  - Each element column has two detection-limit lines per entry: Batch DL and Method DL (the latter being the UKAS-accredited detection limit for the method).
  - When concentrations are below detection limits, they should be reported as below the relevant DL.

## Sampling regime and field procedures
- Sampling schedule:
  - Monthly sampling from a fixed site on each river; most sites sampled within a 2–3 day window each month.
  - Dorset Stour not sampled in some months; first sampling occurred in April 2017.
  - November 2016 used as a trial run; coordination led by Andy Tye (BGS).
- Sampling protocol highlights:
  - Field processing: all filtering and splitting into bottles performed in the field except POC samples (filtered in the lab on return).
  - Samples kept dark in cool boxes or freezers; salinity and electrical conductivity (SEC) measured in the field where possible; temperature recorded in the field to 0.1 °C precision.
  - Sampling depth: 0–30 cm mid-channel where feasible; otherwise from a representative fast-flowing part of the river.
  - Bottles and filters rinsed thoroughly to prevent contamination; 500 mL bottles used for total sample; 60 mL bottles for ICP-MS analyses; isotope samples filtered with 0.45 μm filters into 20 mL glass vials.
  - Field procedures included photographing sites upstream and downstream; gloves worn to avoid contamination; a single collection vessel was rinsed with sample water three times and filled with the sample water for all subsequent bottle filling.
  - In-field data form recorded weather and river conditions; samples were transported in cool boxes or freezers and returned to the institute for analysis.
- Post-sampling processing:
  - Upon return to the institute, samples were acidified to 1% HNO3 (using concentrated HNO3) at BGS Keyworth; to minimize blanks, all samples were prepared with a single acid source.
  - Blank samples created by acidifying MQ water in the same way.

## ICP-MS analyses and QA/QC
- Instrumentation and method:
  - Instrument: Agilent 8900 ICP-QQQ.
  - Analytical method: Ag_2.3.21, Determination of major and trace elements in aqueous samples using ICP-MS.
  - Analyzed concentrations are reported in mg/L or μg/L depending on element.
  - Sample preparation: water samples 0.45 μm filtered and acidified to 1% HNO3; after receipt, samples were further treated with 0.5% v/v HCl in the laboratory.
- Quality control:
  - UKAS accreditation: laboratory is ISO/IEC 17025:2017 (UKAS lab 1816).
  - QC frequency: QC runs every 20 samples; calibration blocks per run (approximately 125 samples per run).
  - Stock/reagents: multiple multi-element standards and single-element standards used (detailed listing provided in the dataset description).
  - Data evaluation: results assessed with Shewhart plots; DLs (detection limits) are defined as batch DL (based on 3× standard deviations × dilution for blanks) and method DL (UKAS method DL for the Ag_2.3.21 method). If concentrations fall below DL, they should be reported as below DL.

## Data accessibility and provenance
- The LOCATE dataset is part of a larger set; Part 1 data (river water parameters and associated estuary data) is available via DOIs and BODC/EIDC repositories.
- Part 2 data (ICP-MS river cations) is described here, with accompanying river-site metadata in locate_river_info.txt.
- Coordination and contact: sampling coordination led by Andy Tye (bgs) with contact details provided in the dataset documentation.
- Additional notes: Some outputs, such as site photos, are available but could not be submitted to EIDC.