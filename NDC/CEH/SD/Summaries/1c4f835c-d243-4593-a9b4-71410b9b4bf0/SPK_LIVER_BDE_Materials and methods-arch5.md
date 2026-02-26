# Determination of PBDE concentrations in livers

- Context and provenance
  - Archived livers from dead sparrowhawks collected across Britain were used, originating from the Predatory Bird Monitoring Scheme.
  - The study period focused on birds dying between 1998 and 2009 from central England, directly east and within 250 km of the Welsh border, to minimise temporal and spatial confounding.
  - Selection was stratified into eight groups by sex (male/female), age (adult/juvenile), and body condition (starved/non-starved). The total analyzed set comprised 59 birds; group sizes ranged from 5 to 11.
  - Data collected at necropsy included provenance, collection date, age, sex, body weight, and a visual six-point body condition score. Tissues were collected, weighed, and archived at -20°C.
  - Some birds lacked whole liver/body weights due to trauma, scavenging, or non-recorded weights from taxidermists, introducing occasional missing body weight data.

- PBDE determination in livers (analytical methods)
  - Approximately 1 g of liver per bird was sampled from various parts to obtain a representative specimen, then homogenised.
  - Lipid content was determined gravimetrically; extracts were cleaned and prepared for analysis.
  - Gas Chromatography–Mass Spectrometry (GC-MS) was used with a 30 m CPSIL-8 CB column to quantify a suite of 30 PBDE congeners (tri- to octa-BDEs), excluding BDE-209 due to methodological limitations.
  - Calibration used seven PBDE standards over a linear range of 2.5–250 pg/µL.
  - Instrument detection limits (LoD) ranged approximately from 0.27 to 0.54 ng/g wet weight across congener groups.
  - Eight procedural blanks were analyzed with samples; sample concentrations were corrected for blank values.
  - Recovery corrections used 13 C12-labelled BDE congeners (28, 47, 99, 100, 153, 154, 183), with recoveries between 74.4% and 88.2%.
  - A QC standard comprising five PBDEs across tri- to hepta-homologue groups (2.5–250 pg/µL) was analysed with unknowns; batches were deemed acceptable if QC concentrations were within ±10% of expected values.

- Data handling and statistical analyses
  - All analyses were performed in Minitab 16.0.
  - General Linear Models (GLMs) were used to test whether age, sex, body condition, and breeding status explained variation in individual PBDE congeners, sum of PBDEs (ΣPBDEs), and liver characteristics (liver mass, liver % lipid).
  - Given potential triple interactions among body condition, age, and sex, age and body condition effects on liver BDE concentrations were examined separately for males and females.
  - PBDE concentrations were log-transformed and liver % lipid was arcsine square-root transformed to satisfy GLM assumptions (homogeneity of variance and normality).
  - Values below the LoD were treated using methods appropriate for censored data; when the proportion below LoD was less than 80% for a congener, non-detect values were interpolated following Hesel’s approach.
  - The study notes limitations related to incomplete data (e.g., missing body weights for some birds) and acknowledges that BDE-209 was not quantified with the employed method.

- Governance and data quality considerations for data stewards
  - Data derive from a long-term monitoring scheme with documented provenance and ethical considerations.
  - Detailed metadata accompany samples (collection site, date, sex, age, body condition, weight) enabling traceability and downstream reuse.
  - Rigorous QA procedures are described (blanks, recoveries, QC standards, and acceptance criteria), supporting data quality and comparability.
  - Transparency about non-detected values and methods for handling censored data aids reproducibility and proper interpretation of exposure assessments.
  - Limitations, such as missing body weights and exclusion of BDE-209, should be captured in data documentation to inform future analyses and data integration with other datasets.