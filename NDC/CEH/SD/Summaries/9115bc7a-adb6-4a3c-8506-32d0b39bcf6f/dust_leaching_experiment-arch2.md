# Dust leaching

## Overview
- Dataset presents the elemental composition of filtered water samples from a controlled dust-leaching experiment conducted at the KISS research station, Kangerlussuaq, West Greenland.
- Water source: lake SS903 (coordinates provided); experiment ran from April 2017 for 63 days.
- Purpose: determine which elements leach from dust into different water types.
- Analytical workflow: samples filtered (GF/F) and analyzed by ICP-MS and ion chromatography at the British Geological Survey laboratories.

## Experimental design and sampling regime
- Fully factorial design with two factors:
  - Dust: present (+) or absent (-)
  - Water type: D (deionised autoclaved), A (abiotic lake water filtered then autoclaved), N (nanobiotic lake water filtered), B (biotic lake water filtered to remove zooplankton)
- Replicates: four per treatment combination
- Incubation conditions: 10°C; 16:8 light:dark; PAR ~40 μmol photons m−2 s−1
- Sampling time points: 0 days (initial), 1 day, 7 days, and 63 days (labeled as 40 in the dataset)
- Post-incubation processing: entire sample filtered and stored refrigerated; filtered water analyzed

## Analytical methods
- Inductively coupled plasma mass spectrometry (ICP-MS; Agilent 8900 series) with collision/reaction cell optimization:
  - Helium mode for most elements
  - Oxygen mode with MS/MS for P, S, As, Se
- Ion chromatography (Dionex ICS5000) for anions (e.g., Cl−, NO3−, SO4^2−, Br−, NO2−, HPO4^2−, F−)
- Units are reported in the accompanying spreadsheet; typical reporting units include mg/L and μg/L depending on the element

## Nature and units of recorded values
- The dataset contains 71 columns of measured variables (elements/ions) with corresponding metadata fields
- Measured elements include Ca, Mg, Na, K, Cl, NO3, NO2, SO4, F, total P, total S, Si, SiO2, and a broad suite of trace metals and metalloids (e.g., Fe, Mn, Zn, Cu, Pb, U, etc.)
- Data are structured with clear method qualifiers (ICP-MS or Ion-Chromatography) per element

## Quality control
- Detection limits provided in the spreadsheet; values below detection limit annotated as <n
- QC checks: standards analyzed at the start, end, and after no more than every 20 samples
- Laboratories operate under ISO/IEC 17025 accreditation

## Data structure details
- Size: 129 rows total (128 samples + 1 header row) and 71 columns
- Key schema (illustrative):
  - Code, Water_type (D, A, N, B), Dust (+ or -), Replicate (1–4), Time point (0, 1, 7, 40)
  - Element concentration columns (e.g., Ca_mg/L, Mg_mg/L, Na_mg/L, K_mg/L, Cl-_mg/L, NO3-_mg/L, SO4-_mg/L, NO2-_mg/L, HPO4-_mg/L, F-_mg/L, Total P_mg/L, Total S_mg/L, Si_mg/L, SiO2_mg/L, etc.)
  - Each row corresponds to a single sample with the measured concentrations and the analytical method indicated
- Timepoint label 40 corresponds to the 63-day endpoint

## How this dataset supports environmental monitoring and analysis
- Provides standardized, quality-controlled data on how dust-derived constituents leach into different water types under controlled conditions
- Facilitates assessment of potential metal and metalloid inputs to freshwater systems from dust events
- Enables temporal analysis across initial, early, mid, and end points to understand leaching dynamics
- Output formats (reports, maps, charts) align with typical monitoring workflows and are suitable for integration with broader environmental health indicators

## Practical considerations for analysts
- Use the four-factor factorial design (dust, water type, replicate, timepoint) to compare leaching behaviors across conditions
- Leverage QA/QA procedures (detection limits, ISO 17025 QA) to assess data confidence and comparability
- Consider linking these data with field dust deposition datasets or water chemistry datasets to evaluate real-world relevance
- To increase data value, integrate this dataset with additional environmental variables (e.g., meteorology, dust source characteristics) and share the underlying data via appropriate data portals as per monitoring best practices

## Key takeaways
- The study systematically tests how dust interacts with four distinct water types over time, measuring a comprehensive suite of elements and anions
- The data are rigorously quality-controlled and well-documented, with explicit replication and timepoint structure
- The resulting dataset is suitable for informing environmental health assessments, dust-leaching models, and policy-relevant monitoring of potential contaminant inputs to aquatic systems