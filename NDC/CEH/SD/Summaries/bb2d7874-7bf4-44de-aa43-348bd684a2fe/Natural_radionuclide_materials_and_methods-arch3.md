# Materials and methods for soil, water and sediment data extracted from: Background exposure rates of terrestrial wildlife in England and Wales

- This document describes the data and methods used to assess naturally occurring radionuclides in terrestrial wildlife and related media in England and Wales, with the aim of informing radiation dose assessments to non-human species.

## 2.1. Proposed ICRP reference animals and plants (RAPs)

- ICRP RAPs used as reference points for assessing radiation effects in non-human species include: Reference Deer; Reference Rat; Reference Duck; Reference Frog; Reference Bee; Reference Earthworm; Reference Pine Tree; Reference Wild Grass.
- The objective is to categorise available data on naturally occurring radionuclides in England and Wales according to these RAPs.

## 2.2. Review of available data

- Data sources reviewed to populate RAPs:
  - Grey literature, refereed journal papers, and in-house databases.
  - RIFE (Radioactivity in Food and the Environment) annual reports, providing activity concentrations for some naturally occurring radionuclides in relevant biota (mostly near sites discharging radionuclides). Most data pertain to non-edible parts with the exception of grass.
  - CEH analyses of biota related to radiocaesium deposition (Chernobyl and Sellafield-related studies).
- Data attribution to RAPs:
  - Reference Duck: any wild bird.
  - Reference Frog: any amphibian.
  - Reference Bee: any flying insect.
  - Reference Earthworm: any earthworm.
  - Reference Pine Tree: any tree.
  - Reference Wild Grass: any wild grass or herb, or data labeled as grass.
  - Mammals: data for “any wild mammalian species” plus separate data for Deer and Rat.
- Acknowledgement of limited RAP-specific data; additional discussion on data availability for the defined RAPs.

## 2.3. Sampling and analyses

- Due to data paucity, a targeted sampling campaign was conducted for Duck, Bee, Earthworm, Pine Tree, and Frog.
- Use of existing CEH sample archives combined with new sampling.
- Collected samples included:
  - Mixed flying insects (predominantly moths) from eight Environmental Change Network sites.
  - Five lodgepole pine trunk samples.
  - Twenty grey heron liver samples from CEH archives.
  - Six earthworm samples.
  - Four rabbits.
  - One toad.
  - Five mallards.
- Wales: additional samples where available (e.g., some heron liver samples from Wales; extra rabbit, mallard, pine, and earthworm samples due to Welsh data gaps).

### 2.3.1. Sample preparation and analyses

- Pine trunks: washed and ashed at 450°C.
- Earthworms: gut evacuation, freeze-dried, and homogenised.
- Insects: dried and homogenised.
- Mallards: plucked, GI tract removed; liver analysed separately.
- Rabbits: skinned, external tissues cleaned; carcasses washed and ashed.
- Herons and mallard liver: freeze-dried and homogenised.
- All samples powdered prior to analysis to determine total U and Th.
- Sealing and secular equilibrium:
  - Samples sealed in 25 mL dishes or 150 mL containers for about 25 days to establish secular equilibrium.
  - Gamma spectrometry with hyperpure germanium detectors conducted; 2-day counting times; spectra analyzed with Genie-VMS.
  - Detector calibration using certified reference materials; density corrections applied; fresh weight (FW) basis used for activity concentrations where possible.
- For toads (small sample): analysed fresh for U and Th, then ashed.
- Chemical analyses for U and Th:
  - 0.5 g of sample digested with 10 mL HNO3 and two drops HF in a microwave; final digest in 10 mL of 10% HNO3.
  - ICP-MS used; detection limits typically 10^-2 mg kg^-1 FW for Th and 10^-3 mg kg^-1 FW for U.
  - Specific activities used to convert total U and Th to activity concentrations: 40K (31.6 Bq g^-1 K), 232Th (4.07 Bq mg^-1 Th), 238U (12.21 Bq mg^-1 U).
  - Assumptions:
    - 238U and 234U assumed to be in secular equilibrium.
    - Equilibrium for other parents/partners in decay chains not assumed due to varying environmental/biological behavior.

## 2.4. Derivation of soil activity concentrations

- For soils, the G-BASE (Geochemical Baseline Survey of the Environment) project provides long-running data on K, U, and Th in soils.
- Sampling design:
  - Typical density of one sample per 2 km² for soils (and up to 1.5–2 km² for stream sediments/waters), with five subsamples within ~20 m x 20 m areas.
- Normalisation and data integration:
  - Over time, analytical procedures and sampling methods changed; data were normalised to enable comparability (described in Beresford et al., 2007).
  - Normalisation between BGS and Wolfson Atlas data achieved via linear quantile transformation for overlapping areas.
  - For U and Th (in sediments) and K, U, Th in soils, extrapolation to complete coverage used bedrock/superficial geology information to assign values to grid squares.
- Spatial derivation:
  - For soils and sediments: geometric means calculated per 1 km grid square using the nearest five samples for each parent material; then aggregated to 25 km² grid squares (5 x 5 km) with area-weighted means.
  - For waters: geometric means derived where data exist; less extrapolation due to weaker sediment–geology relationships.
- Conversion to activity concentrations:
  - Total K, U, Th concentrations converted to activity concentrations using standard specific activities (K-40, 232Th, 238U) listed above.
  - Assumptions of equilibrium:
    - 232Th series treated as in equilibrium.
    - 238U series assumed secular equilibrium with 234U in biological samples; other series may not be in equilibrium due to differing environmental/biological behavior.

## Terrestrial biota references and data handling

- Terrestrial biota data are drawn from multiple sources (RIFE reports, CEH datasets, targeted sampling) and mapped to the defined RAP categories.
- Data are gathered, harmonised, and stored with attention to metadata, sampling date, location (easting/northing), and tissue sampled.
- An internal data dictionary and a structured spreadsheet were used to couple each observation with RAP, location, sampling details, and concentration data (e.g., Bq/kg FW) for whole-body or tissue-specific estimates.
- The methodology emphasises the need for data governance and metadata completeness to enable reproducible assessments and transparent communication of findings.

Implications for monitoring frameworks (relevant for Authors of Monitoring Frameworks)

- Data gaps: limited RAP-specific data, especially for certain terrestrial biota and for Wales; targeted sampling helps fill gaps but ongoing data collection is needed.
- Data sources and openness: reliance on grey literature and archival datasets; importance of data sharing and metadata to ensure data can be reused in policy evaluation and decision-making.
- Data harmonisation: normalization across different analytical methods and sampling schemes is essential to enable meaningful comparisons and trend assessments.
- Communication and governance: transparent data provenance, quality assurance, and governance processes are critical to support public dissemination and policy use.
- Methodological transparency: clear documentation of sampling, preparation, analysis, and interpretation steps enables replication and comparability across monitoring frameworks.