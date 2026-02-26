# Brief description of the dataset

## Overview
- Weekly water quality monitoring data from eight River Thames sites and sixteen major tributaries, covering March 2009 to December 2023.
- Measured parameters include nutrients (phosphorus and nitrogen species), dissolved reactive silicon, temperature, pH, alkalinity, suspended solids, chlorophyll, major dissolved anions (fluoride, chloride, bromide, sulfate), major cations (sodium, potassium, calcium, magnesium, boron) (2009–2016), and trace metals (iron, manganese, zinc, copper) (2010–2013).
- Part of the UK Centre for Ecology & Hydrology’s Thames Initiative monitoring program.

## Dataset scope and contents
- Location: River Thames and major tributaries; data organized by monitoring site.
- Temporal coverage: March 2009 – December 2023 (with some parameters having shorter historical coverage).
- Data gaps: Missing data indicated as blanks; some samples below detection limits marked “nd” (not detectable).
- Site availability: Gauging context linked to Environment Agency stations; mean daily river flow data obtainable from the National River Flow Archive.

## Collection, measurement and analytical methods
- Sampling: Bulk samples collected from the main flow on Mondays or Tuesdays each week.
- Field measurements (2013–present): Water temperature, pH, conductivity, redox potential measured in the field using a Myron Ultrameter.
- Dissolved oxygen: Measured in the field after sampling (since July 2018) with a YSI ProSolo probe.
- Filtration: Subsamples filtered in the field through 0.45 µm membranes; samples stored at 4°C in the dark prior to analysis.
- Laboratory analyses:
  - pH: Laboratory pH meter, buffered and calibrated against standard solutions.
  - Alkalinity: Acidimetric titration to pH 4 and 3.
  - Suspended solids: Filtration, drying, and mass determination.
  - Chlorophyll a: Filtration, acetone extraction, and spectrophotometric quantification.
  - Phosphorus: Total and dissolved phosphorus via digestion and colorimetric methods.
  - Soluble reactive phosphorus (SRP): Colorimetric molybdenum blue method after filtration.
  - Dissolved reactive silicon: Molybdate reaction followed by reduction and spectrophotometry.
  - Ammonium: Indophenol-blue colorimetric method.
  - Dissolved organic carbon and total dissolved nitrogen: Thermal oxidation (until 2010) and Elementar system (from 2011).
  - Anions (fluoride, chloride, nitrite, nitrate, sulfate): Ion chromatography.
  - Cations (dissolved and total): Acidification followed by ICP-OES.
- Quality assurance: All analyses (except suspended solids) run with reference Aquacheck QC standards.

## Data structure, values, and units
- Date/time: Day/Month/Year; sampling time provided as hour:minute.
- Concentration definitions:
  - Total phosphorus = dissolved + acid-extractable particulate phosphorus in unfiltered samples.
  - SRP = filterable reactive phosphorus.
  - Datasets include both dissolved and total nutrient and metal forms as appropriate.
- Units (selected examples):
  - Temperature: degrees Celsius; pH (dimensionless); alkalinity: µe q/L.
  - Suspended solids: mg/L (dry solids).
  - SRP, TP, TDP: µg P/L.
  - Ammonium: mg NH4+/L.
  - Chlorophyll a: µg/L.
  - Major ions and metals: mg/L or µg/L as specified.
  - Conductivity: µS/cm; redox potential: mV; DO: % saturation or mg/L.
- Data ordering: Monitoring site order, then ascending date.

## Quality control and metadata
- Data quality: All analyses (except suspended solids) accompanied by Aquacheck QC standards.
- Metadata completeness: Supporting documents include SiteLocations_2009_2023; daily river flow context from NRFA; some metadata detail may be found in those materials.
- Data handling: Missing values and detection limits explicitly indicated in the dataset.

## Data availability and access
- Flow data: Mean daily river flow available from the National River Flow Archive.
- Gauging references: Sites near Environmental Agency gauging stations; relevant gauging stations specified in supporting documents.
- Data provenance: Collected under the Thames Initiative monitoring program; analytical methods and references provided for reproducibility.

## Use and interpretation notes
- Data interpretation should consider:
  - Periods with missing data and instrument or sampling issues.
  - Differences between dissolved vs total forms for nutrients and metals.
  - Changes in measurement methods over time (e.g., TOC/TN instrumentation).
  - The near-real-time applicability of field measurements vs laboratory-verified values.
- For policy and monitoring framework work, the dataset supports trend analysis, nutrient and metal loading assessments, chlorophyll dynamics, and overall water quality status across multiple sites over a substantial time frame.

## References
- Eisenreich, S. J., Bannerman, R. T., & Armstrong, D. E. (1975). A simplified phosphorus analytical technique.
- Leeks, G. J. L., Neal, C., Jarvie, H. P., Casey, H., & Leach, D. V. (1997). The LOIS river monitoring network: strategy and implementation.
- Marker, A. F. H., Nusch, E. A., Rai, H., & Riemann, B. (1980). Measurement of photosynthetic pigments in freshwater.
- Mullin, J. B., & Riley, J. P. (1955). Colorimetric determination of silicate.
- Murphy, J., & Riley, J. P. (1962). Phosphorus determination in natural waters.
- Neal, C., Neal, M., & Wickham, H. (2000). Phosphate measurement in natural waters.