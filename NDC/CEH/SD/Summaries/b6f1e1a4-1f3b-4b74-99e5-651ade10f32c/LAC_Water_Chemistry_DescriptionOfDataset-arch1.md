# LAC water chemistry_dataset.csv

## Overview
- A dataset of lake water chemistry measurements compiled for multiple lakes across different regions.
- Each lake contributes a single sample, with detailed chemical analyses and supporting metadata.

## Dataset provenance
- Created by: Erika Whiteford, Loughborough University.

## Experimental design and sampling regime
- Water collected from the upper 1 meter of the water column at the deepest point of each lake.
- Sampling contexts: ice-covered lakes in Norway, Greenland, and Russia; ice-free periods in Alaska.
- Number of samples: 1 per lake.

## Collection / generation / transformation methods
- Chemical analyses conducted colourimetrically using standard methods; concentrations calculated from standard curves using raw absorbance data recorded in lab notebooks.
- Data transferred to an Excel file; standard curves applied to convert absorbance to concentrations.

## Abbreviations
- TP: Total Phosphorus
- SRP: Soluble Reactive Phosphorus
- TN: Total Nitrogen
- NO3-N: Nitrate
- NH4-N: Ammonium
- Chl a: Chlorophyll a
- SiO2: Silicate
- Na+: Sodium
- Mg2+: Magnesium
- K+: Potassium
- Ca2+: Calcium
- Cl−: Chloride
- SO4 2−: Sulphate
- DOC: Dissolved Organic Carbon

## Analytical methods
- DOC, SRP, SiO2, NO3−, NH4+, Na+, K+, Mg+, Ca+, Cl−, SO4 2−: filtered in the field through pre-combusted 0.7 µm GF/F filters; unfiltered water kept for TP, TN, and total alkalinity.
- In-field handling: samples kept cold and dark; typically analyzed within 8 hours; stored at 4°C in the dark until analysis (usually within 3 days for DOC).
- Measurements follow established methods (e.g., Mackereth 1989; Koroleff 1983; Jeffrey & Humphrey 1975; Leavitt & Hodgson 2001).
- Chlorophyll a: filtered water filtered onto 1.2 µm GF/C filter; stores at −20°C; measured spectrophotometrically.
- Algal pigments: measured with high-performance liquid chromatography (HPLC).

## Calibration steps
- Machine drift checked; standard curves adjusted as needed.
- Absorbance checks performed when readings approached detection limits; quadratic calculations validated.

## Nature and units of recorded values
- TP, SRP, TN, NO3−, NH4+: µg/L
- SiO2, Na+, Mg2+, K+, Ca2+, Cl−, SO4 2−: mg/L
- DOC: ppm
- Total Alkalinity: meq/L
- Chlorophyll a: µg/L
- BDL = below detectable level

## Quality control
- Linear standard curves verified; raw spectrophotometric readings aligned with curves.
- Checks for readings below detection limits.
- Calculations from quadratic equations checked for errors.
- Water chemistry values cross-validated against previous samples from the same locations.

## Format and structure of stored data
- File format: .csv
- Data structure:
  - Region (region/country)
  - Lake code (lake identifier)
  - Date of collection (DD/MM/YY)
  - TP (µg/L)
  - SRP (µg/L)
  - TN (µg/L)
  - NO3-N (µg/L)
  - NH4-N (µg/L)
  - SiO2 (mg/L)
  - Sodium (mg/L)
  - Potassium (mg/L)
  - Magnesium (mg/L)
  - Calcium (mg/L)
  - Chloride (mg/L)
  - Sulphate (mg/L)
  - Total Alkalinity (meq/L)
  - Chlorophyll a (µg/L)
  - DOC (ppm)

## Details of data structure
- Region: region or country where the lake is located
- Lake code: identifying code for the lake
- Date of collection: date of sampling
- Concentration columns for each measured parameter
- BDL entries indicate below-detectable levels

## References (methods sources)
- Golterman et al., 1978: Methods for physical and chemical analysis of fresh waters
- Jeffrey & Humphrey, 1975: Spectrophotometric equations for chlorophylls
- Koroleff, 1983: Persulfate digestion methods for nutrients
- Leavitt & Hodgson, 2001: Sedimentary pigments (HPLC)
- Mackereth et al., 1989: Water Analysis: revised methods for limnologists
- Qualls, 1989: Determination of total nitrogen and phosphorus via persulfate digestion
- McGowan et al., 2012; related references on algal drivers and environmental change