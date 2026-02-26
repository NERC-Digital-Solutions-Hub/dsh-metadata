# Dust leaching

- Overview: A dataset of the elemental composition of filtered water samples from a dust leaching experiment. Dust was added or not added to different water types to determine which elements leach under varying conditions.

- Location and timeline:
  - Conducted at the KISS research station, Kangerlussuaq, West Greenland.
  - Lake SS903 used (coordinates provided in the dataset description).
  - Experiment started April 2017 and ran for 63 days.
  - Samples stored refrigerated after collection.

- Experimental design:
  - Factors: Dust (present + or absent -) and Water type (D: deionised/autoclaved; A: abiotic lake water; N: nanobiotic lake water; B: biotic lake water).
  - Design: Fully factorial with four replicates per treatment combination.
  - Incubation conditions: 10°C, 16:8 light:dark cycle, ~40 μmol photons m-2 s-1 PAR.
  - Sampling time points: 0 days, 1 day, 7 days, and 63 days (dataset labels 0, 1, 7, 40 respectively).
  - At the end of incubation, samples were filtered and analyzed.

- Analytical methods:
  - ICP-MS (Agilent 8900) used for most elements; collision cell in He mode, with O2 and MS/MS for P, S, As, Se to measure oxide ions.
  - Ion Chromatography (Dionex ICS5000) used for anions; detection via suppressed conductivity.
  - Units and data are documented in the accompanying spreadsheet/table.

- Data structure and contents:
  - Dataset size: 129 rows (128 samples + header) and 71 columns.
  - Columns encode: Code, Water_type (D/A/N/B), Dust (+/−), Replicate (1–4), Time point (days), and concentrations for numerous elements and ions (e.g., Ca, Mg, Na, K, Cl, NO3, SO4, etc.) with respective units and measurement method (ICP-MS or IC).
  - Typical measurement units include mg/L and µg/L; some elements are reported as Total P, Total S, etc., and while most are from ICP-MS, some are from Ion Chromatography.
  - The dataset notes where detection limits apply and indicates values below detection limit as <n.

- Quality control and provenance:
  - Detection limits are indicated in the dataset.
  - QC standards were analysed at the start and end of each run and after no more than every 20 samples.
  - Laboratories conducting analyses are ISO/IEC 17025 accredited.
  - Responsible researchers: Suzanne McGowan and Amanda Burson (experimentation); Michael Watts (analyses).

- Use and reuse notes:
  - Suitable for analyzing how dust presence and water type affect leaching of a broad suite of elements over time.
  - Enables cross-factor comparisons (dust vs. no-dust across D/A/N/B water types) and time-series assessment across sampling points.
  - Can support dashboards or reports that enable end-users to explore element-specific leaching patterns and water chemistry changes.