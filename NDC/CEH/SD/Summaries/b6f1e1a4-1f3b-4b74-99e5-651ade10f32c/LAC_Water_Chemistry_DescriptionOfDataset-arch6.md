# LAC water chemistry_dataset.csv

## Overview
- A dataset of lake water chemistry for multiple circumpolar regions (Norway, Greenland, Russia, Alaska).
- Created by Erika Whiteford, Loughborough University.
- Each lake contributes a single sample from the upper 1 m of the water column, collected during either ice-covered or ice-free periods.

## Experimental design and sampling
- Sampling scope: lakes located in Norway, Greenland, Russia, and Alaska.
- Sampling regime: one sample per lake from the deepest point of the lake during the specified seasonal condition (ice cover or ice-free).
- Region and lake identifiers recorded for each sample.

## Methods and measurements
- Analytical approach: colorimetric analysis with standard curves; raw absorbance readings captured and used with standard curves to derive concentrations.
- Field processing: filtration of most analytes (0.7 µm GF/F filters) with unfiltered water collected for TP, TN, and total alkalinity.
- Sample handling: samples kept cold and dark in the field; lab storage at 4°C in the dark until analysis (typically within 8 hours for most analyses; within ~3 days for DOC; Chl a stored at -20°C after filtration).
- Analytes and methods (examples):
  - TP, SRP, NH4+, NO3-, SiO2 analyzed per standard limnology methods (Mackereth 1989; Koroleff 1983; Qualls 1989; Golterman 1978; Jeffrey & Humphrey 1975; Leavitt & Hodgson 2001; McGowan et al. 2012).
  - Chlorophyll a measured spectrophotometrically following Jeffrey & Humphrey (1975); algal pigments via HPLC (Leavitt & Hodgson 2001; McGowan et al. 2012).
  - DOC measured by combustion after acid preservation.
  - Total alkalinity determined by established methods (Golterman et al. 1978; Koroleff 1983).
- Calibration: routine checks for machine drift and standard curve validity; adjustments made as needed.

## Data structure and content
- File format: .csv
- Key fields:
  - Region (region/country)
  - Lake code (lake identifier)
  - Date of collection (DD/MM/YY)
  - TP (ug/L)
  - SRP (ug/L)
  - TN (ug/L)
  - NO3-N (ug/L)
  - NH4-N (ug/L)
  - SiO2 (mg/L)
  - Sodium (mg/L)
  - Potassium (mg/L)
  - Magnesium (mg/L)
  - Calcium (mg/L)
  - Chloride (mg/L)
  - Sulphate (mg/L)
  - Total Alkalinity (meq/L)
  - Chlorophyll a (ug/L)
  - DOC (ppm)
- Data conventions:
  - BDL indicates below detectable level for applicable fields.
  - Units provided in SI or standard chemical units as specified above.
- Data quality: deliberate checks against linear standard curves, absorbance within calibration range, cross-checks with prior sampling data from same locations.

## Data quality and quality control
- Ongoing verification of standard curves and instrument drift.
- Absorbance readings checked against the standard curve; deviations corrected as needed.
- Values checked for detection limits and consistency with prior lake data at the same sites.

## Data storage and format details
- Primary storage format: CSV
- Sample handling and storage conditions detailed (cold, dark, specific preservation for DOC and Chl a).
- Chl a samples filtered and stored at -20°C until analysis; DOC preserved with sulfuric acid and measured after CO2 sparging.

## References and methodological framework
- Methods and standard references underpinning measurements (examples):
  - Golterman, H.L., Clymo, R.S., Ohnstad, M.A.M. (1978)
  - Jeffrey, S.W., Humphrey, G.F. (1975)
  - Koroleff, F. (1983)
  - Leavitt, P.R., Hodgson, D.A. (2001)
  - Mackereth, F.J.H., et al. (1989)
  - Qualls, R.G. (1989)
  - McGowan, S., et al. (2012)
- These sources document analytical protocols for TP, SRP, TN, NO3-, NH4+, SiO2, DOC, chlorophyll a, and related measurements used in this dataset.