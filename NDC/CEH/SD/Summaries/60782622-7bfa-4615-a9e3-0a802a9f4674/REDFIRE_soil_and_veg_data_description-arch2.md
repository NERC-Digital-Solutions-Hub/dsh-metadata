# Soil and vegetation radionuclide activity concentrations and calculated dose rates from the Red Forest, Chernobyl, Ukraine (2016-2017)

## Aim and Context
- Investigates radiation impacts on a highly contaminated ecosystem (Red Forest) after a severe 2016 fire.
- RED FIRE project set up 60 study plots in burnt and unburnt areas, plus 9 plots near Buriakivka (~8 km from Red Forest).
- Objectives: measure radionuclide activity concentrations in grassy vegetation and soil; estimate total weighted absorbed dose rates to grassy vegetation, deciduous trees, and bacteria; compare burnt vs unburnt areas; use standardised methods to enable temporal/environmental health assessment.
- Data support understanding environmental recovery under a secondary stressor (fire) in a chronically contaminated site.

## Study Sites and Sampling
- September 2017: 60 plots in Red Forest (burnt and unburnt) and 9 plots near Buriakivka.
- At each plot:
  - Marked 1x1 m2 area for soil studies; adjacent 1x1 m2 area for vegetation harvest.
  - GPS coordinates recorded (accuracy ~3 m).
  - Plot burn history recorded as a burn score (1 = no burn, 2 = some burn, 3 = all plot burnt).
  - Pine forest past history inferred from site observations and local knowledge.
- Sampling period spanned 2017 for plot-based measurements; some plots previously used by the TREE project.

## Sample Preparation, Analytical Methods and Dose Estimation
- Vegetation:
  - Harvested in September 2017; sorted into grassy vs other vegetation.
  - Fresh mass (FM) and dry mass (DM) recorded; grassy vegetation homogenised for analysis.
- Soil:
  - Cores (2.5 cm diameter, 10 cm deep) collected from plot corners and center; bulked and homogenised.
  - Subsamples for pH, moisture; remaining soil for radionuclide analysis; samples dried prior to analysis.
- Radionuclide Analyses:
  - Cs-137: measured with high-purity germanium gamma detector; calibration with a Cs-137/152Eu source; minimally detectable activity ~0.18 Bq per sample; uncertainties ~10–15%.
  - Sr-90: measured with a beta-spectrometer (EXPRESS-01) using solid-state samples; uncertainties ~20%.
  - Am-241 and Pu isotopes: radiochemical separation (yield tracers 242Pu and 243Am); HF/HNO3 dissolution, anion exchange, resin separations; alpha spectrometry for isotopes; counting errors typically <20%.
- Transfer and Dose Modelling:
  - Activity concentrations in grassy vegetation and deciduous trees used with site-specific transfer parameters (CR_wo-soil) from published studies to estimate concentrations in wood/biomass.
  - ERICA Tool v1.3 used to estimate weighted absorbed dose rates (µGy h-1) for grassy vegetation and trees (external dose from soil activity concentrations).
  - R&D128 (Revised) model used to estimate weighted absorbed dose to bacteria.
  - Ambient dose rate on the soil surface measured at each plot in Sept 2016 and March 2017 using a MKS-01R meter.

## Data Collected and Dataset Contents
The dataset comprises the following, per plot and sample:
- Plot metadata: plot number, location, pine forest past history, burn score.
- Ambient dose rates: measured Sept 2016 and March 2017 (µSv h-1).
- Vegetation measurements: FM and DM for grassy and other vegetation.
- Grass/soil radionuclide activity concentrations (DM and FM) for Sr-90 and Cs-137 with uncertainties.
- Deciduous tree wood activity concentrations (FM or DM) for Sr-90 and Cs-137 (calculated using transfer parameters and soil activity concentrations).
- Grassy vegetation and deciduous tree wood activity concentrations for Am-241, Pu-238, Pu-239, Pu-240 (calculated using transfer parameters and soil activity concentrations).
- Soil activity concentrations (DM) for Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240.
- Soil DM percentage (DM%) at each plot for March and September 2017.
- Soil properties: soil pH, Loss on Ignition (LOI).
- Dose calculations:
  - Internal weighted absorbed dose rate by isotope (Sr-90, Cs-137, Am-241, Pu-238, Pu-239, Pu-240) for grassy vegetation.
  - External weighted absorbed dose rate by isotope for grassy vegetation.
  - Total weighted absorbed dose rate by isotope for grassy vegetation (internal + external).
  - Total weighted absorbed dose rate for grassy vegetation (all isotopes).
  - Internal, external, and total weighted absorbed dose rates by isotope for deciduous tree wood.
  - Total weighted absorbed dose rate for deciduous tree wood (all isotopes).
  - Total weighted absorbed dose rate by isotope and in aggregate for bacteria.
- The dataset includes uncertainties for activity concentrations and dose estimates, reflecting measurement and calculation precision.

## Dose Calculation Methods and Outputs
- External dose estimates rely on measured soil activity concentrations.
- Internal dose estimates incorporate transfer parameters (CR_wo-soil) from relevant studies for grasses, trees, and bacteria.
- Absorbed dose rates are reported per isotope and as total sums, for grassy vegetation, deciduous trees, and bacteria.
- Ambient dose rates provide contextual exposure at soil surfaces.

## Uncertainties, Detection Limits and Quality Considerations
- Cs-137 detection limit ~0.18 Bq per sample; uncertainties ~10–15% for gamma measurements.
- Sr-90 uncertainties ~20% for beta-spectrometry measurements.
- Alpha spectrometry for Am-241 and Pu isotopes includes typical counting errors <20%.
- Data capture includes FM/DM, plot-level burn history, soil properties, and uncertainties to support transparent interpretation and cross-study comparisons.

## Potential for Data Use and Reuse
- Standardised dataset enabling temporal and spatial comparisons of radionuclide activity and dose across burnt/unburnt conditions.
- Compatible with environmental monitoring workflows (data verification, quality assurance, cleaning, and transformation).
- Datasets and transfer parameters enable cross-site comparisons and integration with broader Chernobyl Exclusion Zone data.
- Opportunities to increase value by combining with additional environmental datasets and by sharing underlying data for broader scrutiny and policy analysis.

## Acknowledgements and Funding
- Funded by NERC (Grant NE/P015212/1) for the RED FIRE project.
- Acknowledges contributions from Ukrainian collaborators and support from UKCEH.