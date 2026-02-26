# Sediment collection

## Overview
- Describes sediment trap collection and sediment core sampling at Rostherne Mere (May 2010–Sept 2016) and subsequent analyses.
- Provides data products: three CSV datasets containing trap data, core data, and dataset-specific metadata/derived metrics.

## Sampling and data collection workflow
- Sediment trapping
  - Use Technicap PPS 4/3 automatic sequencing traps (1310 mm long, 252 mm ID, 1:5.1 trapping ratio, 0.05 m2 area).
  - Traps deployed at 10 m (shallow) and 25 m (deep) depths; each trap feeds into 12 × 250 mL HDPE bottles representing 2-week collection periods (longer periods up to 4 weeks in January–February).
  - Traps reset every 6 months; trap sediment kept cool, dark, sealed during transport; stored frozen in laboratory prior to analysis.
- Sediment core
  - 112 cm Livingstone piston core collected at 26 m depth (Sept 2011).
  - Core stored vertically in a dark cold room at 5°C; extruded at 1 cm intervals for upper 50 cm, then 0.5 cm intervals.

## Analysis methods and calibration
- Pre-analysis processing
  - Freeze-drying of trap and core samples.
  - Loss-on-ignition (LOI) to determine organic matter (OM) via weight loss after 3 h at 550°C.
  - Organic carbon (OC) calculated from %OM using a lake-specific factor (OC = OM × 0.56) derived from calibration against mass-spectrometry OC measurements.
- Isotopic and elemental analyses
  - d13C analyzed by mass spectrometry; calibration results included (e.g., SOIL B and BROC2) used to convert OM to OC and interpret carbon/nitrogen data.
  - Carbon to nitrogen ratios (C/N) and carbon to LOI ratios (C/LOI) recorded.
- Chronology and flux calculations
  - 210Pb activity measured for core samples to determine sedimentation rates using the CRS (constant rate of supply) model.
  - Confidence intervals calculated via first-order counting uncertainty.
  - Derived metrics include focusing-corrected organic carbon burial rates (g C m-2 yr-1) and various sediment fluxes.

## Data structure and contents
- Datasets
  - RMLOItoTOC: 9 columns; links LOI-derived data to OC, including SampleNo, d13C, C, N, C/N, Trap/core indicator, Depth, LOI, C/LOI.
  - RMSedCore2011LOI: 7 columns; core depth, water content, CaCO3, LOI, estimated date, sedimentation rate, and focusing-corrected organic carbon flux.
  - RMTrapSed: 14 columns; sample identifiers, collection dates, trap depth (Shallow/Deep), CaCO3, LOI, minerogenic fraction, days collecting, dry weight, trap area, and various flux calculations (organic matter, organic carbon, CaCO3, minerogenic).
- Key fields and units
  - Recorded values include water content, LOI (%), CaCO3 (%), OC (%), C/N, C/LOI, sedimentation rates (g cm-2 yr-1 for core; g m-2 d-1 for traps), and various fluxes (g m-2 d-1 or g m-2 yr-1).
  - Depths: trap depths (10 m or 25 m) and core depths in cm.
  - Time stamps: collection dates and durations; sample dating via 210Pb chronology.

## Data quality, provenance, and references
- Provenance
  - Original methods and calibration references: Appleby (2001) for CRS chronology; Dean (1974) LOI method; Wright (1967) piston sampler.
- Calibration and interpretation notes
  - Lake-specific OC conversion factor (OC = OM × 0.56) derived from calibration against mass-spectrometry OC data.
  - Example calibration results provided (SOIL B, BROC2) to support carbon quantification and interpretation.
- Data completeness and limitations
  - Blank fields indicate samples not analyzed.
  - Longer collection periods noted for some months; potential variability in trap capture rates across intervals.
- Data governance and reuse
  - Data are organized into defined CSV files with explicit column metadata, supporting reuse, discovery, and integration with other datasets.
  - Clear documentation of sampling design, processing steps, and calculation methodologies to support reproducibility.

## Usage considerations for Data Stewards
- Ensure dataset discoverability and interoperability by maintaining the three-part structure (trap data, core data, and LOI/OC data) and linking by SampleCode/Depth.
- Preserve provenance and calibration details (d13C calibrations, OC conversion factor, CRS chronology method) to enable correct interpretation and reanalysis.
- Track data quality flags and blanks to communicate processed completeness to data users.
- Maintain metadata alignment with the described methods for future integration with other lake sediment datasets and longitudinal studies.