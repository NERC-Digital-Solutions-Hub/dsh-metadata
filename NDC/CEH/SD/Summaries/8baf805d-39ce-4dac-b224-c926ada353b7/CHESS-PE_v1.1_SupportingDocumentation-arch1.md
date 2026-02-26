# Climate hydrology and ecology research support system potential evapotranspiration dataset (1961-2015) [CHESS-PE]

- Purpose and scope
  - Provides two daily estimates of potential evapotranspiration (PET) on a 1 km resolution grid over Great Britain for 1961–2015.
  - Derived from CHESS-met meteorological variables and CEH-GEAR precipitation; time and spatial extent match for both variables.

- The two PET variables
  - PET: Penman-Monteith potential evapotranspiration for a well-watered grass surface (mm/day).
  - PETI: PET with interception correction (mm/day). On days with rainfall, accounts for canopy interception that reduces transpiration; includes an interception store that dries over the day and is added back to evaporation.

- Input data used
  - PET: air temperature (Ta), specific humidity (qa), downward longwave and shortwave radiation (Ld, Sd), surface air pressure (p*), from CHESS-met.
  - PETI: all PET inputs plus CEH-GEAR precipitation (scaled to appropriate units).

- Calculation and modelling details
  - PET (EP) is computed using the Penman-Monteith equation, assuming grass with a constant stomatal resistance of 70 s m−1 (reference FAO standard; Allen et al. 1998).
  - PETI uses the same Penman-Monteith calculation for E_P and adds interception dynamics:
    - On wet days, calculate interception E_I by using zero stomatal resistance.
    - PETI = E_P with interception linked to an exponential dry-down of the interception store (parameters S0 and Stot govern the initial and total interception capacity).
  - The calculation framework follows Robinson et al. (in review) with full methodological details available there.

- Data format and access
  - Files are netCDF, CF-compliant, following CEH gridded dataset conventions.
  - Data are stored as monthly files; there is one file per variable (PET and PETI).
  - The dataset supports clear provenance and reproducibility, with references and underlying data sources documented.

- Key characteristics and caveats for users
  - Resolution and scope: 1 km grid covering Great Britain; values represent atmospheric evaporative demand (not actual soil evaporation without water limitation).
  - Assumptions:
    - PET assumes a well-watered grass surface.
    - PETI incorporates canopy interception with a fixed interception process and stores; real-world interception can vary with vegetation and rainfall characteristics.
  - Sources and dependencies:
    - PET inputs depend on CHESS-met meteorology; precipitation inputs rely on CEH-GEAR data.
  - Reproducibility and traceability:
    - Full calculation details and related methodology are published (Robinson et al., in review); data and metadata are intended to be discoverable via data portals.

- References
  - FAO. Crop evapotranspiration guidelines (Allen et al., 1998).
  - CEH-GEAR data and methodology (Keller et al., 2015; Tanguy et al., 2016).
  - Penman-Monteith foundational work (Monteith, 1965).
  - CHESS-met meteorology dataset (Robinson et al., 2015).
  - Related trend and methodology papers (Robinson et al., 2015; Robinson et al., 2016; Robinson et al., in review).