# Supporting documentation for plant biomass and leaf-level functional traits from four different genotypes of sugarcane plants grown under a range of ozone conditions

## Overview
- Experimental data examining the impacts of ozone (O3) on four Saccharum sugarcane genotypes using the TropOz facility in Queensland, Australia.
- Two experimental runs with nine Open Top Chambers (OTCs) exposing plants to a semi-continuous O3 gradient (roughly 15–120 ppb).
- Data intended to support O3 dose–response analyses and linkage to regional vegetation models; accompanying paper Cheesman et al. (2023) and related data deposit.

## Experimental facility and plant material
- TropOz facility: nine independently controlled OTCs (22.2 m3 each) with calibrated O3 delivery and centralized monitoring of ozone, temperature, VPD, and PAR.
- Experimental runs:
  - Run 1: Badila, Q240, and CTC4 exposed for 96 days.
  - Run 2: Mandalay exposed for 100 days (started later due to growth).
- Genotypes:
  - Badila (Saccharum officinarum L. cv. Badila)
  - Mandalay (Saccharum spontaneum cv. Mandalay)
  - Q240 (commercial hybrid)
  - CTC4 (commercial hybrid)
- Growth conditions: plants grown in pots with high organic matter mix, watered daily, fertilized biweekly; full sun, no drought stress.

## Data collected and key metrics
- O3 exposure data:
  - Chamber-specific O3 concentrations (ppb) recorded frequently (approx. every 22 minutes).
  - Meteorological context: temperature, VPD, PAR, averaged at five-minute intervals.
- Plant measurements:
  - Biomass partitioning into leaf, stalk, and roots after harvest; leaf area and leaf mass per area (LMA) from L+1 leaf.
  - final biomass and detailed leaf/plant traits captured in Sugarcane_Biomass.
- Gas exchange and stomatal metrics:
  - Stomatal conductance (gs) measured with porometer and Li-6400XT; data converted to Relative Stomatal Conductance (RSC).
  - DO3SE-based phytotoxic ozone dose (PODy) calculated per genotype-chamber, with y thresholds (0 and 2 nmol m-2 s-1) to support regional simulations.
- Dose–response and exposure metrics:
  - AOT40 (ppm h) concentration-based exposure metric.
  - PODy (with y = 0 to 8 nmol m-2 s-1) derived using DO3SE, calibrated with gas-exchange data.
  - Dose–response for relative biomass decline estimated against PODy.
- Quality control:
  - Cross-checks of O3 data against zero-air standards; meteorological data validated against local station; biomass verification with annually calibrated scales and outlier reweighing.

## Data files deposited
- Sugarcane_O3.csv: O3 concentrations (ppb) for nine chambers during the first experiment; columns include date and Chamber_1 to Chamber_9.
- Sugarcane_Mandalay_O3.csv: O3 concentrations (ppb) for nine chambers during the second experiment (Mandalay); similar structure.
- Sugarcane_Met_5min.csv: environmental conditions (5-minute averages) for the first experiment; columns include AirTC_Avg, RH, PAR_Den_Avg, Datetime.
- Sugarcane_Mandalay_Met_5min.csv: environmental conditions (5-minute averages) for the second experiment.
- Calculated_PODy.csv: 14 columns of calculated PODy values across four genotypes, for various chamber and threshold combinations (POD2, POD6, POD0–POD8, AOT40, etc.).
- Sugarcane_Biomass.csv: 28 columns detailing final biomass, leaf traits, stems, roots, and total biomass per plant, with Genotype, Plant_ID, Chamber_ID, Date, New/Old Leaf metrics, leaf areas, LMA, stem counts, biomass totals, and a Flagged flag for removal notes.
- Note: Mandalay gas-exchange data could not be collected with the same method as others; some environmental differences between runs are acknowledged and should be accounted for in analyses.

## Data quality and validation
- Data collected with factory-calibrated sensors; cross-validated with local meteorological station data.
- O3 concentrations checked against zero-air standards every 22 minutes.
- Biomass measurements taken with annually calibrated scales; reweighing used to confirm suspected outliers after extended drying.

## Potential data products and reuse
- Dose–response modeling: link biomass decline to PODy and AOT40 across genotypes to derive genotype-specific sensitivity.
- Regional model integration: PODy (0 and 2 nmol m-2 s-1 thresholds) enables budgeting of O3 losses under dynamic environmental conditions for larger-scale vegetation models.
- Comparative analyses: cross-genotype comparisons of biomass allocation (leaf, stalk, root) and leaf traits (LMA) under differing O3 exposures.
- Dashboards or self-serve insights: make PODy, AOT40, gs/RSC, and biomass metrics explorable by genotype, chamber, and exposure level.
- Documentation alignment: data are designed to be used in conjunction with Cheesman et al. (2023) and the TropOz facility data.

## Considerations for reuse
- Two experimental runs experienced different environmental conditions; adjust dose–response interpretation accordingly.
- Mandalay data had limited gs measurements; rely on control-chamber data and DO3SE calibration where direct measurements are unavailable.
- Threshold selections for PODy (e.g., 0 vs 2) influence cross-study comparability; the dataset provides multiple POD thresholds for flexibility.

## References
- Cheesman et al. (2023). Impacts of ground-level ozone on sugarcane production. Science of the Total Environment.
- Emberson (2020); Jarvis (1976); Hayes et al. (2020a); Agathokleous & Saitanis (2020); Agathokleous et al. (2019); Moura et al. (2018b); Pleijel et al. (2022); Kreyling et al. (2018) – methodological context for DO3SE and dose–response approaches.