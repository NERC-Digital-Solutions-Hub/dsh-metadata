# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2021-2022)

## Overview
- Reports an ammonia (NH3) enhancement experiment at Glencorse woodland near Edinburgh (Birch plantation) to study NH3 effects on vegetation, bryophytes, lichens, and soil.
- NH3 release is wind-controlled (275–345 degrees) and activated when threshold wind speeds are met.
- NH3 concentrations are measured in situ and used to drive a dry deposition model across a four-layer canopy, including soil, understory, trunks, and canopy surfaces.

## Data Collection and Content
- Location: Glencorse experimental site (latitude/longitude provided), altitude ~200 m.
- Timeframe: September 2021 to December 2022 (monthly NH3 analyses).
- Measurement approach:
  - NH3 concentrations measured at 1.5 m height along monitoring transect using ALPHA samplers (low-cost passive high-absorption).
  - Vertical NH3 concentrations measured at 25 cm intervals from 5 m to 3.5 cm above ground at 4, 10, and 16 m from the source.
  - Data used to model vertical concentration gradients and drive deposition estimates.
- Output: Deposition flux estimates to soil, understory, trunks, and canopy surfaces via a bi-directional resistance model.

## Measurements and Deposition Modeling
- Model framework:
  - Four-layer canopy compensation point model.
  - Bi-directional deposition with stomatal and soil re-emission components.
  - Deposition flux to soil uses quasi-laminar boundary layer resistance; trunk deposition uses boundary layer resistance around trunks; stomatal and cuticular fluxes parameterized with LAI dependencies.
- Key equations (conceptual):
  - Fχ(z) = χa / Rt (deposition flux at height z).
  - Rt combines resistances for soil, canopy, trunks, and stomatal/cuticular pathways.
- Parameterizations used for deposition components (soil, trunks, stomatal, cuticular) referenced from established sources (e.g., Schuepp, Nemitz, Massad, Jones, DEPAC, Sutton).
- Complete methodology and modeling details are provided in Deshpande et al. (2024).

## Data Quality and Provenance
- Quality control:
  - Visual checks for instrument malfunction, datalogger issues, and power cuts.
  - Obvious erroneous data removed; regular-missed values due to scheduled power cuts.
  - Some gaps due to sensor replacement and maintenance.
- Provenance:
  - Data produced from field measurements and modeled deposition fluxes, with explicit references to the underlying literature and models.

## Data Structure and Metadata
- Dataset size: 126 measurements across 17 parameters.
- File format: CSV with clearly described columns.
- Key columns (examples):
  - Distance (m; negative = southwest, positive = northeast from NH3 source)
  - Month (year-month)
  - NH3_conc_measured (µg m^-3)
  - NH3_conc_soil, NH3_conc_us, NH3_conc_ts, NH3_conc_tc (modelled NH3 concentrations at soil, understory, trunk, canopy levels; all in µg m^-3)
  - Deposition flux columns: Fg (soil), Fs_us (stomatal deposition to understory), Fw_us_* (various cuticular deposition parameterizations), Ftt (to trunks), Fs_tc, Fw_tc_* (canopy-related deposition), Fd_tc / Fd_us (alternative flux parameterizations)
- Metadata notes:
  - Distances are measured relative to the NH3 enhancement source.
  - Units and descriptions are provided for each parameter to support interpretability and reuse.

## Access, Reuse and Documentation
- Data availability: CSV dataset accompanying the publication; detailed methodology and analysis are described in Deshpande et al. (2024).
- Documentation references:
  - Empirical measurements and canopied deposition modeling methods are anchored in established studies (Fowler, Chamberlain, Nemitz, Massad, Jones, DEPAC, Sutton, etc.).
- Funding: UKRI GCRF South Asian Nitrogen Hub supported establishing the facility.

## Limitations and Considerations
- Data gaps due to scheduled power cuts and occasional sensor faults.
- Some measurement heights and vertical gradients rely on spatially distributed samplers, which may carry uncertainties related to deployment geometry and environmental conditions.
- Deposition estimates depend on multiple parameterizations; users should consider model choice and sensitivity when combining with other datasets.

## Funding and References
- Funding: UKRI GCRF South Asian Nitrogen Hub.
- Core references include Chamberlain (1968, 1984), Fowler (1978), Nemitz et al. (2000), Massad et al. (2010), Jones et al. (2007), DEPAC module (van Zanten et al., 2010), Sutton et al. (1998), and Deshpande et al. (2024).