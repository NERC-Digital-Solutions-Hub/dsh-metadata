# Brief description of the dataset

## Overview
- Weekly water quality monitoring dataset for eight sites along the River Thames and sixteen major tributaries.
- Coverage: March 2009 – December 2023.
- Measured parameters include phosphorus and nitrogen species, dissolved reactive silicon, water temperature, pH, Gran alkalinity, suspended solids, chlorophyll, major dissolved anions (fluoride, chloride, bromide, sulfate), major cations (sodium, potassium, calcium, magnesium, boron) (measured 2009–Oct 2016), and dissolved/total concentrations of iron, manganese, zinc, and copper (measured 2010–Feb 2013).
- Part of the UK Centre for Ecology & Hydrology’s Thames Initiative monitoring programme.
- Missing data appear as blanks; samples below detection limits marked nd (not detectable).

## Data scope and provenance
- Data source: Thames Initiative monitoring programme coordinated by CEH.
- Flow data: mean daily river flow data available from the National River Flow Archive (NRFA).
- Site references: relevant gauging stations near most sites; site specifics provided in supporting documentation (SiteLocations_2009_2023).

## Collection and sampling methods
- Bulk samples collected weekly from the main river flow (Monday or Tuesday).
- In-field measurements (March 2013–present): water temperature, pH, conductivity, redox potential.
- Dissolved oxygen measured in-field (since July 2018) using a YSI ProSolo probe.
- Subsamples filtered in the field through 0.45 μm membranes; samples stored in the lab at 4°C in the dark prior to analysis.

## Analytical methods and laboratory procedures
- pH: measured in the lab with a calibrated pH meter (NIST-traceable buffers).
- Gran alkalinity: determined by acidimetric titration to pH 4 and 3.
- Suspended solids: determined by filtration, drying, and reweighing.
- Chlorophyll a: extracted from filtered samples and quantified spectrophotometrically after acetone extraction.
- Phosphorus: total phosphorus (TP) and total dissolved phosphorus (TDP) by digestion and colorimetric quantification; soluble reactive phosphorus (SRP) by colorimetry.
- Dissolved reactive silicon: molybdate reaction followed by reduction and spectrophotometry.
- Ammonium: indophenol-blue colorimetric method.
- Dissolved organic carbon (DOC) and total dissolved nitrogen (TDN): thermal oxidation (until 2010) and a later Elementar Cube system (from 2011).
- Major dissolved anions: fluoride, chloride, nitrite, nitrate, sulfate by ion chromatography.
- Cations: total (unfiltered) and dissolved (filtered) concentrations by ICP-OES after acidification.
- Quality control: analyses (except suspended solids) run with Aquacheck QC standards.

## Variables, units and data structure
- Date/time: day/month/year; sampling time in hour:minute.
- Concentrations and measurements reported with specified units:
  - Phosphorus species and nitrogen species: μg P/L or mg N/L (varies by analyte).
  - Dissolved/total metals (Fe, Mn, Zn, Cu, etc.): μg/L or mg/L (depending on analyte).
  - Chlorophyll a: μg/L.
  - Chlorophyll-related parameters, alkalinity, chlorophyll and nutrients have detailed unit definitions within the dataset documentation.
  - Temperature: °C; pH (dimensionless); conductivity: μS/cm; redox potential: mV; dissolved oxygen: % saturation and mg/L.
  - Other parameters include various dissolved and total anions/cations with their respective units as listed in the dataset description.

## Data quality, documentation and updates
- Data presented in monitoring site order, then ascending date order.
- Data quality controls applied via QC standards (Aquacheck) for all analyses except suspended solids.
- Comprehensive methodological documentation included (collection, analytical methods, and references) to support reproducibility and auditability.

## Usage considerations and implications for data leaders
- Longitudinal coverage (2009–2023) enables trend analysis across riverine systems and tributaries, with multiple parameters enabling nutrient, metal, and productivity assessments.
- Gaps may exist due to missing data and earlier measurement windows (e.g., certain metals measured only during specific periods).
- Data alignment with external flow data (NRFA) supports combined hydro-chemical analyses and load estimations.
- Metadata and supporting documents (e.g., SiteLocations_2009_2023) are essential for precise site mapping and contextual interpretation.
- Clear documentation of units, measurement techniques, and quality controls aids in cross-project data integration and governance.

## References
- Eisenreich, S. J., Bannerman, R. T., & Armstrong, D. E. (1975). A simplified phosphorus analytical technique.
- Leeks, G. J. L., Neal, C., Jarvie, H. P., Casey, H., & Leach, D. V. (1997). The LOIS river monitoring network: strategy and implementation.
- Marker, A. F. H., Nusch, E. A., Rai, H., & Riemann, B. (1980). The measurement of photosynthetic pigments in freshwaters.
- Mullin, J. B., & Riley, J. P. (1955). The colorimetric determination of silicate.
- Murphy, J., & Riley, J. P. (1962). A modified single solution method for determination of phosphorus in natural waters.
- Neal, C., Neal, M., & Wickham, H. (2000). Phosphate measurement in natural waters: interference issues.