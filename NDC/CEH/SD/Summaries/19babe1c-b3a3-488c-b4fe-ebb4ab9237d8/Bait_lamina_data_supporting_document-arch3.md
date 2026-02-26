# Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016)

- This document describes the column headings, materials, and methods for the data files underlying the study of soil biological activity in the Chernobyl Exclusion Zone (CEZ), tying to the paper: Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016). Beresford et al., 2021.

## Data files and content

- Radionuclide_concentration_data_2005.csv
  - Contains Cs-137, Sr-90, Cs-134, K-40, Co-60 soil activity concentrations (dry mass) with site details, coordinates, sampling date, etc.
- Bait_lamina_2005.csv
  - Records radionuclide data relevant to bait lamina and associated soil context for 2005 sampling.
- Reader_1_bait_lamina_2016.csv and Reader_2_bait_lamina_2016.csv
  - Contain blind readings of bait lamina strips by two readers at 18 CEZ sites (three 1x1 m plots per site; 16 strips per plot) with hole-level piercing data and plot-level metadata (pH, moisture, etc.).
- Main_data_2016.csv
  - Core 2016 dataset including location, coordinates, ambient dose rate, radionuclide concentrations (Cs, Sr, Am, Pu), dose-rate estimates by organism, and plot-level summaries (e.g., total bites, percent utilization, bite holes by segments, soil properties, simple habitat, field notes).
- Concentration_ratios.csv
  - Contains concentration ratios for annelid, detritivorous arthropod, and related nuclides used in dose calculations.
- The data relate to the study “Dataset underlying the assessment of soil biological activity in the Chernobyl Exclusion Zone (September 2005 and spring 2016)” (Beresford et al., 2021).

## Study design and sites

- 2005
  - Four CEZ sites: Red Forest (High and Dead), Izumrudnoe (Low), Novoshepel Forestry (Medium).
  - Sampling date: 27 September 2005.
  - Bait lamina deployed; pH and soil moisture measured.
- 2016
  - Eighteen CEZ sites within the CEZ; includes Red Forest (eight sites) and adjacent woodland sites categorized as Coniferous, Deciduous, and Red Forest.
  - Ambient soil dose rates measured in the Red Forest using a dose-rate meter.
  - Three 1x1 m plots per site (two plots at one deciduous site); 16 bait lamina sticks per plot deployed in a 4x4 grid; retrieved after ~18 days.
  - Soil temperature measured at insertion and removal; five 10 cm-deep soil cores collected per plot for pH, moisture, and dry mass determination.

## Bait lamina methodology

- Bait lamina strips
  - Dimensions: ~155x6x1 mm PVC with sixteen 5 mm aperture holes starting 10 mm from the bottom; top 70 mm of the strip has no apertures.
  - Bait composition: 70% cellulose, 25% finely ground wheat bran, 5% active charcoal.
  - Reading method: qualitative feeding scored as pierced (1) or unpierced (0); holes assessed for evidence of bait removal and distribution along the strip.
  - Readers: two independent readers per plot; results averaged; strips read blind to deployment site.
- Data handling
  - For analyses, results per plot are summed across all 16 sticks.

## Soil analyses and radionuclide measurements

- Soil sampling
  - Five cores per plot (corners and center), 5x10 cm cores; bulked and homogenised; subsamples for pH and moisture; remaining material dried to determine dry mass.
- Measurements and methods
  - pH: standard soil method.
  - Moisture: oven-dried mass fraction.
  - Radionuclides (2005): Cs-137, Sr-90, Cs-134, K-40, Co-60 measured by gamma spectrometry and beta spectrometry with specified detection limits and uncertainties.
  - Radionuclides (2016): Cs-137, Sr-90, Am-241, Pu isotopes (238, 239, 240) measured by high-purity germanium detectors; detection limits and measurement uncertainties provided.
- Uncertainties and detection limits
  - Typical uncertainties around 10-15% for major isotopes (e.g., Cs, Am) depending on sample type; minimum detectable activities indicated per method.

## Dose rate estimation and modelling

- Organisms and models
  - Annelid and detritivorous arthropod dose rates estimated with the ERICA Tool (Brown et al. 2008, 2016).
  - Soil bacteria dose rates estimated with the R&D128 model (tied to the limitation that ERICA cannot model bacteria due to size considerations).
- Inputs and assumptions
  - Concentration ratios used: 2014 Lumbricidae-derived ratios for annelids; ERICA-default ratios for detritivorous arthropods.
  - Pu activity concentrations in soil used with 238 Pu/239 Pu/240 Pu isotopic ratios from Red Forest soil samples (2014 data).
  - Assumed 100% occupancy within the soil column for all three organisms.
  - Measured soil dry matter percentages used to scale external dose rates accordingly (e.g., 10% DM yields 10% of the dose compared to 100% DM).

## Data structure and metadata

- Column explanations
  - Tables 1–5 provide detailed explanations and units for all columns across the files, including sample identifiers, locations, sampling dates, radiological measurements, bait lamina results, soil properties, and dose metrics.
  - Some fields include minimum detectable activity markers (<) and summary fields (e.g., Average_total_bites, Percent_utilisation, Bite_holes_1_4, 1_8, 9_16, etc.).
  - Location, coordinates, plot identifiers, and sampling metadata are consistently defined to support cross-file linkage.

## Data quality, governance, and use

- Data quality and transparency
  - Metadata and column definitions are explicitly documented to support reproducibility and data quality assessment.
  - Two-reader blind scoring for bait lamina readings enhances reliability; results averaged across readers.
- Data sharing and governance
  - The dataset aligns with ISO 18311:2016 (bait-lamina test) and established radionuclide measurement protocols; methodology and references are cited to support governance and methodological transparency.
  - Availability and reuse are supported by linking to the broader Beresford et al. dataset and related data centers (e.g., cited ERICA/R&D128 tools and supporting literature).
- Relevance to monitoring frameworks
  - Provides concrete environmental health indicators (feeding activity via bait lamina, soil chemical and radiological status, ambient dose rates, and modeled dose to key soil biota) that can inform policy decisions on environmental monitoring, risk assessment, and ecological protection in radiologically contaminated landscapes.
  - Demonstrates integration of field measurements, laboratory analyses, and modeling approaches into a cohesive dataset suitable for evaluating policy-relevant environmental health outcomes.

## References and related resources

- ISO 18311:2016. Soil quality - Method for testing effects of soil contaminants on the feeding activity of soil dwelling organisms - Bait-lamina test.
- ERICA Tool (Brown et al. 2008, 2016) for estimating wildlife radiation dose rates.
- R&D128 (Copplestone et al. 2001) for ecological dose assessment methods.
- Beresford et al. (2012–2021) and related papers documenting CEZ radiological data, wildlife exposure, and field effects studies.
- Allen (1974) chemical analysis reference for soil analyses.
- Gaschak et al. and Bondarkov et al. methodological references for radionuclide measurements.