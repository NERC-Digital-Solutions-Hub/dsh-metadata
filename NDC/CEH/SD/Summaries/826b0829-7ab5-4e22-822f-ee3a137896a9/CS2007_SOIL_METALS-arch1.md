# Soil metals 2007 [Countryside Survey], Great Britain

- A dataset of soil metal concentrations from Countryside Survey 2007 in Great Britain, using up to 256 1km squares (402 cores analysed) with data collected across 1km sampling squares and plots within each square.
- Focus on metal concentrations in topsoil (0-15 cm) from multiple cores and locations, enabling broad and country-level comparisons and trend analysis.

## Data file and columns

- File: CS2007_SOIL_METALS.csv
- Key location identifiers:
  - SQUARE: 1km square sampling site code
  - PLOT: Plot within each 1km square (one of 5 plots)
  - YEAR: Survey year
  - COUNTRY: England (ENG), Scotland (SCO), Wales (WAL)
  - COUNTY07: County or council area
  - LC07, LC07_NUM: ITE Land Class 2007 (categorical and numeric codes)
  - EZ_DESC_07: Countryside Survey Environmental Zone description
- Metals measured (ppm / mg/kg equivalents):
  - Cd, Cr, Cu, Ni, Pb, Zn, Al, Ti, Mn, As, Se, Mo, Hg
- Additional metadata:
  - Additional notes on data use, acknowledgments, and references

## Sampling design and data coverage

- Sampling strategy aligned with Countryside Survey’s statistical design:
  - Great Britain stratified by Land Classes to capture environmental gradients
  - 591 sample squares surveyed in 2007 (289 England, 107 Wales, 195 Scotland)
  - Soils collected from 0-15 cm, with locations standardized relative to Main Plot corners; later surveys used different corners but maintained spacing (2–3 m between surveys)
- Core sampling specifics:
  - 402 soil cores analysed for metals
  - From up to 2 cores per 1km square, randomly selected from the original 5 X-plots in the 1978 survey
- Coverage enables national statistics and country-level reporting, with power analyses guiding the number of samples for different analytes

## Laboratory methods and analytes

- Digestion and analysis:
  - Aqua Regia digestion (Standards method: The Standing Committee of Analysts 1986) for metal determinations
  - 2000 survey analyses by ICP-OES; 2007 enhanced with inductively coupled plasma mass spectrometry (ICP-MS) to expand analyte suite
  - Current CEH Lancaster standard: up to 27 analytes (including As, Hg, and the core metals Pb, Zn, Cu, Cd, Ni, Mn)
- Protocols and methods:
  - Detailed laboratory and field protocols described in the Countryside Survey soils manual
  - Analytical methods cross-checked and documented; re-analysis performed if issues identified

## Quality assurance and control

- QA and accreditation:
  - Laboratories accredited to ISO 17025 (UKAS)
  - QA framework and procedures documented in CS soils manual
- QC targets and procedures:
  - Total analytical error target: 20% (10% precision + 10% bias)
  - Actions for QC deviations:
    - If a QC standard falls outside the action limit or two successive QC standards exceed warning limits, associated data may be rejected
    - CRM results outside bias target may trigger data rejection
  - Post-analysis review: after 100 samples, potential recalibration of error targets for some determinands; potential reinstatement of previously rejected batches based on demonstrated capability
- Cross-checks and re-analyses:
  - Standard samples and blind replicates in analytical runs
  - Methods cross-checked when changes occurred; re-analyses conducted as needed

## Data usage, documentation, and references

- Acknowledgement required for all CS data use:
  - "Countryside Survey data owned by NERC - Centre for Ecology & Hydrology"
  - Countryside Survey © and database rights apply
- Key references and documentation:
  - Emmett et al. 2008 Countryside Survey: Soils Manual (CS Technical Report No. 3/07)
  - Emmett et al. 2008 Countryside Survey: Soils Manual details field and laboratory processing, QC, archiving, and data handling
  - Emmett et al. 2010 Countryside Survey: Soils Report from 2007 (for additional context)
  - Additional publications on ITE Land Classification and related methodologies (e.g., Bunce et al.)
  - Access to CS materials through Countryside Survey website and NERC/NERC-CEH repositories
- Data management and dissemination:
  - Protocols, cross-comparison results, power analyses, and statistical approaches are documented and archived (refer to CS2007 Soils Manual and related CS Technical Reports)

## Implications for data analysts

- Enables cross-country and land-class–level analyses of soil metal concentrations in Great Britain
- Suitable for correlation with environmental gradients (land class, environmental zones) and for trend analysis across campaigns
- Supports assessment of data quality and reproducibility through documented QA/QC procedures and ISO 17025 accreditation
- Requires proper acknowledgment and awareness of sampling design when modeling spatial patterns or scaling results to local levels due to the stratified sampling and 1km-square resolution