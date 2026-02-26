# Radioisotope concentrations of soil samples from UK saltmarshes collected between 2018 and 2021

## Overview
- Part of the Carbon Storage in Intertidal Environments (C-SIDE) project funded by NERC (NE/R010846/1).
- Dataset contains 1,358 down-core soil samples from 19 UK saltmarshes, collected 2018–2021.
- Measured radioisotopes: total and unsupported 210Pb (210Pb and 210Pbex), 214Pb, 137Cs, and 241Am.
- Data are recorded with precise geographic locations in decimal degrees (WGS84).

## Location and sampling coverage
- Observations span multiple saltmarsh sites around the UK coastline to represent diverse saltmarsh habitats.
- Each observation includes latitude and longitude (decimal degrees, WGS84).
- Sampling date is recorded for each core/sub-sample.

## Key variables and data structure
- Core_ID: Core identification (text).
- Location: Saltmarsh name (text).
- Sample_Depth_cm: Depth interval of sub-sample (cm).
- Mid_Depth_cm: Mid-point depth of the interval (cm).
- Lat_dec_deg, Long_dec_deg: Geographic coordinates (decimal degrees).
- Sampling_Date: Date of sample collection.
- Mass_g: Mass of each sub-sample (g).
- Cs-137_Bq_kg: Cesium-137 activity concentration (Bq/kg).
- Cs-137_2-sigma: Uncertainty for Cs-137 (2-sigma).
- Pb-210_Bq_kg: Lead-210 activity concentration (Bq/kg).
- Pb-210_2-sigma: Uncertainty for Pb-210 (2-sigma).
- Pb-214_Bq_kg: Lead-214 activity concentration (Bq/kg).
- Pb-214_2-sigma: Uncertainty for Pb-214 (2-sigma).
- Pb-210ex_Bq_kg: Excess (unsupported) 210Pb concentration (Bq/kg).
- Pb-210ex_2-sigma: Uncertainty for Pb-210ex (2-sigma).
- Am-241_Bq_kg: Americium-241 activity concentration (Bq/kg).
- Am-241_2-sigma: Uncertainty for Am-241 (2-sigma).

## Methods and quality assurance
- Sample preparation: Freeze-dried, lightly milled samples sealed in polystyrene vessels; typical packed mass up to 30 g; smaller masses near the top of cores.
- Counting: Samples counted for a minimum of ~86,000 seconds (~24 hours) per sample across 2019–2023; on average ~25 samples per core.
- Instrumentation: Ortec planar detector system (GEM-FX8530-S N-type); ultra-low background HPGe gamma spectrometry optimized for 210Pb detection.
- Target isotopes and gamma energies: 210Pb (46.5 keV), 214Pb (295.3 keV; 352.0 keV), 137Cs (661.6 keV), and 241Am (59.5 keV); multiple energies used for QA.
- Calculation of 210Pbex: Total 210Pb minus 226Ra activity (measured via 214Pb) to obtain the unsupported component.
- Calibration: Instrument calibrated with low-background soil spiked with certified mixed radioactive standards at masses 3.2 g, 9.9 g, 16.6 g, 30.4 g; analysis with EG&G GammaVision software; verified by inter-laboratory tests with IAEA materials (moss soil QA focusing on 210Pb, 214Pb, 137Cs, 40K).
- Data QA: Laboratory equipment calibrated per institutional practices; Moss soil QA used as part of quality assurance.

## Data format and accessibility
- Data stored as CSV files; includes detailed header descriptions and units.
- Data resource description corresponds to the dataset named C_SIDE_saltmarsh_radioisotopes_concentrations.csv.
- Includes metadata for each field (description, type, and units) to support discoverability and reuse.

## Practical considerations for analysts
- Enables dating of saltmarsh sediment cores via 210Pb/210Pbex dating along with 214Pb and 137Cs markers.
- Supports cross-site comparisons due to standardized sampling, preparation, counting, and QA procedures.
- Provides measurement uncertainties (2-sigma) for all isotope concentrations, essential for statistical modeling and interpretation.
- Suitable for studies on carbon storage, sedimentation rates, and environmental change in UK saltmarsh ecosystems.

## Provenance and data lineage
- Project: Carbon Storage in Intertidal Environments (C-SIDE); funded by NERC.
- Data resource: Radioisotope concentrations from UK saltmarsh soils, 2018–2021, with 1358 samples across 19 sites.
- Documentation includes core identifiers, precise geolocations, sampling dates, depth intervals, mass, activities, and associated uncertainties.