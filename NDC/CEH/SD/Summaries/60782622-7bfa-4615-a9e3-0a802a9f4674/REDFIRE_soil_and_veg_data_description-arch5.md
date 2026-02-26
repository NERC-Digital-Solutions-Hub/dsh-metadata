# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Investigates radionuclide activity and derived dose rates in the Red Forest after a 2016 fire.
- Establishes 60 study plots in burnt/unburnt areas and 9 plots near Buriakivka to quantify radionuclide transfer to grassy vegetation, soil, and deciduous tree wood, and to estimate absorbed doses.
- Uses these data to understand recovery of ecosystems exposed to radiation and a secondary fire stressor.

## Study design and sampling
- September 2017: 60 plots in the Red Forest (burnt and unburnt) and 9 plots near Buriakivka (≈8 km away).
- Each plot: 1x1 m2 area for soil-related measurements; adjacent 1x1 m2 area for undisturbed vegetation sampling (harvested in September 2017).
- Plot locations recorded with GPS (≈3 m accuracy); many Red Forest plots previously used by the TREE project.
- Burn history captured as a burn score (1 = none; 2 = some areas burnt; 3 = all plot burnt).

## Data collected (Dataset contents)
- Plot metadata: plot number, location, pine forest past history, burn score.
- Ambient dose rate: measurements at the soil surface in September 2016 and March 2017.
- Vegetation data: fresh mass (FM) and dry mass (DM) for grassy and other vegetation; radionuclide activity concentrations in grassy vegetation (DM/FM) for Sr-90 and Cs-137 with uncertainties.
- Soil data: five soil cores per plot (bulked and homogenised) for pH, moisture, and radionuclide activity concentrations (Sr-90, Cs-137, Am-241, Pu isotopes, etc.).
- Deciduous tree wood data: estimated activity concentrations for Sr-90 and Cs-137 using transfer parameters from CEZ sites; Am-241 and Pu isotopes estimated in grassy vegetation and wood using site-specific transfer parameters.
- Internal and external weighted absorbed dose rates: by isotope and for grassy vegetation, deciduous tree wood, and bacteria; total dose rates by plot and by all isotopes.
- Soil characteristics: %DM, soil pH, and loss on ignition (LOI) for March and September 2017.
- Transfer parameters: used for calculating CR wo-soil values (vegetation-to-soil radionuclide transfer) for relevant species.

## Methods and measurements
- Radionuclide analyses:
  - Cs-137 in vegetation and soil measured with a high-purity germanium gamma detector; calibration with Cs-137/152Eu source; detection limit ~0.18 Bq per sample; uncertainties ~10–15%.
  - Sr-90 in vegetation and soil measured with a beta-spectrometer using a thin plastic scintillator; no radiochemical pre-treatment; daily calibration; uncertainties ~20%.
  - Am-241 and Pu isotopes: samples dissolved with HF and acids; Pu separated via anion exchange; americium separated and alpha-spectrometry performed; counting uncertainties typically <20%.
- Transfer parameter use:
  - Am-241 and Pu in grassy vegetation and wood inferred using published transfer parameters (CR wo-soil) from Red Forest references and CEZ sites.
  - Cs-137 and Sr-90 transfer for trees inferred using site-specific transfer parameters.
- Dose estimation:
  - External dose rates calculated with measured soil activity concentrations using the ERICA Tool v1.3.
  - Internal dose rates estimated with the revised R&D128 approach for appropriate media.
  - Ambient dose rates measured in situ complement modeled doses.

## Dose calculations and models
- Weighted absorbed dose rates computed for each isotope separately and then summed to produce total internal, external, and combined dose rates for:
  - Grassy vegetation
  - Deciduous tree wood
  - Bacteria
- Total site dose rates provided as sums across all isotopes and by individual isotopes.

## Data quality, uncertainty, and provenance
- Uncertainties reported for each radionuclide measurement (e.g., 10–15% for Cs-137, ~20% for Sr-90; alpha-spectrometry uncertainties <20%).
- Calibration and quality control anchored to established methods and references (e.g., Beresford et al., Bondarkov et al., Copplestone et al., Holiaka et al.).
- Transfer parameter data credited to specific personnel and publications; contributions acknowledged for data collation.
- Documentation includes method references, instrument models, and calibration sources to enable reproducibility.

## Dataset structure and variables (summary)
- Plot-level: plot number, location, pine forest past history, burn score, ambient dose rate (2016, 2017).
- Vegetation: FM/DM for grassy and other vegetation; radionuclide activity concentrations (Sr-90, Cs-137) in grassy vegetation (DM/FM) with uncertainties.
- Soil: five cores per plot aggregated; pH, moisture; activity concentrations (Sr-90, Cs-137, Am-241, Pu isotopes) in soil (DM); %DM and LOI (March/Sept 2017).
- Deciduous tree wood: estimated activity concentrations for Sr-90, Cs-137, Am-241, Pu isotopes (FM) using transfer parameters.
- Dose metrics: internal/external/total weighted absorbed dose rates by isotope and/or by media (grassy vegetation, deciduous wood, bacteria); total dose rates per plot and overall.
- Transfer parameters: CR wo-soil values used for specific media.

## Usage, sharing, and documentation considerations (Data Steward perspective)
- Rich, multi-media dataset with detailed metadata suitable for data discovery, governance, and reuse in ecological radiological studies.
- Clear documentation of sampling design, measurement methods, detection limits, uncertainties, and dose modeling approaches supports data provenance and reproducibility.
- Suitable for integration into data portals with standardized units, versioning, and cross-referencing to cited methods and transfer parameter sources.
- Requires careful handling of legacy data (e.g., previously used plots) and explicit metadata on plot history, burn status, and site-specific transfer parameters to ensure interoperability.
- Encouraged to publish alongside methodological references and to provide access to supporting software or calculator parameters (e.g., ERICA, R&D128) for reproducible dose estimations.