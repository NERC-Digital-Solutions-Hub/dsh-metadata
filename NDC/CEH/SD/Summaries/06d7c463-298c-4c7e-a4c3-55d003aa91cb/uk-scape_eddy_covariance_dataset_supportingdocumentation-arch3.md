# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2018-2023

- Purpose and scope
  - Presents the UK-SCAPE Eddy Covariance dataset: time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological, soil physics, and vegetation data.
  - Covers ten eddy covariance (EC) flux tower sites across England and Wales, with measurement periods specified per site (2018–2023 context).
  - Includes site metadata, site-specific flux and ancillary data, vegetation data, and a data dictionary.

- Dataset composition
  - Site metadata file: UK-SCAPE_Site_Metadata.csv.
  - Flux and ancillary data: one file per site (filename format described).
  - Vegetation data: UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv.
  - Data dictionary: UK-SCAPE_Data_Dictionary.csv describing variables and units.

- Study sites and characteristics
  - Ten sites span diverse land uses: croplands (peat and mineral soils), managed grasslands, lowland fens under conservation, and upland blanket bog.
  - Elevation range from 2 m below sea level to 565 m above sea level; climate and soil conditions vary (temperatures 5–10 °C; rainfall 534–1815 mm/yr).
  - Metadata include land use, soil type, location, measurement height, instrumentation, and year-specific crop information where applicable.

- Sampling regime
  - Continuous automated measurements for flux, meteorology, and soil physics during site-specific periods.
  - Vegetation data collected where possible.

- Flux data acquisition
  - Turbulent fluxes (H and LE) measured above canopy with open-path EC systems (sonic anemometer + LI-7500 IRGA).
  - Data recorded at 20 Hz, logged to CR3000 Micrologger, telemetered to secure server.
  - Measurement heights varied by site; cropland sites adjusted Zm during maize growth.
  - Data files named per site and soil/land-use type.

- Ancillary data acquisition
  - Air temperature (TA) and relative humidity (RH) at 2.0 m; barometric pressure from IRGA.
  - Net radiation (NETRAD) and components (SW_IN, SW_OUT, LW_IN, LW_OUT).
  - Soil heat flux (G) at 0.03 m, soil water content (SWC) and soil temperature (TS) at multiple depths.
  - Precipitation (P) from tipping bucket or digital gauge; peatlands include water table depth (WATER_TABLE_DEPTH).
  - Data scanned at 0.1 Hz and aggregated to 15- or 30-minute means (precipitation sums).
  - Data quality notes: water table depth sensors can be susceptible to soil ingress.

- Vegetation data
  - Biomass data (destructive sampling when possible) and canopy height/LAI (non-destructive measurements when possible).
  - Biomass analyses include moisture content and dry biomass; used to estimate carbon export (C_EXPORT) where applicable.
  - Crop yields and agricultural timings obtained where available.

- Instrument calibration and data quality
  - Regular sensor repair/replacement; gas analyzers calibrated per manufacturer specs when feasible.
  - Quality control (QC) of raw data via in-house and manufacturer-recommended procedures.
  - QC procedures include outlier removal, stability tests, tilt/angle corrections, and turbulence and footprint checks.

- Data processing and quality assurance
  - Eddy covariance processing with EddyPro software (Version 7.0.6): 30-minute flux averages; includes standard corrections (angle-of-attack, rotation to local coordinates, spectral attenuation, density corrections, etc.).
  - Footprint assessment using the Flux Footprint Prediction (FFP) tool; fluxes considered representative if >80% originated within target ecosystem.
  - Post-processing QC: statistical outliers (MAD), stationarity and turbulent condition tests, and manual review of plots for obvious errors.

- Gap-filling and flux partitioning
  - Gaps in EC fluxes and ancillary/derived data filled using Marginal Distribution Sampling (Reichstein et al., 2005).
  - Partitioning NEE into GPP and RECO using night- and day-time methods (Reichstein et al., 2005; Lasslop et al., 2010).
  - Gap-filling and partitioning implemented with REddyProc (R) and, where possible, ancillary data gap-filled using COSMOS-UK sites.

- Data structure and accessibility
  - Time series available per site as separate CSV files; complete time series for flux/ancillary data between START_DATE and END_DATE.
  - Vegetation time series (Biomass, Canopy Height/LAI) provided as non-continuous CSVs.
  - Missing data denoted by -9999; site/applicable metadata denoted as NA.
  - Data dictionary describes data types, variables, and units; ensures consistency and interoperability.

- Metadata, governance, and limitations
  - Emphasis on metadata completeness and data governance to support reuse in monitoring frameworks.
  - Acknowledges barriers to data sharing and metadata gaps; dataset provides structured metadata and provenance to aid transparency.
  - Limitations noted: possible data gaps due to instrument issues; water table sensor exposure to soil ingress on peatlands; variable measurement heights and site-specific conditions.

- Funding, acknowledgments, and authorship
  - Data collection supported by NERC and other project-specific funding; contributions from multiple UK centers and landowners.
  - Acknowledges landowners and site managers for access and permissions.

- Relevance for monitoring frameworks
  - Demonstrates end-to-end data lifecycle: site selection, standardized instrumentation, QC, gap-filling, and flux partitioning.
  - Provides a replicable workflow and data products suitable for evaluating environmental policies and informing future decisions.
  - Emphasizes the importance of metadata, data quality, openness, and governance to enable policy-relevant analyses.