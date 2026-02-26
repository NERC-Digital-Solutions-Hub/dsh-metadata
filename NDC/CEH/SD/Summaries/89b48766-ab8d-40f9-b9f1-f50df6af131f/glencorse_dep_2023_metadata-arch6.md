# Ammonia concentration and deposition data from Glencorse experimental site near UKCEH, Edinburgh (2023)

- Purpose: Provide ammonia concentration and deposition data from a wind-controlled NH3 enhancement experiment in a Birch plantation to study NH3 effects on forest vegetation, bryophytes, lichens, and soil.
- Location and timing: Glencorse woodland, near Edinburgh, UK (latitude 55.8539, longitude -3.2151; altitude 200 m). Data collected January 2023 to December 2024.
- Sampling system: NH3 released only when wind direction is 275–345 degrees and wind speeds exceed 0.31 m s-1; concentrations measured at 1.5 m height along monitoring transect using ALPHA low-cost samplers; monthly analysis.

## Data and methods

- Measurements and heights:
  - NH3 concentration at multiple vertical layers along the transect:
    - 1.5 m height (monitoring quadrats)
    - Soil surface (0.05 m)
    - Understorey (0.5 m)
    - Trunk surfaces (1.75 m)
    - Canopy (3.5 m)
- Deposition modelling:
  - Bi-directional resistance model to estimate deposition (and emission) to soil, understory vegetation, tree trunks, and tree canopy.
  - Deposition flux formula relates ambient NH3 concentration, total resistance to dry deposition, and deposition velocity.
  - Soil surface deposition uses quasi-laminar boundary layer resistance; trunk deposition uses quasi-laminar boundary layer around trunks; stomatal, cuticular, and capacitance resistances are parameterized for understorey, canopy, and leaves with multiple parameterizations.
  - Five parameterizations used for cuticular deposition (and one capacitance case) with Leaf Area Index (LAI) dependence; includes DEPAC module (van Zanten et al. 2010), Massad et al. 2010, Jones et al. 2007, Sutton et al. 1998, and additional formulations.
  - Stomatal deposition flux model uses Rs, with an LAI dependency and bounds (RsMax, RsMin, solar radiation influence).
- Model improvements:
  - Current model simulates NH3 concentration peaks during NH3 release to estimate deposition; prior version used mean monthly NH3 concentrations to drive deposition. The new approach better captures peak deposition during release periods.

## Data structure and contents

- Dataset size: 108 measurements of 17 parameters.
- Format: CSV with columns including:
  - Distance (m) from NH3 source
  - Month (year-month)
  - NH3_conc_measured (µg m-3) – monthly average at 1.5 m
  - NH3_conc_soil (µg m-3) – soil surface
  - NH3_conc_us (µg m-3) – understory
  - NH3_conc_ts (µg m-3) – trunk surfaces
  - NH3_conc_tc (µg m-3) – canopy
  - Fg, Fs_us, Fw_us_Massad, Fw_us_DEPAC, Fw_us_Jones, Fd_us
  - Ftt, Fs_tc, Fw_tc_Massad, Fw_tc_DEPAC, Fw_tc_Jones, Fd_tc
  - Each deposition flux value is in kg ha-1; negative values indicate emission
- Data integrity notes:
  - Quality control included visual checks; removing errors from instrument malfunction, datalogger issues, and power cuts.
  - Regular missing values reflect scheduled power cuts; some gaps stem from sensor replacement.
  - Data are an extension of the 2022 dataset from the same site.

## Quality control and limitations

- Visual QC performed; erroneous data from instruments removed.
- Gaps correspond to:
  - Scheduled power cuts
  - Time needed to replace faulty sensors
- Some missing values are expected due to operational interruptions; users should account for these in analyses.

## Dataset context and usage

- Relation to prior datasets: Extends the 2022 dataset from the Glencorse site; includes a major methodological improvement in the deposition model to reflect NH3 release periods.
- Intended use: Enables researchers and data users to analyze NH3 concentration and deposition dynamics across vertical forest compartments; supports calibration and validation of bi-directional exchange models; facilitates cross-site comparisons and policy-relevant interpretation of ammonia deposition to forest ecosystems.
- Documentation and references: Detailed methodology, analysis, and findings described in Deshpande et al. (2024a, 2024b); key methodological foundations from Chamberlain (1968, 1984), Fowler (1978), Jones et al. (2007), Massad et al. (2010), Nemitz et al. (2000), Sutton et al. (1998), van Zanten et al. (2010), and related works.

## Funding

- UKRI GCRF South Asian Nitrogen Hub (NE/S009019/1) and UKCEH National Capability for UK Challenges Programme NE/Y006208/1.