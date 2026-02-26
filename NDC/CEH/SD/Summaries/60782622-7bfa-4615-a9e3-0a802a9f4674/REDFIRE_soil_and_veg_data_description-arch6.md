# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Assesses radionuclide activity concentrations and calculated dose rates in the Red Forest (Chernobyl Exclusion Zone) after a severe fire in 2016.
- RED FIRE project conducted in September 2017 across 60 plot sites (burnt and unburnt) plus 9 plots near Buriakivka ( ~8 km from the Red Forest).
- Data include plot details, radionuclide activity concentrations in grassy vegetation and soil, and dose-rate estimates for grassy vegetation, deciduous trees, and bacteria.
- Dose estimates use external exposure from soil activity and transfer parameters to estimate plant and bacteria doses; some sites with no grassy vegetation have no grassy-vegetation dose estimates.
- Related data and methods are published in Beresford et al. 2020 and Holiaka et al. 2020, with methodology supported by ERICA Tool and R&D128.

## Sampling design and dataset structure
- Plot setup: 60 Red Forest plots (burnt and unburnt) and 9 plots near Buriakivka; a 1x1 m2 square for soil/vegetation studies and a second adjacent 1x1 m2 area for undisturbed vegetation harvest.
- GPS location recorded (accuracy ~3 m).
- Sampling occurred in September 2017, with a one-year study window for measurements.
- Burn history and burn score recorded per plot (1 = no burn, 2 = some burn, 3 = all plot burnt).
- Ambient dose rate measured on soil surface at two time points: Sept 2016 and March 2017.

## Sampling, preparation, and analytical methods
- Vegetation:
  - Samples harvested and sorted into grassy vegetation vs other; measured fresh mass (FM) and dry mass (DM) after air-drying.
  - Grassy vegetation homogenised for radionuclide analyses.
- Soil:
  - Five cores per plot (2.5 cm diameter, 10 cm deep: corners and center) pooled and homogenised.
  - Subsamples: pH (fresh soil), moisture (oven-dried), and remaining soil used for radionuclide analysis after drying (~80°C).
- Radionuclide analyses:
  - Cs-137 in grassy vegetation and soil measured with high-purity germanium gamma detector; Cs-137 calibration with a standard source; detection limit ~0.18 Bq per sample; typical uncertainty ~10–15%.
  - Sr-90 in grassy vegetation and soil measured with a beta-spectrometer; no radiochemical pre-treatment; daily calibrations; uncertainties ~20%.
  - Am-241 and Pu isotopes in soil and vegetation analyzed after chemical separation (HF digestion, multiple acids, anion exchange/TRU resin) and alpha spectrometry; yield tracers (242Pu, 243Am) added; typical counting uncertainties <20%.
- Transfer parameters:
  - Am-241 and Pu isotopes in grassy vegetation and Agrostis gigantea transfer to soil using CR wo-soil values from Beresford et al. 2020.
  - Sr-90 and Cs-137 in deciduous trees use CR wo-soil values for CEZ sites from Holiaka et al. 2020; Am-241 and Pu-238/239/240 in Pinus sylvestris wood use Red Forest site parameters from Beresford et al. 2020.
- Dose estimation:
  - External dose to grassy vegetation and trees estimated with ERICA Tool v1.3 (Brown et al. 2008, 2016) using measured soil activity concentrations (FM) for external exposure.
  - Internal and external dose rates per isotope for grasses and trees calculated via ERICA; a revised R&D128 model used to estimate dose to bacteria.
  - Ambient soil-dose rate recorded separately and used for context.

## Dataset contents (data fields)
- Plot metadata: plot number, location, pine forest history, burn score.
- Ambient dose rates: measured in September 2016 and March 2017.
- Vegetation masses: FM and DM for grassy vegetation and for “other” vegetation.
- Grass activity concentrations: Sr-90 and Cs-137 (DM and FM) with uncertainties.
- Deciduous tree wood activity concentrations: Sr-90 and Cs-137 (FM) derived using soil transfer parameters and measured soil concentrations.
- Grassy vegetation Am-241 and Pu-238/239/240 (FM) concentrations estimated using transfer parameters and soil data.
- Soil activity concentrations (DM) for Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240.
- Soil DM percentages: %DM measured in March and September 2017.
- Soil properties: pH, loss on ignition (LOI).
- Dose metrics (grassy vegetation, deciduous wood, bacteria):
  - Internal, external, and total weighted absorbed dose rates by isotope (Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240).
  - Totals per isotope and overall totals across all isotopes for each biological category (grassy vegetation, deciduous wood, bacteria).

## Dose estimation and data interpretation
- External doses computed from measured external soil concentrations; internal doses derived from transfer parameters and isotope-specific activity concentrations in plant/biomass.
- Multi-isotope approach enables comparison of radiological burden across vegetation types and bacteria.
- The dataset supports ecological exposure assessments and radiological risk analyses in contaminated forest ecosystems, particularly under post-fire recovery conditions.

## Data provenance, references, and use
- Core methods and transfer parameter data draw from:
  - Beresford et al. 2020 (transfer to wildlife; deciduous trees and grassy vegetation for certain isotopes)
  - Holiaka et al. 2020 (Sr-90 and Cs-137 inventories in CEZ forest stands)
  - ERICA Tool updates (Brown et al. 2008, 2016)
  - R&D128 methodology (Copplestone et al. 2001)
- Acknowledgements: Dimitri Holiaka (transfer parameters), Claire Wells (data collating support); funded by NERC NE/P015212/1 (RED FIRE).
- Related project: RED FIRE (Radioactive Environment Damaged by fire: a Forest In Recovery); project page: ceh.ac.uk/redfire.