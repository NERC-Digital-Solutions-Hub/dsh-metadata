Vegetation and soil data from a survey of British calcareous grasslands (1990 and 2007) Survey of British Calcareous Grasslands, 1990 & 2007  - Dataset Summary

## Overview
- National survey of calcareous grasslands in Britain conducted in 1990–1993 and a resurvey in 2006–2009.
- Primary aim: collect standardized vegetation and soil data to analyze species patterns, community relationships, and responses to environmental factors such as climate and nitrogen deposition.
- Sites were nature reserves with management aimed at maintaining diversity; plots were chosen to cover geographic, climatic, and deposition gradients.

## Data Coverage
- Geographic: Britain (Great Britain).
- Time periods: 1990 (1990–1993) and 2007 (2006–2009).
- Plots: 128 plots surveyed in 1990; 48 plots surveyed in 2007 (data for seven plots missing from 1990; total usable 121 plots from 1990 data).

## Data Categories
- Vegetation Data
  - Vascular plants, bryophytes, and macrolichens recorded.
  - Frequency-based presence/absence in 36 sub-quadrat samples per plot (0.5 x 0.5 m each).
  - Vegetation grouped into grasses, other herbs, and lower plants; occasional vouchers taken for verification.
- Soil Data
  - Top 10 cm soil pH measured in the field (1990) or via laboratory analyses (2007 onward).
  - Soil chemistry: plant-available phosphorus (Olsen-P), nitrate and ammonium, base cations (Ca, Na, Mg, K), aluminum, organic matter (loss on ignition), soil depth, type, and related descriptors.
  - Sampling aligned with copper-marker grid locations to minimize disturbance.

## Survey Design & Methods
- Plot layout
  - Each plot ~144 m² (typically 12 x 12 m; sometimes 6 x 24 m).
  - Permanent marking using seven copper wire marker loops buried 5–15 cm deep for relocatability (5 cm relocation accuracy in practice).
  - Plot subdivided into four 6 x 6 m blocks; each block into nine 2 x 2 m units; each unit sampled by a 0.5 x 0.5 m quadrat.
  - Grid orientation and marker system designed for rapid relocation and repeatability.
- Vegetation sampling
  - In each quadrat, record height and percent cover; note features (ant-hills, bare rock, etc.).
  - All vascular plants, bryophytes, and macro lichens recorded as present in quadrats; dominant species have additional cover notes.
  - Recording uses a standardized form/checklist to improve data quality and consistency.
  - Time per plot ranges from 3 to 12 hours; grid setup ~45 minutes.
- Soil sampling
  - 1990: pH determined in the field from top 10 cm soil.
  - 2007: soil samples collected as five-subsample composite (top 10 cm) and stored for analysis; pH, plant-available P (Olsen), NO3–/NH4+ (from NaCl extracts), base cations, Al, organic content measured in the lab; moisture-corrected results reported.
- Data handling
  - Data processed and analyzed with VESPAN II software; frequency data used to derive constancy classes and compare with National Vegetation Classification (NVC) profiles.
  - MATCH used in preliminary tests to compare with NVC; data suitable for multivariate analyses despite limited cover estimates.
- Limitations
  - Lack of comprehensive cover estimates; potential loss of copper markers due to treasure-hunting; technique unique and not directly comparable with other datasets.
  - Constancy for infrequent species may be underrepresented relative to full NVC sampling; data best used with frequency-based analyses and for cross-site comparisons within this dataset.
  - Some data gaps: 1990 original reports for seven plots could not be recovered.

## Data Files
- CG_SITES.csv
  - Site-level and plot-level information for calcareous grassland surveys (1990 and 2007).
  - Key fields: PLOT_ID, PLOT, SITE, STATUS, YEAR, OSGR, EASTING, NORTHING, NVC, PH, ALT, ASPECT, SLOPE, SCREE, PH_LE_6, COASTAL, NOTES, ORG, AMMONIUM, NITRATE, AVE_SOIL_DEPTH, SOIL_TYPE.
- CG_VEG.csv
  - Vegetation species records by plot and year.
  - Key fields: PLOT_ID, PLOT, YEAR, SPECIES_REC, BRC_NUM, BRC_NAME, COUNT, GROWTH.
- CG_SITES and CG_VEG are the primary data tables; 2007 dataset excludes bryophytes (present in 1990 dataset only).

## Provenance and Access
- Originators (1990): T.C.G. Rich, E.A. Cooper, J.S. Rodwell, A.J.C. Malloch (Lancaster University); DoE contract.
- Resurvey (2007): L.J.L. Van Den Berg, P. Vergeer, T.C.G. Rich, S.M. Smart, D. Guest, M.R. Ashmore (multiple institutions); NERC grant.
- Publications and data references
  - Rich et al. (1993): Effects of climate change and air pollution on British calcicolous ecosystems.
  - Rodwell (ed.) (1993): Final report to UK Department of the Environment.
  - Van Den Berg et al. (2011): Direct and indirect effects of nitrogen deposition on species composition change in calcareous grasslands.
  - Rich et al. (2015): Survey of British calcareous grasslands, 1990 and 2007. NERC Environmental Information Data Centre. DOI: 10.5285/38a73c7b-3e3c-4517-a33f-bd28b292b9e1.
- Data handling and tools
  - VESPAN II (Malloch 1988) used for data handling; MATCH (Malloch 1990) used for cross-referencing with NVC.
- Access
  - Data centralized in the NERC Environmental Information Data Centre; datasets include site, vegetation, and soil measurements for 1990 and 2007 calcareous grasslands.