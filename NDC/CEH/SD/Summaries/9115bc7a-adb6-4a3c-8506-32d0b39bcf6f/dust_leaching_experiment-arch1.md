# Dust leaching

## Overview
- Dataset records the elemental composition of filtered water samples from an experiment testing dust addition across different water types.
- Location: KISS research station, Kangerlussuaq, West Greenland; lake SS903 (coordinates provided).
- Experiment duration: started April 2017 and continued for 63 days.
- Samples were filtered (GF/F) and analyzed by ICP-MS and ion chromatography at the British Geological Survey laboratories (Keyworth).
- Purpose: determine which elements leach out of dust in different water types.
- Principal investigators/analysts: Suzanne McGowan, Amanda Burson (conductors); Michael Watts (analyses).

## Experimental design and sampling regime
- Fully factorial design with two factors: dust (dust added (+) vs no dust (-)) and water type (four levels: D, A, N, B).
- Replication: four replicates per treatment combination.
- Water-type definitions:
  - D: deionised water autoclaved to eliminate microbes.
  - A: abiotic lake water filtered to remove microbes.
  - N: nanobiotic lake water filtered to 0.7 μm.
  - B: biotic lake water filtered to remove zooplankton (200 μm mesh).
- Incubation conditions: 10°C; 16:8 light:dark cycle; photon irradiance ~40 μmol m⁻² s⁻¹ PAR.
- Sampling times: initialization (0 days), 1 day, 7 days, and 63 days (dataset labeled as 40 for the final time point).
- End of incubation: entire sample filtered; filtered water analyzed and stored refrigerated.

## Analytical methods
- Inductively Coupled Plasma Mass Spectrometry (ICP-MS): Agilent 8900 series; collision cell in He mode for most elements; O2 with MS/MS for P, S, As, Se to measure oxide products.
- Ion Chromatography (IC): Dionex ICS5000; anions detected by suppressed conductivity; separation using AG19/AS19 columns with KOH eluent (10–100 mM).
- Units and detection limits: reported in the accompanying spreadsheet; measurements below detection limit indicated as <n.
- Quality controls: QC standards run at the start and end of each run and after no more than every 20 samples.
- Laboratory accreditation: ISO/IEC 17025.

## Data structure and contents
- Dataset size: 129 rows (128 samples + header) and 71 columns.
- Key columns:
  - Code descriptions and treatments (for water_type and Dust), Replicate, Time point.
  - Measured concentrations for multiple elements (e.g., Ca, Mg, Na, K, Cl, NO3, NO2, SO4, F, P, S) with their respective measurement methods (ICP-MS or IC).
- The column structure includes coding for treatment and water type:
  - Water_type: D, A, N, B.
  - Dust: + or -.
  - Replicate: 1–4.
  - Time: 0, 1, 7, or 40 (final time point; corresponds to 63 days of incubation).
- Units are provided in the dataset metadata for each element (e.g., mg/L, μg/L, etc.).

## Quality control and data provenance
- Detection limits noted in the spreadsheet; values below LD are marked as <n.
- QC standards analyzed at defined intervals to ensure accuracy.
- Data and analyses align with ISO 17025 standards, indicating formal laboratory quality management.

## Practical use and considerations
- Enables assessment of how adding dust affects leaching of a broad suite of elements across four water types and over time.
- Suitable for:
  - Detecting correlations between dust presence and element leaching.
  - Comparing leaching dynamics across abiotic, nanobiotic, and biotic water conditions.
  - Building predictive models of dust-driven leaching under varied water chemistry and microbial contexts.
- Analysis notes:
  - Handle non-detects appropriately (<LD) in statistical analyses.
  - The final time point labeled 40 corresponds to 63 days; interpret time axis accordingly.
  - Maintain data provenance by referencing sample codes and method annotations.