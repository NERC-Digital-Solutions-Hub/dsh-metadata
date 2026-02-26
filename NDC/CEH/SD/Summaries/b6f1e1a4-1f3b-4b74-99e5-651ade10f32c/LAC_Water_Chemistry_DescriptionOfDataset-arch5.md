# LAC water chemistry_dataset.csv

## Overview
- Datasets record lake water chemistry from multiple regions (Norway, Greenland, Russia during ice cover; Alaska during ice-free periods).
- Sampling: one sample per lake from the upper 1 meter of the water column at the deepest point of each lake.

## Provenance and creators
- Created by Erika Whiteford, Loughborough University.

## Experimental design / sampling regime
- One lake sample per site.
- Sampling occurs during ice-covered periods (Norway, Greenland, Russia) or ice-free periods (Alaska).

## Collection / generation / transformation methods
- Water chemistry analyzed colorimetrically using standard methods based on color development from known standard concentrations.
- Raw absorbance at specified wavelengths recorded; standard curves used to calculate concentrations.
- Data initially recorded in lab notebooks and transferred to an Excel data file.

## Abbreviations and key variables
- Includes: TP (Total Phosphorus), SRP (Soluble Reactive Phosphorus), TN (Total Nitrogen), NO3- (Nitrate), NH4+ (Ammonium), Chl a (Chlorophyll a), SiO2 (Silicate), Na+ (Sodium), Mg2+ (Magnesium), K+ (Potassium), Ca2+ (Calcium), Cl- (Chloride), SO4^2- (Sulfate), DOC (Dissolved Organic Carbon), Total Alkalinity.
- BDL indicates below detectable level.

## Analytical methods
- DOC, SRP, SiO2, NO3-, NH4+, Na+, K+, Mg2+, Ca2+, Cl-, and SO4^2- filtered in the field through pre-combusted 0.7 µm GF/F filters; unfiltered water collected for TP, TN, and total alkalinity.
- Samples kept cold and dark in the field, typically analyzed within 8 hours; stored at 4°C in the dark until analysis.
- TP, SRP, NH4+, NO3-, and SiO2 analyzed by established methods (Mackereth et al. 1989; Koroleff 1983 modification by Qualls 1989).
- TN analyzed by Environment Agency (UK) and J. Saros, USA; total alkalinity by Golterman et al. (1978).
- DOC analyzed by Ptcatalysed combustion after acidification; instrumentation: Shimadzu TOC-V CSN.
- Chlorophyll a measured by spectrophotometry after filtration; pigments analyzed by HPLC per Leavitt and Hodgson (2001).

## Calibration and quality control
- Regular checks for machine drift.
- Standard curves checked for linearity; curves adjusted if needed.
- Absorbance values below detection limits checked for reliability.
- Calculations from quadratic equations verified; cross-check with previous lake data at same locations.

## Data format and structure
- Stored as a .csv file.
- Core structure includes: Region, Lake code, Date of collection, TP (ug/L), SRP (ug/L), TN (ug/L), NO3-N (ug/L), NH4-N (ug/L), SiO2 (mg/L), Sodium (mg/L), Potassium (mg/L), Magnesium (mg/L), Calcium (mg/L), Chloride (mg/L), Sulphate (mg/L), Total Alkalinity (meq/L), Chlorophyll a (ug/L), DOC (ppm).
- Values use standard units (e.g., µg/L, mg/L, ppm, meq/L); BDL used where below detection.

## Data governance, sharing and updates
- Documented methodological provenance, standard references, and QC steps support data traceability and reuse.
- Clear metadata structure facilitates integration with other datasets and future updates or expansions (supporting data stewardship responsibilities for discoverability and governance).

## References (methodological basis)
- Golterman, H. L., et al. 1978. Methods for physical and chemical analysis of fresh waters.
- Jeffrey, S. W., and Humphrey, G. F. 1975. Chlorophyll extraction and quantification.
- Koroleff, F. 1983. Methods of seawater analysis (persulfate oxidation).
- Leavitt, P. R., and Hodgson, D. A. 2001. Sedimentary pigments; LC/HP LCA references.
- Mackereth, F. J. H., et al. 1989. Water Analysis methods for limnologists.
- Qualls, R. G. 1989. Determination of nitrogen and phosphorus via persulfate oxidation.