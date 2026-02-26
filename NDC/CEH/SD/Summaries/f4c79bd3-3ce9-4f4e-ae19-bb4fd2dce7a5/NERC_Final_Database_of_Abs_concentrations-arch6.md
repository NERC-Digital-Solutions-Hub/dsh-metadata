# Brief description of the dataset

- A dataset of weekly concentrations of fluoroquinolones and the resistance gene qnrS in the South West UK, including a wide range of analytes listed (various fluoroquinolones and related compounds). Concentrations reported in ng/L; data format accommodates nd (not detected) and MQL (below method quantification limit) flags.
- Outputs are intended to support understanding of antibiotic presence and resistance gene dissemination in the aquatic environment.

## Study area and sampling points

- Five major wastewater treatment plants (WWTPs) contributing to a single river catchment, covering ~2,000 km² with a population of ~1.5 million (over 75% of the catchment’s population).
- Sampling includes:
  - Wastewater influent and effluent (7 consecutive days, Wed–Tue, June–October 2015).
  - River water upstream and downstream of the effluent discharge point at varying accessible distances (except Site E, where the WWTP discharges directly to the estuary, so no river sample).
- Influent samples represent 24 h composites; river water samples are grab samples.

## Sample collection and handling

- Influent wastewater: volume-proportional 24 h composites; subsamples ~80 mL collected roughly every 15 minutes; samples cooled to 4°C during collection; pooled after 24 h.
- Effluent wastewater: time-proportional samples due to limited variation within the matrix over short intervals.
- River water: 8 L grab samples collected upstream and downstream of the discharge point.
- All samples transported to the laboratory on ice; site-specific details such as distance from discharge points vary by accessibility.

## Sample preparation and analytical method

- Filtration and internal standardization:
  - Wastewater filtered through GF/F (0.7 µm); 50 mL filtered sample spiked with isotopically labeled internal standards (1 mg/L).
- Extraction and cleanup:
  - Solid-phase extraction (SPE) using Oasis HLB cartridges (60 mg); conditioning, washing, and elution steps detailed.
  - Eluates evaporated to dryness under nitrogen, reconstituted in 0.5 mL of 10 mM ammonium formate/methanol (1:99 v/v) with 0.05% formic acid; filtered prior to analysis.
- Instrumentation and analysis:
  - LC-MS/MS: Waters ACQUITY UPLC system with a chiral CHIRALCEL OZ-RH column (5 µm, 15 cm × 2.1 mm) at 30°C; isocratic mobile phase: 10 mM ammonium formate/methanol 1:99 with 0.05% formic acid; flow 0.1 mL/min.
  - Detection: triple quadrupole MS (Xevo TQD) in positive mode; optimized source conditions; nitrogen and argon used as gases.
  - Data processing with TargetLynx software.
  - Analyses performed in duplicate.
- Method validation:
  - Fully validated as described in Castrignano et al. 2018.

## Data format and content

- Concentrations of quinolones in influent, effluent, and receiving environment (river) during the monitoring week presented in ng/L.
- Data include the listed analytes and the corresponding sample types (influent, effluent, river upstream, river downstream); Site E lacks river water data.

## Validation, references, and notes

- Validation: method validated as described in Castrignano et al. 2018.
- Key references:
  - Castrignano et al. 2018. Enantioselective fractionation of fluoroquinolones in the aqueous environment using chiral liquid chromatography coupled with tandem mass spectrometry.
  - Castrignano et al. 2020. (Fluoro)quinolones and quinolone resistance genes in the aquatic environment: A river catchment perspective.
  - Petrie et al. 2016. Multi-residue analysis of 90 emerging contaminants in environmental matrices.
- Additional context: the dataset focuses on antibiotic concentrations and resistance gene monitoring in a real catchment scenario, enabling assessment of removal efficiencies and environmental exposure.