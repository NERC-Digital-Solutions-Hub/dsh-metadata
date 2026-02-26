# EIDC Supporting information
Monthly atmospheric ammonia, acid gas, inorganic aerosols and base cation concentrations from Northern Ireland DELTA gas and aerosol monitoring network, 2019-2020

## What the data include
- Monthly atmospheric concentrations (µg m-3) for 2019 and 2020 from four Northern Ireland DELTA gas and aerosol monitoring sites.
- Gases: ammonia (NH3), nitric acid (HNO3), sulphur dioxide (SO2).
- Aerosols: ammonium (NH4+), nitrate (NO3-), sulphate (SO4 2-), chloride (Cl-), sodium (Na+), calcium (Ca2+), magnesium (Mg2+).
- Joint operation by Agri-Food and Biosciences Institute (AFBI) and UK Centre for Ecology & Hydrology (UKCEH); funded by DAERA, Northern Ireland.

## Purpose and application
- Extend spatial monitoring across NI to better understand atmospheric composition and regional variability.
- Concurrent measurement of gas and aerosol components to examine NH3 interactions with acid gases (HNO3, SO2) and inorganic particulate matter.
- Provide data for testing atmospheric transport models and estimating annual budgets of reduced nitrogen (NH3, NH4+) vs oxidised nitrogen (HNO3, NO3-) and sulphur.

## Monitoring network and sites
- Four DELTA sites across NI (to increase spatial coverage beyond the two AGANet NI sites):
  - Hillsborough (AFBI25)
  - Ballynahone (AFBI26)
  - UoU Coleraine (AFBI27)
  - Sandholes (AFBI28)
- Start dates in 2019; ongoing monitoring at these sites during 2019–2020.
- Sites measured monthly with time-integrated sampling.

## DELTA method and sampling
- UKCEH DELTA system: low-volume diffusion denuder method for long-term monitoring of reactive gases (NH3, HNO3, SO2) and aerosols (NH4+, NO3-, SO4 2-, Cl-, Na+, Ca2+, Mg2+).
- Sampling rate: 0.2–0.4 L min-1; monthly exposure cycles; gas meters record sampled air volume.
- Sample train includes denuders for gases and downstream aerosol filters; extracts analyzed in UKCEH Lancaster laboratory.
- Exposure window: monthly cycles aligned to calendar months (±5 days).

## Analytical methods and detection limits
- Gases and aerosols are analyzed from aqueous extracts or filters:
  - Gases: NH3 (DA), HNO3 and SO2 (DC1/DC2); HONO suspected but not reported due to interference.
  - Aerosols: NH4+, NO3-, SO4 2-, Cl-, Na+, Ca2+, Mg2+ (PT); additional NO3-, Cl- (FPH) and NH4+ (FPA) components.
- Analytical methods:
  - IC for most anions (NO3-, SO4 2-, Cl-).
  - SEAL-AA3 for NH4+.
  - ICP-OES for Na+, Ca2+, Mg2+.
- Typical detection limits (one month exposure, volume ~15 m3):
  - Gases: NH3 0.01 µg m-3 (NH4+), HNO3 0.05 µg m-3 (NO3-/SO4 2-), SO2 0.05 µg m-3.
  - Aerosols: NH4+ 0.02 µg m-3, NO3- 0.06 µg m-3, SO4 2- 0.06 µg m-3, Cl- 0.16 µg m-3, Ca2+ 0.09 µg m-3, Mg2+ 0.05 µg m-3, Na+ 0.16 µg m-3.

## Data structure and output
- Data stored and processed in the UKCEH AAGA (Oracle-based) database; concentrations are time-integrated averages for the exposure period.
- Final outputs are ratified, time-stamped, and version-controlled.
- Dataset fields cover: site_id, site_name, network_id (AFBI), parameter_id (gas/aerosol species), measurement_start/end dates and times, concentration, detection flags, verification status, data capture status, unit, and data status code.
- Each row represents one month of data for a single site; site names are linked to spatial identifiers.

## Quality control and data validation
- Multi-stage QC process (three stages) with automated and manual checks:
  - Stage 1: Auto-flagging and automated checks (e.g., date overlaps, sampling duration, flow rate, outliers, missing samples).
  - COVID-related adjustments: extended exposure periods observed Apr–Jun 2020 and flagged accordingly.
  - Stage 2: Manual review of monthly blanks, ion balance checks (Na+:Cl-, NH4+:NO3-+SO4 2-), sampling malfunctions, and outliers.
  - Stage 3: Expert review by experienced air quality scientists considering site context, regional patterns, expected concentrations, and cross-site comparisons.
- After corrections, a final locked output is produced with a “Ratified” status.

## Data flags and quality indicators
- Flags follow the European EBAS/EMEP conventions, grouped into Valid, Missing, and Invalid categories.
- Examples of common flags:
  - 147 V: below detection limit but reported and considered valid.
  - 999 M: missing data.
  - 699 I / 668 V: mechanical or instrumental issues (e.g., damaged filters, flow anomalies).
  -  skip details: many specific flags indicating contamination, coating errors, co-located instrument data, or extreme values.
- Flags are standardized to harmonize data submissions across networks (EMEP/EBAS).

## Access, references, and resources
- EN 17346: European standard for ammonia determination using diffusive samplers.
- Key publications documenting the methodology and network context (AGANet, NAMN) and pan-European monitoring findings.
- Resources and flags:
  - AGANet network information: https://uk-air.defra.gov.uk/networks/network-info?view=aganet
  - NAMN NH3 monitoring protocols: https://uk-air.defra.gov.uk/networks/network-info?view=nh3
  - EBAS flag index: https://projects.nilu.no/ccc/flags/