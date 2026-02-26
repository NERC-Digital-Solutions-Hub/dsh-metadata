# LAC water chemistry_dataset.csv

## Overview
- Dataset created by Erika Whiteford, Loughborough University.
- Focus: lake water chemistry across multiple regions (Norway, Greenland, Russia, Alaska).
- Sampling design: single sample per lake, collected from the upper 1 m at the deepest point; timing varies with ice cover (ice-covered or ice-free periods).

## Sampling design and collection
- Water collected from the upper 1 m of the water column at the deepest point of each lake.
- One sample collected per lake.
- Regions include ice-covered and ice-free periods (locations listed in metadata).

## Analytical methods and quality control
- Colourimetric analyses using standard curves; raw absorbance values recorded and converted to concentrations via standard curves.
- Filtration and sampling:
  - DOC, SRP, SiO2, NO3-, NH4+, Na+, K+, Mg2+, Ca2+, Cl-, SO42- filtered in the field through pre-combusted 0.7 µm GF/F filters.
  - TP, TN, total alkalinity analyzed from unfiltered water.
  - Samples kept cold and dark in the field; typically returned to the lab within 8 hours; stored at 4°C in the dark until analysis.
- Laboratory analyses:
  - Water chemistry analyzed following established methods (Mackereth et al. 1989; Koroleff 1983; Golterman et al. 1978).
  - DOC measured by Pt-catalyzed combustion after acidification and CO2 sparging; analyzed on a Shimadzu TOC-V CSN.
  - Chlorophyll a measured by filtration and spectrophotometry (Jeffrey & Humphrey 1975) after pigment extraction; pigments measured by HPLC (Leavitt & Hodgson 2001; McGowan et al. 2012).
  - Chlorophyll a samples stored at -20°C; DOC samples stored as specified; other chemicals stored at 4°C, dark.
- Calibration and QC:
  - Regular checks for machine drift; standard curves validated and adjusted if necessary.
  - Absorbance checked against detection limits; quadratic calculations checked for errors.
  - Water chemistry values cross-validated with previous samples from the same locations.

## Data format, structure, and units
- File format: .csv
- Columns include:
  - Region (region/country), Lake code (lake identifier), Date of collection (DD/MM/YY)
  - TP (µg/L), SRP (µg/L), TN (µg/L), NO3-N (µg/L), NH4-N (µg/L), SiO2 (mg/L)
  - Sodium (Na+, mg/L), Potassium (K+, mg/L), Magnesium (Mg2+, mg/L), Calcium (Ca2+, mg/L)
  - Chloride (Cl-, mg/L), Sulphate (SO4 2-, mg/L), Total Alkalinity (meq/L)
  - Chlorophyll a (µg/L), DOC (ppm)
- Abbreviations defined (e.g., TP, SRP, TN, NO3-N, NH4-N, Chl a, SiO2, DOC)
- Notations:
  - BDL indicates below detectable level

## Data governance and sharing
- Data are stored in a public CSV format with accompanying methodological details.
- Metadata includes location, sampling date, parameter definitions, units, and data quality notes.
- Sharing of underlying datasets is acknowledged as necessary for transparency, with clear documentation to facilitate reuse.

## References and methods sources
- Golterman, H. L., Clymo, R. S., and Ohnstad, M. A. M. (1978): Methods for physical and chemical analysis of fresh waters.
- Jeffrey, S. W., and Humphrey, G. F. (1975): Chlorophyll a measurement equations.
- Koroleff, F. (1983): Persulfate digestion methods.
- Leavitt, P. R., and Hodgson, D. A. (2001): Sedimentary pigments; applied in pigment analysis.
- Mackereth, F. J. H., et al. (1989): Water analysis methods.
- McGowan, S., et al. (2012): Studies on algal community change.
- Qualls, R. G. (1989): Determination of total nitrogen and phosphorus using persulfate oxidation.