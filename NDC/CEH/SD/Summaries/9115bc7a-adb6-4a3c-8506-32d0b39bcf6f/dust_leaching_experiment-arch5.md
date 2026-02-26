# Dust leaching

- The dataset contains the elemental composition of filtered water samples from an experiment assessing how dust additions affect leaching of elements in different water types.
- Location and time: KISS research station, Kangerlussuaq, West Greenland; lake SS903 (coordinates provided); experiment ran from April 2017 for 63 days.
- Researchers: Suzanne McGowan and Amanda Burson conducted the experiment; Michael Watts performed analyses.
- Sample processing: water samples were filtered (GF/F) before analysis; samples stored refrigerated.

## Experimental design and sampling

- Design: fully factorial with two factors (dust: with dust (+) or no dust (-); water type: four treatments: D, A, N, B) and four replicates.
- Water type definitions:
  - D: deionised water autoclaved
  - A: abiotic lake water filtered to remove microbes, then autoclaved
  - N: nanobiotic lake water filtered to 0.7 µm
  - B: biotic lake water filtered to remove zooplankton (200 µm mesh)
- Incubation conditions: 10°C, 16:8 light:dark cycle, ~40 μmol photons m-2 s-1 PAR.
- Sampling points: 0 days, 1 day, 7 days, and 63 days (labelled as 40 in the dataset).
- End of incubation: entire sample filtered and analyzed; samples stored in refrigerator.

## Analytical methods

- Elemental analysis: Inductively coupled plasma mass spectrometry (ICP-MS) using an Agilent 8900 series instrument; collision-reduced mode (He) for most elements; for P, S, As, Se, use O2 with MS/MS for oxide product ion measurement.
- Anion analysis: Ion chromatography (Dionex ICS5000) with suppressed conductivity detection.
- Units: all values reported in the accompanying spreadsheet (units vary by analyte; see dataset for specifics).
- Quality control: detection limits noted in the spreadsheet; measurements below detection limit labeled as <n; QC standards run at the start and end of each run and approximately every 20 samples; ISO/IEC 17025 accreditation implied for the laboratories.

## Data structure and metadata

- Dataset size: 129 rows (128 samples + header) and 71 columns.
- Key structure details:
  - Metadata columns include Water_type (D, A, N, B), Dust (+/−), Replicate (1–4), Time point (sampling end-point), and analyte-specific data.
  - Analyte columns cover a wide range of elements (e.g., Ca, Mg, Na, K, Cl, NO3, NO2, SO4, F, P, S) with corresponding units and measurement methods (ICP-MS or Ion-Chromatography).
  - Each row represents a single sample and includes data for multiple elements, with method and unit information embedded in the metadata.
- Data dictionary: the dataset includes a detailed mapping of column codes to experimental treatments and analyte measurements.

## Quality control and data quality

- Detection limits are specified in the dataset; values below detection are flagged accordingly.
- Instrumental and methodological QC procedures are documented (start/end runs and periodic standards).
- Laboratories are ISO/IEC 17025 accredited, supporting data credibility and traceability.

## Data accessibility and reuse

- The dataset is described with a comprehensive metadata structure, including experimental design, sampling regime, and analytical methods, facilitating reuse and cross-study comparisons.
- Clear documentation of sample treatments, time points, and units supports reproducibility and integration into data portals or repositories.

## Data stewardship considerations and challenges

- Stewardship focus areas:
  - Maintain explicit links between sample identifiers and experimental design (dust treatment, water type, replicate, time point).
  - Preserve unit conventions and measurement methods for each analyte to ensure interoperability across systems.
  - Include detection limits and QC records to support data quality assessments.
- Potential challenges:
  - Managing a large, multi-method dataset (ICP-MS and IC) with numerous analytes and unit types.
  - Ensuring consistent metadata propagation when uploading to data portals or catalogues.
  - Handling legacy or non-interoperable formatting if integrating with other systems or datasets.