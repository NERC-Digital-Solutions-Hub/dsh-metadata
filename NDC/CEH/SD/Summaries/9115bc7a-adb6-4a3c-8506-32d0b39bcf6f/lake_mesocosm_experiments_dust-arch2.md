# Overview of the data

- A mesocosm experiment conducted in three lakes in the Kangerlussuaq region of West Greenland to assess how added dust affects water chemistry and phototrophs in water, on sediments, and on an artificial substrate.
- Researchers: Suzanne McGowan and Amanda Burson.
- Experiment duration: 14 days, initiated July 2018.

## Experimental design and sampling regime

- Location: Three lakes (Lake SS17b, SS1590, SS906) with specified latitude/longitude coordinates.
- Setup: 6 enclosures per lake (60 cm diameter, ~1 m depth) embedded in lake sediments; each enclosure contained a terracotta pot at the bottom as an artificial substrate for phytobenthos.
- Treatments: Three mesocosms per lake received dust at 0.196 g/L (roughly 25–35 g per mesocosm, adjusted for water depth/volume); three served as controls.
- Arrangement: Dust-treated and control enclosures alternated in a 3×2 grid within a wooden frame.
- Measurements: In situ water parameters (conductivity, temperature, dissolved oxygen) measured in the upper 20 cm with a YSI multiprobe.
- Sampling schedule:
  - Start and end of experiment for water and phytoplankton from mesocosms.
  - Surface sediments sampled at start and end.
  - Terracotta pots sampled at the end for biofilms.
  - Sampling dates varied by lake but generally included an initial day 0 sampling and a final day sampling after 14 days.

## Collection, generation, and transformation methods

- Water sampling: Integrated-depth samples collected with a plastic tube; filtered in the field through GF/F filters; chlorophyll a analyzed spectrophotometrically.
- Post-sampling processing: Terracotta pots removed; biofilms scraped and rinsed; suspended material frozen until analysis. Surface sediments stored frozen prior to analysis.
- Chlorophyll and pigments: Chlorophyll a measured; pigments extracted and analyzed by HPLC with detailed solvent systems and calibration against standards.
- Documentation of samples: Total sample volume recorded; aliquots taken volumetrically for analysis.

## Analytical methods and units of measured values

- Water chemistry:
  - Soluble reactive phosphorus (SRP), ammonium (NH4-N), nitrate (NO3-N), silicate, total phosphorus (TP), total nitrogen (TN).
  - Units include µg/L for many nutrients and mg/L for silicate; major ions analyzed by ion chromatography.
  - Additional in situ water parameters recorded: temperature (°C), dissolved oxygen (% and mg/L), conductivity (µS/cm), pH.
  - Total alkalinity reported as meq/L in association with other measures.
- Chlorophyll analysis:
  - Water, phytobenthos, and sediments: chlorophyll a (Chl a) concentrations measured; units: µg/L for water, µg/cm² for phytobenthos, µg/g for sediments.
- Pigments and pigments by group (HPLC):
  - Pigment concentrations included chlorophylls and carotenoids (e.g., Chl b, Chl a, Chl c2, fucoxanthin, diadinoxanthin, diatoxanthin, lutein, zeaxanthin, alloxanthin, pheophytin variants, etc.).
  - Units for sediment measurements: nanomoles per gram or per square centimeter; for pot scrapes: nanomoles per square centimeter.
- Additional pigment data:
  - B-carotene and various pigment concentrations on artificial substrate (pots) and in surface sediments, with corresponding units and surface densities (mg/cm² for certain measurements).

## Quality control and data validation

- Colorimetric water analyses:
  - New calibration curves run with each batch; data discarded if r² < 0.998.
- Instrument calibration:
  - Ion chromatography calibrated with 10-point curves.
  - YSI probes calibrated daily for pH and DO (three-point pH, single-point DO in air) and weekly for conductivity.
- HPLC pigment analysis:
  - Pigment standards used for eight-point calibration annually.
  - Stability checks using plant extract added at start and end of each run to verify retention times.
  - Manual verification of pigment identifications and baseline integrations by a trained expert.

## Data structure and organization

- Dataset contains 37 rows and 46 data columns.
- Column organization:
  - Columns 1–5: experimental condition descriptors (lake code, dust treatment, replicate, time point, sample date).
  - Columns 6–17: water measurements at start and end (chlorophyll a, nutrients, in situ parameters, etc.).
  - Columns 18–31: surface sediment analyses (pigments and related metrics).
  - Columns 32–46: terracotta pot scrape analyses (pigments and related metrics).
- Example descriptors include lake/site identifiers, dust treatment status, replicate number, sampling time point, and date.

## Data scope and intended use

- Purpose: Provide a standardized, high-quality dataset to monitor environmental health impacts of dust on lake systems, enabling cross-time and cross-site comparisons and policy-relevant analyses.
- Emphasis for analysts monitoring the environment:
  - Standardised data collection and quality assurance enable clear evaluation of environmental health and policy performance over time.
  - Datasets are designed to be inter-operable and to support integration with other related environmental data.

## References

- APHA (2005). Standard methods for the examination of water and wastewater.
- Chen et al. (2001). Historical trends of hypoxia on the Louisiana shelf: pigments as biomarkers.
- Parsons TR, Strickland JD (1963). Discussion of spectrophotometric determination of marine-plant pigments.