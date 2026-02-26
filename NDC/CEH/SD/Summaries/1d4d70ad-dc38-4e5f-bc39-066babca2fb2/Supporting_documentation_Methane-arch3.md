# Methane fluxes from peatland plateaus and thawing peatland plateaus and from burnt and unburnt forests from permafrost in subarctic Canada

## Objective
- Document methane flux measurements across peatland plateaus, thawing peatland features, and burnt/unburnt boreal forests in subarctic Canada (2013–2014).
- Establish a dataset to compare fluxes across different landscape features and fire histories, with detailed methodological guidance for replication and monitoring.

## Study sites and design
- 2013
  - Teslin, Yukon: peatland plateau (Teslin Peatland Plateau, TPP) with five replicates (TPP1–TPP5); adjacent thawing peatland plateau with margins and center locations:
    - TWM (margin)
    - T5M (about 5 m from margin)
    - TMID (center)
    - Each location had three replicates (e.g., TWM1–3, T5M1–3, TMID1–3)
  - FireFox region, about 100 km north of Whitehorse, Yukon: burnt vs unburnt black spruce forests
    - FFU (FireFox Unburnt) with five replicates
    - FFB (FireFox Burnt) with five replicates
- 2014
  - White Truck site near Yellowknife, Northwest Territories: peatland plateau named White Truck Plateau (WTP) with five replicates (WTP1–5)
  - Within White Truck, three thawing features:
    - WTM (White Truck Moss) – recent collapse feature; three replicates
    - WTS (White Truck Sedge) – recent collapse feature; three replicates
    - WTW (White Truck Wetland) – older collapse feature; one feature with three replicates
  - No burnt vs unburnt forest measurements in 2014
- Access considerations
  - Boardwalks constructed to access thawing features and minimize disturbance

## Measurement methodology
- Timing: methane flux measurements conducted during summers in 2013 and 2014
- Flux measurement setup
  - Ground collars of PVC tubes:
    - 160 mm diameter for peatland plateau and forest sites
    - 315 mm diameter for thawing features
  - Chambers: PVC tubes, 15–35 cm high, fitted on top of collars
  - Gas analysis: Detecto Pak-Infrared (DP-IR) methane gas analyser
  - Duration: Measurements monitored for up to 4 hours (based on rate of change)
  - Calibration: DP-IR calibrated with a certified 100 ppm CH4 standard; automatic self-test; measurements within 2 ppm of standard
  - Volume calculation: collar-ground distance used to compute headspace volume
  - Flux estimation: slope of linear regression of CH4 concentration vs. time; intercept and R^2 reported
- Environmental context during measurement
  - On-site air temperature (weather station)
  - Soil temperature at 5 cm and 10 cm inside the collar after chamber removal
  - Volumetric soil moisture at the surface (0–6 cm) using ML3 ThetaKit
  - Thaw depth measured with a metal rod until resistance encountered
  - Water table depth measured relative to a site datum established early in the season

## Data coding and structure
- Methane flux coding aligns with the soil profiles dataset
- Note: data for soil cores and methane fluxes come from different locations; GPS coordinates are provided in the dataset file

## Data quality assurance and calibration
- Quality control
  - DP-IR self-test and standard gas calibration
  - Use of certified 100 ppm CH4 standard; cross-checks within 2 ppm of standard
  - Regression-based flux estimation with reporting of slope, intercept, and R^2
- Replication and coverage
  - Multiple replicates per site/feature (e.g., 5 replicates for TPP; 3 replicates per thaw feature in 2013; 5 replicates for forest sites; 2014 thaw features with 3 replicates each per feature)

## Environmental measurements and context
- Measured variables alongside methane flux
  - Air temperature (on-site weather)
  - Soil temperature at 5 cm and 10 cm
  - Surface soil moisture (0–6 cm)
  - Thaw depth
  - Water table depth relative to a datum

## Data organization and metadata considerations
- Data units and structure
  - All measured variables provided per column in the dataset
  - Clear coding of site names, feature types, and replicate identifiers
- Data accessibility considerations for monitoring frameworks
  - Comprehensive documentation of site codes, feature classifications, replicates, and measurement protocols
  - Metadata notes highlight alignment with other datasets (soil profiles) and potential location-based data separation

## Implications for monitoring frameworks
- Strengths for policy-relevant monitoring
  - Clear experimental design comparing peatland, thaw features, and forest conditions (burnt vs unburnt)
  - Detailed measurement protocol enabling reproducibility and inter-study comparability
  - Inclusion of both flux measurements and key environmental context variables
- Potential challenges and considerations
  - 2014 absence of burnt/unburnt forest data limits cross-year comparisons for that feature type
  - Data coding relies on alignment with separate soil profile datasets; ensure consistent metadata schemas
  - Data access and sharing of underlying coordinates and datasets should consider data governance and privacy/operational constraints

## Limitations and notes
- 2014 dataset lacks burnt vs unburnt forest measurements
- Some features (e.g., WTW) are represented by a single feature with multiple replicates, which may affect spatial interpretation
- Data integration requires careful harmonization of methane flux data with soil profile datasets due to potential location differences across data types