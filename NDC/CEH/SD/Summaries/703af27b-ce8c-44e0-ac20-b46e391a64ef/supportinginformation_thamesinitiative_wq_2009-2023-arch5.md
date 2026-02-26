# Brief description of the dataset

## Overview
- Weekly water quality monitoring dataset for eight sites along the River Thames and sixteen major tributaries.
- Coverage: March 2009 to December 2023.
- Parameters include nutrients (phosphorus species, nitrogen species), dissolved silica, temperature, pH, alkalinity, suspended solids, chlorophyll a, major dissolved anions and cations, and various metals (with varying availability over time).
- Data quality notes: missing data represented as blanks; samples below detection limits marked as nd (not detectable).

## Data scope and content
- Geographic scope: Thames River and major tributaries in the UK, monitored under the UK Centre for Ecology & Hydrology's Thames Initiative.
- Time span: 2009–2023 (with some parameters measured only during subset periods).
- Key parameters and units:
  - Physical/chemical: water temperature (°C), pH, conductivity (µS/cm), redox potential (mV), dissolved oxygen (% saturation and mg/L), dissolved organic carbon (mg/L), total dissolved nitrogen (mg/L, N), dissolved silica (mg/L Si), chlorophyll a (µg/L), ammonium (mg/L NH4+), Gran alkalinity (µEq/L).
  - Nutrients: total phosphorus (µg/L P), dissolved/soluble reactive phosphorus (µg/L P), total dissolved phosphorus (µg/L P).
  - Ions and metals: fluoride, chloride, nitrite, nitrate, sulfate (anions); sodium, potassium, calcium, magnesium, boron (cations); dissolved and total iron, manganese, zinc, copper; aluminum.
- Data organization: output presented site-ordered, then by date ascending.
- Supporting data: mean daily river flow data available from the National River Flow Archive; most sites near Environment Agency gauging stations; site locations documented in SiteLocations_2009_2023 (supporting documents).

## Collection, generation and analytical methods
- Sampling cadence: bulk samples collected weekly (Monday/Tuesday) from the main flow at each site.
- Field measurements (2013–present): water temperature, pH, conductivity, redox potential.
- In-field filtration: subsamples filtered through 0.45 μm membranes; dissolved measurements taken from filtered samples where applicable.
- Lab storage: samples stored in the dark at 4°C prior to analysis.
- Analytical methods (illustrative):
  - pH: lab measurement with calibrated pH meter (pH 4, 7, 10 buffers; traceable to NIST).
  - Gran alkalinity: acidimetric titration to pH 4 and 3 with 0.5N H2SO4.
  - Suspended solids: filtration and mass loss on pre-dried filter paper.
  - Chlorophyll a: filtration, acetone extraction, spectrophotometric measurement.
  - Phosphorus: TP and TDP via acidified persulfate digestion; SRP via molybdenum blue method.
  - Soluble reactive phosphorus: phosphomolybdate method (modified Murphy and Riley).
  - Dissolved reactive silicon: molybdate reaction with tin(II) chloride reduction; spectrophotometric measurement.
  - Ammonium: indophenol-blue colorimetric method.
  - DOC/TDN: thermal oxidation (2010) and then a 2011 switch to Elementar Cube instrumentation.
  - Major anions/cations: ICPOES analysis.
- Instrumentation references: Seal Auto Analyser 3, Beckman spectrophotometer, and standard analytical references cited for each method.
- Data completeness notes: some historical gaps in certain analyte sequences (see below).

## Data quality and governance
- Quality control: analyses (except suspended solids) conducted with reference Aquacheck QC standards.
- Documentation and metadata: measurements and units clearly defined; date/time format recorded as day/month/year and hour:minute for sampling time.
- Data integrity notes:
  - Missing data appear as blanks.
  - nd marks used for not detectable values.
  - Some parameters have restricted time frames due to method or instrument availability:
    - Major cations measured 2009–October 2016 (only).
    - Major dissolved metals measured August 2010–February 2013.
    - DOC/TDN measurement methods changed in 2010–2011.
- References for analytical methods provided for reproducibility and auditability.

## Data governance implications for Data Stewards
- Provenance and traceability: ensure metadata captures site, date, exact parameters, method used, instrument model, and any method changes over time.
- Metadata completeness: verify the SiteLocations_2009_2023 document and NRFA flow data linkage are accessible and versioned.
- Data versioning: track changes to methods or units (e.g., switch from Thermalox to Elementar Cube for DOC/TDN).
- Interoperability considerations: note historical gaps in parameter measurements and ensure downstream users understand time-bound availability.
- Data stewardship actions: maintain data storage with QA records, ensure access to supporting documents, and document any data corrections or recalibrations.

## Limitations and caveats
- Some datasets have incomplete time coverage for certain analytes due to instrument or methodological changes.
- Missing data and detection-limit handling are explicit, requiring careful interpretation for trend analyses.
- Mean daily river flow data referenced to external NRFA source; ensure continued accessibility and proper citation.

## References and supporting materials
- Method references for key analyses (phosphorus, silica, chlorophyll, pH, etc.) provided in the document.
- Supporting documents include SiteLocations_2009_2023 and NRFA flow data links.