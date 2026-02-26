# LAC water chemistry_dataset.csv

## Overview
- A dataset capturing lake water chemistry to monitor environmental health and policy performance over time.
- Aims to provide standardized, comparable measurements across multiple lakes and regions.

## Creator
- Erika Whiteford, Loughborough University

## Experimental design / sampling regime
- Water collected from the upper 1 meter of the water column at the deepest point of each lake.
- Sampling periods:
  - Ice cover for Norway, Greenland, Russia.
  - Ice-free periods for Alaska.
- One sample collected per lake.

## Collection / generation / transformation methods
- Water chemistry analyzed colorimetrically using standard methods based on color development from known standards.
- Standard curves recorded in lab notebooks; raw absorbance at specified wavelengths captured for each protocol.
- Data transferred to Excel; standard curve used to calculate concentrations.

## Abbreviations / variables
- TP: Total Phosphorus
- SRP: Soluble Reactive Phosphorus
- TN: Total Nitrogen
- NO3-: Nitrate
- NH4+: Ammonium
- Chl a: Chlorophyll a
- SiO2: Silicate
- Na+: Sodium
- Mg2+: Magnesium
- K+: Potassium
- Ca2+: Calcium
- SO4 2-: Sulfate
- Cl-: Chloride
- DOC: Dissolved Organic Carbon
- Total Alkalinity: meq/L

## Analytical methods
- Analytes filtered in the field (0.7 µm GF/F) for DOC, SRP, SiO2, NO3-, NH4+, Na+, K+, Mg2+, Ca2+, Cl-, SO4 2-; TP, TN, and total alkalinity analyzed from unfiltered water.
- Samples kept cold and dark in the field; typically analyzed within 8 hours in the lab.
- Lab analyses:
  - TP, SRP, NH4+, NO3-, SiO3: Mackereth et al. (1989) methods (with Koroleff modification by Qualls 1989 for TN)
  - TN: Environment Agency (UK) and University of Maine methods
  - Total alkalinity: Golterman et al. (1978)
  - DOC: P-catalyzed combustion after removing inorganic carbon; Shimadzu TOC-V CSN
  - Chl a: Spectrophotometric method following Jeffrey & Humphrey (1975)
  - Algal pigments: HPLC per Leavitt & Hodgson (2001) as in McGowan et al. (2012)
- Sample preservation: DOC preserved with H2SO4; Chl a filters stored at -20 C; general sample storage at 4 C in the dark.

## Calibration steps
- Regular checks for machine drift.
- Standard curves checked for linearity; adjustments made as needed.
- Absorbance values checked against detection limits; quadratic calculations verified.

## Nature and units of recorded values
- Concentrations in SI units:
  - TP, SRP, TN, NO3-, NH4+, Chl a: µg/L
  - SiO2, Na+, Mg2+, K+, Ca2+, Cl-, SO4 2-: mg/L
  - DOC: ppm
  - Total Alkalinity: meq/L

## Quality control
- Ongoing validation of standard curves and raw spectrophotometric readings against the standard curve.
- Handling of below-detection-level (BDL) values.
- Cross-checks of water chemistry values with prior samples from the same locations.

## Format of stored data
- .csv file.

## Details of data structure
- Region: Region or country where the lake is located.
- Lake code: Identifying code for the lake.
- Date of collection: Date sample was taken (DD/MM/YY).
- TP (ug/L)
- SRP (ug/L); BDL indicates below detectable level.
- TN (µg/L)
- NO3-N (µg/L)
- NH4-N (µg/L); BDL indicates below detectable level.
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

## References (methods)
- Golterman, H.L., et al., 1978: Methods for physical and chemical analysis of fresh waters.
- Jeffrey, S.W., & Humphrey, G.F., 1975: Chlorophyll a methods.
- Koroleff, F., 1983: Persulfate digestion methods (seawater analysis).
- Leavitt, P.R., & Hodgson, D.A., 2001: Sedimentary pigments.
- Mackereth, F.J.H., et al., 1989: Water Analysis methods.
- McGowan, S., et al., 2012: Humans and climate drivers of algal change.
- Qualls, R.G., 1989: Persulfate oxidation for nitrogen and phosphorus determination.