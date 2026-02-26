# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Overview
- Investigates how radiation from the Chernobyl accident persists in the Red Forest ecosystem after a major 2016 fire.
- Implemented the RED FIRE project to study 60 plots in burnt and unburnt areas, plus 9 plots near Buriakivka, focusing on soil and vegetation radionuclide activity concentrations and derived dose rates.
- Aims to produce data suitable for map-based interpretation of spatial patterns in contamination and radiation exposure.

## Spatial sampling design
- 60 study plots within the Red Forest (burnt and unburnt) and 9 plots near Buriakivka (~8 km from the Red Forest).
- At each plot:
  - A 1 x 1 m2 area used for soil-related measurements; an adjacent 1 x 1 m2 area harvested for vegetation.
  - Plot coordinates recorded with GPS (accuracy ~3 m).
  - Burn history documented via a burn score (1 = no burn, 2 = some areas burnt, 3 = all plot burnt).
- Prior use of plots by the TREE project informed design and location.

## Field methods and laboratory analyses
- Vegetation sampling (September 2017): harvested both grassy vegetation and other vegetation; samples separated into grassy and other; fresh mass measured; samples air-dried and mass recorded; grassy vegetation homogenised for analysis.
- Soil sampling (September 2017): five cores per plot (2.5 cm diameter, 10 cm deep) collected (corners and center); cores bulked per plot, homogenised; subsamples for pH and moisture; remaining material dried for radionuclide analysis.
- Radionuclide measurements:
  - Cs-137 in grassy vegetation and soil by gamma spectrometry (HPGe detector).
  - Sr-90 in grassy vegetation and soil by beta spectrometry (thin-film plastic scintillator).
  - Am-241 and Pu isotopes in soil and vegetation via radiochemical separation and alpha spectrometry.
- Calibration and detection limits:
  - Cs-137 minimum detectable activity ~0.18 Bq per sample; Sr-90 uncertainties ~20%.
  - Isotope transfer parameters used for dose calculations based on prior studies and CEZ-site data.
- Dose calculations:
  - External dose rates computed from measured soil activity using the ERICA Tool v1.3.
  - Internal and external dose components computed for grassy vegetation, deciduous tree wood, and bacteria; total dose rates derived by summing per-isotope contributions.
  - Ambient external dose rate measured on soil surface at each plot in Sep 2016 and Mar 2017.

## Dose estimation and transfer parameters
- Transfer parameters (CR wo-soil) for deciduous trees and grasses drawn from:
  - Agrostis gigantea (grassy vegetation) within Red Forest (Beresford et al. 2020).
  - Pinus sylvestris (wood) within Red Forest (Beresford et al. 2020).
  - Deciduous trees from CEZ sites (Holiaka et al. 2020) for Sr-90 and Cs-137.
- Additional Am-241 and Pu isotopes transfer parameters applied to grasses and deciduous wood.
- Dose calculation framework:
  - ERICA Tool v1.3 used to estimate weighted absorbed dose rates (µGy h-1) for grassy vegetation and trees.
  - R&D128 methodology applied to estimate bacterial dose rates.
  - Ambient soil surface dose rates used for external exposure input.

## Dataset and variables
The dataset comprises plot- and sample-level information, including:
- Plot metadata: plot number, location, pine forest past history, burn score.
- Environmental measurements: ambient dose rate (Sep 2016, Mar 2017).
- Biomass data: fresh mass (FM) and dry mass (DM) for grassy and other vegetation.
- Radionuclide activity concentrations:
  - Grassy vegetation: Sr-90 and Cs-137 (DM and FM, with uncertainties).
  - Soil: Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240 (DM).
  - Estimated activity concentrations in deciduous tree wood for Sr-90, Cs-137, Am-241, Pu isotopes (via transfer parameters and soil concentrations).
- Dose data:
  - Internal, external, and total weighted absorbed dose rates by isotope for grassy vegetation.
  - Internal, external, and total weighted absorbed dose rates by isotope for deciduous tree wood.
  - Internal, external, and total weighted absorbed dose rates for bacteria.
  - Totals: per-isotope and overall total weighted dose rates (µGy h-1).
- Soil properties: pH, moisture percentage, loss on ignition (LOI) at each plot (Sept 2017; some March 2017 data).
- Additional derived measures: DM percentages, and site-specific parameters (e.g., burn history context).

## GIS relevance and potential uses
- Enables spatial visualization of radionuclide distributions and radiological risk across the Red Forest and surrounding areas.
- Can be integrated with other GIS layers (soil properties, burn history, ambient dose rates) to analyze drivers of contamination patterns.
- Supports hotspot identification, temporal comparisons (2016–2017 ambient rates), and assessment of fire disturbance on radiological exposure.
- Provides a rich, plot-based dataset suitable for map-based decision support, policy briefings, and public-facing visualisations.

## Data quality and caveats
- GPS accuracy ~3 m; plot-level uncertainties inherent in radiochemical measurements (noted for Sr-90 and Cs-137).
- Transfer parameter uncertainties influence estimated activity concentrations in vegetation and wood.
- Multiple data sources for transfer factors (Red Forest and CEZ) applied to different components of the dataset.
- Ambient dose rates represent specific measurement times (2016 and 2017) and may not capture all temporal variability.

## References and acknowledgements
- Methodological and transfer parameter sources include Beresford et al. (2020), Holiaka et al. (2020), Bondarkov et al. (2002, 2011), and Copplestone et al. (2001).
- Acknowledges field and data support from Ukrainian and UK institutions; funded by NERC grant NE/P015212/1 (RED FIRE).