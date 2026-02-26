# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Purpose and Context
- Investigates radionuclide activity concentrations and calculated dose rates in soil, grassy vegetation, deciduous trees, and bacteria within the Red Forest, the most anthropogenically contaminated radioactive ecosystem on Earth.
- Examines the combined impact of radiation exposure and a secondary stressor (fire) after a severe 2016 fire burned ~80% of the Red Forest.
- RED FIRE project conducted in September 2017 with sixty study plots in burnt and unburnt areas and nine plots near Buriakivka village (~8 km from the Red Forest) to assess recovery dynamics.

## Study Design and Sampling
- Plot setup: 60 Red Forest plots (burnt and unburnt) plus 9 plots near the village.
- Sampling units: at each plot, a marked 1x1 m2 area for soil-related studies and measurements over 2017; an adjacent 1x1 m2 area to harvest vegetation (September 2017).
- Positioning: plot coordinates captured with GPS (accuracy ~3 m); many plots previously used by the TREE project.
- Burn assessment: burn score per plot (1 = no burn, 2 = some burnt areas, 3 = all plot burnt); pine forest history recorded from site observations.

## Data Collected
- Plot metadata: plot number, location, pine forest past history, burn score.
- Environmental context: ambient dose rate measured on soil surface in September 2016 and March 2017.
- Vegetation measurements: fresh mass (FM) and dry mass (DM) for grassy and other vegetation; grassy vegetation samples analyzed for radionuclide activity concentrations (Sr-90 and Cs-137) with uncertainties.
- Soil measurements: soil cores (five per plot: four corners and center) analyzed for pH, moisture, and radionuclide activity concentrations (Sr-90, Cs-137, Am-241, Pu isotopes) with DM measurements.
- Deciduous trees: estimated activity concentrations (FM) in wood for Sr-90, Cs-137, Am-241, Pu isotopes using site-specific transfer parameters.
- Bacteria: estimated total weighted absorbed dose rates.
- Transfer parameters: use of CR wo-soil values from literature for grasses (Agrostis gigantea) and wood (Pinus sylvestris) within Red Forest and CEZ sites.
- Additional dataset elements: LOI (loss on ignition) of soil, percentage soil DM, and detailed dose partitioning (internal/external) by isotope for grassy vegetation and deciduous wood, plus total dose rates.

## Analytical Methods
- Gamma spectrometry for Cs-137 using HPGe detector with calibration source; detection limit ~0.18 Bq per sample; uncertainties ~10–15%.
- Sr-90 determination via beta-spectrometry with thin plastic scintillator; uncertainties ~20%.
- Actinide analysis (Am-241, Pu isotopes): radiochemical separation, alpha spectrometry; traceable yield tracers added; multiple chemical steps; uncertainties <20%.
- Transfer parameter application: CR wo-soil values from Beresford et al. (2020) and Holiaka et al. (2020) to derive concentrations in grasses and wood from measured soil activities.
- Dose estimation:
  - ERICA Tool v1.3 used to estimate weighted absorbed dose rates to grassy vegetation and trees (external dose using measured soil activities).
  - Revised R&D128 spreadsheet model used to estimate weighted dose to bacteria.
  - Ambient soil surface dose rates measured at plot scale to contextualize results.

## Dataset Contents
- Plot details: number, location, pine forest past history, burn score, ambient dose rates (Sept 2016 and Mar 2017).
- Vegetation data: FM and DM for grassy and other vegetation; radionuclide concentrations (Sr-90, Cs-137) in grassy vegetation with uncertainties (DM and FM).
- Deciduous tree wood: estimated activity concentrations for Sr-90, Cs-137, Am-241, Pu isotopes (FM), derived via transfer parameters and soil concentrations.
- Soil data: activity concentrations (DM) for Sr-90, Cs-137, Am-241, Pu isotopes; %DM measured in March and September 2017; pH; LOI.
- Dose data: internal and external weighted absorbed dose rates by isotope for grassy vegetation and deciduous wood; total weighted absorbed dose rates by isotope and in aggregate for grassy vegetation, deciduous wood, and bacteria.
- Additional descriptors: burn score, ambient dose rate context, and metadata enabling replication and cross-site comparison.

## Key Findings and Implications
- While specific numerical results are not detailed in the summary, the dataset enables comparative analyses of radiation exposure across burnt vs. unburnt areas, different organisms (grassy vegetation, trees, bacteria), and multiple radionuclides (Sr-90, Cs-137, Am-241, Pu isotopes).
- The approach combines field measurements, laboratory analyses, transfer parameter usage, and standardized dose modeling (ERICA and R&D128) to produce comprehensive dose assessments in a recovering, fire-affected radioactive ecosystem.

## Data Governance, Quality, and Reuse
- Methods and datasets are documented with measurement uncertainties, calibration details, and references for transfer parameters and dose models to support reproducibility.
- Data are organized to support cross-study comparisons and methodological benchmarking in environmental radiological assessments.
- Acknowledges funding and collaborations; data collection builds on prior TREE project work, enhancing continuity and data discoverability for future research and governance.

## Challenges and Considerations for Data Leaders
- Fragmented data sources across field plots, laboratory analyses, and historical measurements; integration requires clear metadata and standardized units.
- Uncertainties vary by measurement type (e.g., gamma spectroscopy vs. beta-spectrometry vs. alpha spectrometry) and transfer parameter sources; careful propagation is essential.
- Dependence on site-specific transfer parameters necessitates careful documentation to enable transferability to other ecosystems or regions.