# Exposure of Burrowing Mammals to Rn-222 in Northwest England - MATERIALS & METHODS

## Overview
- Seven field sites in northwest England chosen to span a range of radon potential categories (less than 1% to greater than 30% of homes exceeding the UK Action Level of 200 Bq m^-3), based on radon-potential maps from Miles et al. (2007).
- Sites 1, 6, and 7 located in limestone-like bedrock and had the highest radon potentials.
- Experimental setup involved constructing artificial burrows (three per site, except Site 1 with one due to shallow soil) to study burrow air radon exposure.
- Data collected through multiple measurement methods from July 2009 to June 2010, with some late-start dates (Sites 6–7) and site-specific adjustments.

## Data types and collection methods
- Passive radon measurements
  - PADC/CR-39 detectors housed in diffusion chambers within artificial burrows; moistureresistant design in 200 µm polyethylene bags.
  - Detectors replaced every 4–6 weeks; results reported as time-integrated radon exposure (kBq 222Rn h m^-3) and converted to concentrations (kBq m^-3) using exposure duration.
  - Rodent damage occasionally occurred; mitigated by placing poultry wire around detectors.
- Active radon measurements
  - AlphaGUARD instrument measured burrow air directly via a probe inserted ~90 cm into each burrow at 1 L/min, with repeated one-minute readings and purging between readings.
  - Measurements also taken in three natural burrows near Site 1 for comparison.
- Soil gas radon measurements
  - 0.8 cm tubes driven to ~80 cm depth (blocked by rock/root constraints at times).
  - Gas pumped into Lucas scintillation cells linked to Pylon AB5 monitor; three one-minute counts used to determine Bq m^-3 after background subtraction.
  - Calibration with HPA FRED method; measurements taken at three spots around each artificial burrow (approximately 1 m from detector).
- Soil moisture and temperature
  - 0–10 cm soil samples near each burrow collected with each detector change to determine moisture by drying at 60°C.
  - Temperature monitored by Tinytag data loggers placed ~30 cm from the burrow end at ~50 cm depth; loggers record every 30 seconds and are downloaded in the field.
- Timing and site notes
  - Detector fitting/removal dates recorded; occasional burrow relocation due to water ingress or other issues.
  - Site 7 measurements occurred only after establishment in October 2009, limiting AlphaGUARD measurements there.

## Data processing and dosimetry
- Dosimetric approach
  - Adapted whole-body dose conversion coefficients (DCCs) for 222Rn in equilibrium with short-lived daughters, using an allometric framework to scale for different animal geometries (mouse-like, rabbit-like, fox-like) representing small herbivores, larger mammals, etc.
  - Considered three exposure scenarios from Vives i Batlle et al., adapting for burrow air exposure by treating burrow air akin to above-ground air exposure; soil immersion exposure not estimated.
  - Equilibrium factor (F) between radon and progeny is uncertain for burrows; standard human indoor value not applicable. Used an assumed F of 0.8 (discussed in the text; sensitivity acknowledged).
  - Equilibrium equivalent concentration (EEC) derived by multiplying measured 222Rn concentration by F.
  - Dose conversions performed with a spreadsheet implementation, using a weighted alpha factor of 10 (instead of 20) to align with wildlife background dose-rate estimates.
- Data products
  - Concentrations and derived doses calculated for small rodent, herbivorous mammal, and carnivorous mammal geometries; results applicable to species inhabiting underground burrows.

## Quality assurance, metadata, and provenance
- QA/QA-steps embedded in methods
  - Use of a single detector batch (PADC from the same batch) to maintain consistency; quality criteria aligned with HPA standards.
  - Detectors stored in controlled conditions before use; periodic validation via control detectors returned to HPA.
  - Systematic recalibration and field checks of instruments (AlphaGUARD, Lucas cells, Pylon monitor) with documented calibration procedures.
- Metadata and documentation
  - Site radon potential category and bedrock-type context recorded for each site.
  - Detailed procedural notes on burrow construction, detector placement, relocation, and rodent damage mitigation.
  - Logs maintained for detector change dates, sampling times, and environmental conditions (soil moisture, soil temperature).
- Data lineage and transparency
  - Multiple measurement modalities documented (passive detectors, active buron measurements, soil gas measurements, environmental parameters) enabling cross-validation and reproducibility.
  - Calculations and assumptions (F value, DCC selection, geometry choice, data conversions) clearly described to enable re-analysis or alternative modeling.

## Limitations and practical challenges
- Uncertainty in radon-progeny equilibrium within burrows; F value not empirically measured for burrows and may vary with ventilation.
- Field limitations:
  - Some burrows were relocated due to water ingress; measurement opportunities varied by site.
  - Rock and root obstacles prevented full-depth soil gas sampling at all locations and depths.
  - Site 7 lacked AlphaGUARD measurements due to late establishment.
- Data gaps
  - Not all sites/features had identical measurement coverage (e.g., soil depth sampling variability; some sites missing certain measurements at specific times).

## Data governance considerations for Data Stewards
- Dataset readiness and standards
  - Comprehensive, multi-modal radon-related data with robust procedural metadata suitable for repository submission and reuse.
  - Clear documentation of field site context (radon potential, bedrock), detector batches, calibration status, and measurement intervals.
- Data quality and reproducibility
  - QA records, control detectors, and storage/handling notes enhance trustworthiness and enable independent verification.
  - Transparent handling of assumptions (e.g., equilibrium factor F) and their impact on dose estimates.
- Data sharing and stewardship implications
  - Suitable for deposition in environmental/radiation data portals with standardized units (Bq m^-3, kBq m^-3, etc.) and accompanying metadata.
  - Potential need to provide access to supporting materials (raw detector counts, calibration files, and dosimetry calculators) to enable independent reuse or reanalysis.
- Limitations to disclose for users
  - Burrow-specific F values are assumed rather than measured; dose estimates depend on this assumption.
  - Variable site coverage and occasional measurement gaps due to field conditions.