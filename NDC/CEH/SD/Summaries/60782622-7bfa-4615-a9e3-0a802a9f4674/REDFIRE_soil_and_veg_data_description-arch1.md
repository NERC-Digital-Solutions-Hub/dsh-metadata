# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Investigates the recovery of the Red Forest, the most anthropogenically contaminated radioactive ecosystem, after a severe July 2016 fire that affected ~80% of the area.
- RED FIRE project established 60 study plots (burnt and unburnt) in the Red Forest and 9 plots near Buriakivka (~8 km away).
- Data include plot details, radionuclide activity concentrations in grassy vegetation and soil, and estimated dose rates to grassy vegetation, deciduous trees, and bacteria.
- External dose rate estimates for grassy vegetation available where grassy vegetation was present; no dose estimates for grass where absent.

## Study design and sampling
- Fieldwork conducted in September 2017.
- Plot design: 1 x 1 m2 plots for soil-related measurements and vegetation sampling; an adjacent undisturbed 1 x 1 m2 area for vegetation harvest.
- GPS coordinates recorded for all plots (accuracy ~3 m).
- Burn history captured as a burn score (1 = no burn, 2 = some burn, 3 = all plot burnt).
- Additional context: pine forest past history obtained from site observations and local knowledge.
- Most Red Forest plots previously used in the TREE project.

## Measurements and laboratory analyses
- Vegetation: harvested in September 2017; samples sorted into "grassy" and "other" vegetation; fresh mass (FM) and dry mass (DM) recorded; grassy samples homogenised for radionuclide analyses.
- Soil: collected as five cores per plot (2.5 cm diameter, 10 cm depth); cores pooled and homogenised; sub-samples analysed for pH and moisture; remaining material analysed for radionuclides after drying.
- Radionuclides measured:
  - Cs-137 and Sr-90 activity concentrations in grassy vegetation and soil (via gamma spectrometry and beta spectrometry, respectively).
  - Am-241, Pu-238, Pu-239, Pu-240 activity concentrations in soil and grassy vegetation using radiochemical separation and alpha spectrometry.
  - Transfer parameters (CR wo-soil) used to estimate activity concentrations in deciduous tree wood and grassy vegetation for specific isotopes.
- Calibration and detection:
  - Cs-137: high-purity germanium gamma detector; calibration with a Cs-137/Eu-152 source.
  - Sr-90: beta-spectrometry with a thin-film plastic scintillator; daily calibrations.
  - Am/Pu: radiochemical separation, alpha spectrometry; yield tracers added; typical counting uncertainties <20%.
- Additional measurements:
  - Soil pH, moisture, and loss on ignition (LOI) to characterise soil properties.
  - Ambient soil surface dose rate measured at each plot in Sept 2016 and March 2017 using a MKS-01R meter.
- Dose estimation tools:
  - ERICA Tool version 1.3 for weighted absorbed dose rates to grassy vegetation and trees (external dose based on measured soil activity).
  - Revised R&D128 model for weighted absorbed dose to bacteria.
  
## Data products and contents
Dataset comprises (per plot and sample type):
- Plot metadata: number, location, pine forest past history, burn score.
- Ambient dose rates: Sept 2016 and Mar 2017.
- Plant/soil masses: FM and DM for grassy and other vegetation samples.
- Radionuclide activity concentrations:
  - Grass samples (FM and DM) for Sr-90 and Cs-137 with uncertainties.
  - Deciduous tree wood (FM/DM) estimated Sr-90 and Cs-137 concentrations using transfer parameters and soil concentrations.
  - Grass and tree wood for Am-241, Pu-238, Pu-239, Pu-240 (FM/DM) using transfer parameters and soil concentrations.
  - Soil concentrations (DM) for Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240.
  - Percent DM of soil at each plot measured in March and September 2017.
  - Soil pH and LOI at each plot (Sept 2017).
- Dose calculations:
  - Internal and external weighted absorbed dose rates by isotope for grassy vegetation.
  - Total weighted absorbed dose rates by isotope for grassy vegetation.
  - Internal, external, and total weighted absorbed dose rates by isotope for deciduous tree wood.
  - Total weighted absorbed dose rates by isotope for bacteria (and overall total for all isotopes).
- Additional context:
  - Burn score and associated plot burn status.
  - Transfer parameter references and site-specific parameter usage across different matrices.

## Key outputs and significance
- Provides a comprehensive, multi-matrix dataset linking radionuclide contamination (Sr-90, Cs-137, Am-241, Pu isotopes) to ecological media (grass, other vegetation, deciduous trees, bacteria) under post-fire conditions.
- Enables estimation of radiation dose rates to vegetation, trees, and microbes, facilitating assessment of ecological recovery under a composite stressor (radiation plus fire).
- Uses established radiological assessment tools (ERICA) and dose-models (R&D128) to quantify ecological exposure.
- Data facilitate cross-matrix comparisons (soil–vegetation–wood) and spatially explicit analyses (plot-level burn status, ambient dose rates, soil properties).

## References and acknowledgements
- Methods and transfer parameters drawn from Beresford et al. (2020), Holiaka et al. (2020), and related ERICA and R&D128 literature.
- Acknowledges support from the NERC RED FIRE project (NE/P015212/1) and contributions from Ukrainian and UK collaborators. RED FIRE project page: https://www.ceh.ac.uk/redfire