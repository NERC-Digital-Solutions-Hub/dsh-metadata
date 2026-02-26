# Dust leaching

- Overview
  - Dataset provides elemental composition of filtered water samples from a dust-leaching experiment.
  - Location: KISS research station, Kangerlussuaq, West Greenland; lake SS903 coordinates provided.
  - Duration: 63 days, started April 2017.
  - Purpose: determine which elements leach out of dust in different water types.
  - Experimental conductors and analysts: Suzanne McGowan and Amanda Burson conducted the experiment; Michael Watts conducted the analyses.

- Experimental design and data collection
  - Factorial design with two factors: dust (with dust (+) or no dust (-)) and water type (four types: D, A, N, B).
  - Fully factorial design with four replicates per treatment combination.
  - Water types:
    - D: deionised water autoclaved to remove microbes
    - A: abiotic lake water filtered and autoclaved to remove microbes
    - N: nanobiotic lake water filtered
    - B: biotic lake water filtered to remove zooplankton
  - Dust treatment: presence or absence of dust
  - Incubation conditions: 10°C, 16:8 light:dark cycle, approximately 40 μmol photons m-2 s-1 PAR
  - Sampling timepoints: 0 days (initialization), 1 day, 7 days, and 63 days (labelled as 40 in the dataset)
  - Post-incubation processing: entire sample filtered through GF/F paper; filtered water stored for analysis

- Analytical methods
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS, Agilent 8900) for most elements
    - Collision cell operated in He mode; for P, S, As, Se, O2 is used with MS/MS to measure oxide product ions
  - Ion Chromatography (ICS5000) for anions (e.g., Cl-, NO3-, SO4^2-, etc.)
  - Quality control and data limits
    - Detection limits noted in the dataset; values below detection limit marked as <n
    - QC standards analyzed at the start, end, and approximately every 20 samples
    - Laboratories accredited to ISO Standard 17025

- Nature and units of recorded values
  - Units are specified in the dataset (spreadsheet/table accompanying the data)
  - Measured variables include a wide suite of elements and ions (e.g., Ca, Mg, Na, K, Cl-, NO3-, NO2-, SO4^2-, F-, PO4^3-, Si, SiO2, etc.)
  - Some measurements reported in mg/L (major elements) and others in µg/L (trace elements)

- Details of data structure
  - Dataset structure: 129 rows total (128 samples + 1 header row) and 71 columns
  - Key metadata fields:
    - Code and Code for treatment (Dust and Water_type)
    - Water_type: D, A, N, B
    - Dust: + or -
    - Replicate: 1–4
    - Time point: sampling end point (0, 1, 7, 40)
    - Elemental/ion measurements (e.g., Ca_mg/L, Mg_mg/L, Na_mg/L, K_mg/L, Cl-_mg/L, NO3-_mg/L, NO2-_mg/L, SO42-_mg/L, F-_mg/L, Total P_mg/L, Total S_mg/L, Si_mg/L, SiO2_mg/L, and many trace elements in µg/L or µg/L ranges)
  - Column descriptions indicate technique (ICP-MS or Ion-Chromatography) for each measurement

- Data provenance and accessibility
  - Analyses performed at the British Geological Survey laboratories, Keyworth
  - Dataset includes a detailed data dictionary within the table, linking each column to its description, units, and measurement method
  - Experimental authors and responsible analysts are documented

- Relevance to data strategy and governance (Data Leaders perspective)
  - Demonstrates a well-documented data lifecycle: clear experimental design, provenance, analytical methods, QC, and ISO 17025-aligned practices
  - Provides a comprehensive data dictionary and structured metadata to support discoverability and re-use
  - Highlights the importance of recording measurement techniques and units consistently across a large, multi-variable dataset
  - Offers a model for managing complex, multi-factor environmental experiments with numerous measured parameters and replication
  - Potential considerations for data stewardship:
    - Ensure mapping of timepoint label (40) to actual day count is clearly documented for reuse
    - Maintain consistent units across records and document any unit conversions
    - Preserve links between meta fields (Dust, Water_type, Replicate, Time) and measured variables to enable robust filtering and analyses
    - Verify accessibility of detection limits and QC metadata for reproducibility and secondary analyses