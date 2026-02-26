# Carbon dioxide and methane fluxes and associated environmental observations from paired burned/unburned peatland undergoing restoration

- Purpose and scope
  - Time-series dataset of land surface–atmosphere exchanges: Net Ecosystem CO2 Exchange (NEE), methane (CH4), sensible heat (H), latent heat (LE), plus meteorological observations.
  - Focused on two blanket bog sites within Forsinard RSPB Reserve, Flow Country, Scotland, as part of peatland restoration after forestry clearance and following a wildfire in May 2019.
  - Aims to evaluate environmental health measures related to peatland restoration and wildfire impacts to inform policy and decision-making.

- Experimental design and site details
  - Two sites: UK-DKF (burned area from wildfire) and UK-DKE-RESTORED (proximate area protected from fire for instrumentation; restored area close to DKF).
  - Time period: 25/09/2019 – 20/05/2021 (data capture until 16/10/2020 affected by power/sonic anemometer issues; post-16/10/2020 data have significant gaps).
  - Context: Former forestry block with restoration steps; footprint largely in SW wind direction; canopy height around 0.25 m at RESTORED, increasing in FIRE area after burn.

- Measurements and instrumentation
  - Fluxes: 30-minute density- and turbulence-corrected fluxes for CO2 (NEE), CH4, LE, and H derived from eddy covariance (EC) systems.
  - CO2/water measurements: Enclosed-path Li-COR LI-7200 for H2O/CO2; open-path Li-7700 for CH4.
  - Meteorology and micrometeorology: 15-minute data (processed to 30-minute) for air temperature (Ta), relative humidity (RH), wind speed/direction, net radiation (Rn), incoming shortwave radiation (Rg), PAR (PPFD), soil parameters, precipitation, and water table depth.
  - Equipment specifics: Windmaster Pro sonic anemometer, Li-Cor analysers, Vaisala HMP155 for Ta/RH, soil sensors (G, Ts, SWC), 0.05 m depth soil temperature sensors, soil heat flux plates, water table sensor, and data loggers: 20 Hz sampling for EC and micrometeorology, aggregated to 30-minute means.
  - Spatial context: ~300 m fetch in SW direction; some microform variability (three microforms) in soil and vegetation structure.

- Data processing and quality control
  - Processing: Fluxes calculated with EddyPRO v7.0.6; standard 30-minute aggregation; corrections for coordinate rotation, density effects, cospectral attenuation, and humidity effects; CO2 storage considered negligible; NEE assumed equal to turbulent CO2 flux.
  - Calibration and maintenance: Gas analysers calibrated per manufacturer; no on-site span/zero checks during data capture due to remoteness; June 2021 zero/span check indicated no significant drift.
  - Quality control: Data are submitted without formal screening due to patchy capture; quality flags included to aid future QA/QC, with a defined flag schema (e.g., raw, reviewed, calibrated, removed faulty data, interpolations, modelled data).
  - Data provenance and references: Methodologies align with Mauder et al. (2013), Moncrieff et al. (1997, 2004), Schotanus et al. (1983), Webb et al. (1980), among others.

- Data structure and content
  - Single CSV file containing: DateTime (UTC) and a comprehensive set of fluxes, meteorology, soil and water metrics, and multiple quality flags.
  - Key data columns include: SWC microforms, Ts (soil temperature), Ta, RH, PPFD, Rn, Rg, P_rain, WTD, G (soil heat flux), H (sensible heat), LE (latent heat), co2_flux (NEE), h2o_flux, ch4_flux, co2_mixing_ratio, h2o_mixing_ratio, ch4_mixing_ratio, u*, L, wind_speed, wind_dir, (z-d)/L, and corresponding FLAG fields for each variable.
  - Flags follow a standardized coding scheme (e.g., 000 raw, 001 primary data, 002 calibrated, 003 removed, 01# interpolated gaps, 02# filled, etc.; maximum interpolation gap 1 hour).

- Data limitations and gaps
  - Patchy data capture led to incomplete time series; no post hoc screening applied beyond quality flags.
  - Instrumental issues: sonic anemometer and power supply problems; data gaps intensified by weather, management constraints, and COVID-19 travel restrictions; post-16/10/2020 data show significant gaps.
  - Calibration limitations: no on-site, real-time span/zero checks during the data period, which may affect long-term consistency (though June 2021 calibration indicated no significant drift).

- Relevance for monitoring frameworks and policy
  - Demonstrates an integrated, end-to-end approach to monitoring peatland responses to wildfire and restoration, linking carbon and methane fluxes with detailed micrometeorology and soil dynamics.
  - Provides both raw and processed flux data, enabling transparency, reproducibility, and independent re-processing within monitoring frameworks.
  - The metadata-rich dataset (including QA/QC flags, instrument specifics, and processing steps) supports governance around data quality, provenance, and data-sharing practices.
  - Useful for evaluating restoration efficacy, informing climate and land-management policies, and guiding future monitoring design to mitigate data gaps and improve data accessibility.

- References and methodological backbone
  - Core flux processing and quality-control references: Mauder et al. (2013); Vickers & Mahrt (1997); Wilczak et al. (2001); Nakai et al. (2006); Moncrieff et al. (1997, 2004); Schotanus et al. (1983); Webb et al. (1980).