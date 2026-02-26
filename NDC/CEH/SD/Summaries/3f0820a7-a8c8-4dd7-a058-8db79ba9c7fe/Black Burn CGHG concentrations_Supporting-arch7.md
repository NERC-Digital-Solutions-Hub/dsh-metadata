# Collection Methods and Analytical Methods for Dissolved Carbon and Gases in Black Burn Stream (2007-2011)

## Overview
- Describes how POC, DOC, DIC, CO2, CH4, and N2O were collected and analyzed from stream water at the Black Burn to support data visualizations and analyses in GIS.
- Timeframe: sampling approximately weekly from January 2007 to December 2011 (measurements ongoing at the time of writing).
- Aims to provide robust, comparable concentration data for map-based interpretation of carbon and greenhouse gas dynamics in a freshwater system.

## Sampling Location and Timeline
- Location: Black Burn stream (approx. 55°47'41" N, 3°14'52" W).
- Frequency: approximately weekly sampling.
- Samples collected on each occasion for POC, DOC, DIC; headspace gas samples collected to estimate dissolved CO2, CH4, and N2O.

## Collection Methods
- Water sample volumes:
  - 300 mL glass bottles for POC, DOC, DIC analyses.
  - 40 mL water samples equilibrated with 20 mL ambient air for headspace gas analysis.
- Headspace technique details:
  - Vigorous shaking with ambient air at stream temperature for 1 minute.
  - Two replicate headspace samples collected per occasion, plus a separate ambient air sample.
- Sample handling and storage:
  - Filtration of stream water through pre-ashed GF/F filters (0.7 µm) within 24 hours.
  - POC determined by loss-on-ignition (Ball 1964 method).
  - Filtrate stored in the dark at 5°C and analyzed within 2 weeks.

## Analytical Methods
- DOC and DIC analysis:
  - Instruments: Rosemount-Dohrmann DC-80 total organic carbon analyser (2007) or PPM LABTOC Analyser (2008 onward).
  - Detection range: 0.1–4000 mg C L⁻¹.
- POC analysis:
  - Method: loss-on-ignition following Ball (1964).
- Headspace gas analysis:
  - Instrument: HP5890 Series II gas chromatograph with electron capture detector (ECD) for N2O and flame ionization detector (FID) with attached methaniser for CH4/CO2.
  - Analysis performed within two weeks of collection.
- Notes on calculations:
  - Concentrations of dissolved CO2, CH4, and N2O derived from the headspace concentrations using Henry’s Law, taking the mean of replicate headspace measurements, ambient air concentration, stream water temperature, and air pressure into account.

## Dissolved Gas Calculations
- Inputs for calculation:
  - Mean replicate headspace concentrations.
  - Ambient air concentrations.
  - Stream water temperature at sampling time.
  - Atmospheric pressure.
- Method references:
  - Based on established headspace methodologies (e.g., Billett et al., 2004; Dinsmore et al., 2010; Kling et al., 1991; Hope et al., 1995).

## Data Variables and Units
- POC: mg C L⁻¹
- DOC: mg C L⁻¹
- DIC: mg C L⁻¹
- CO2: mg C L⁻¹
- CH4: µg C L⁻¹
- N2O: µg N L⁻¹

## Data Quality, Provenance, and Reproducibility
- Replicates: two replicate headspace samples per occasion plus ambient air samples to ensure reliability.
- Temperature and pressure conditions recorded to enable accurate Henry’s Law calculations.
- Data collection and analysis follow standard methods, with cross-referencing to established literature for headspace techniques.
- Analyses conducted within recommended time windows to maintain sample integrity and comparability over time.

## GIS and Data Integration Implications
- Time-stamped, location-based concentration data enable creation of spatially and temporally explicit maps of dissolved carbon species and trace greenhouse gases.
- Standardized units and detailedMethod sections facilitate integration with other datasets and reproducibility in GIS workflows.
- The use of replicated measurements and documented calculation methods supports quality assurance in map visualizations and derived indicators of carbon fluxes in stream ecosystems.