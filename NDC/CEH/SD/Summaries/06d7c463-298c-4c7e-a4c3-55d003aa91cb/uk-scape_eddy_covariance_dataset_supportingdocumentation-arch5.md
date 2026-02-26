# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2018-2023

## What this dataset is
- Time series dataset of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), with supporting meteorological, soil physics, and vegetation data.
- Collected from ten eddy covariance (EC) flux tower sites across England and Wales (2018–2023).
- Includes site metadata, site-specific flux and ancillary data, vegetation data, and a data dictionary.

## Data holdings and structure
- Site metadata: UK-SCAPE_Site_Metadata.csv (characterises each site; includes start/end dates, land use, soil type, climate, location, and sensor details).
- Flux data: site-specific files named <SITE_ID>_<SOIL_TYPE>_<LAND_USE>_<START_DATE>_<END_DATE>.csv (one per site), containing turbulent fluxes (H, LE, and related variables) measured above the canopy.
- Ancillary data: same site-specific CSV format for meteorological and soil-physics measurements (TA, RH, P, NETRAD, SW_IN/OUT, G, SWC, TS, WATER_TABLE_DEPTH where applicable).
- Vegetation data: UK-SCAPE_Biomass.csv and UK-SCAPE_Canopy_Height_LAI.csv (non-continuous time series; biomass sampling and canopy height/LAI measurements).
- Data dictionary: UK-SCAPE_Data_Dictionary.csv (describes data types, variables, units, sensor depth where applicable).
- Missing data: -9999 used to denote missing records; NA used for non-applicable metadata.

## Site characteristics and study design
- Site types include croplands (peat and mineral soils), managed grasslands, peatlands (lowland fens, bog), and a range of elevations (-2 m to 565 m a.s.l.) with mean annual temps 5–10 °C and rainfall 534–1815 mm/year.
- Sampling regime: continuous automated measurements of flux, meteorology, and soil physics during specified START_DATE to END_DATE windows; vegetation data collected when possible.
- Measurement specifics:
  - Fluxes: open-path EC systems with sonic anemometer and LI-7500 IRGA; 20 Hz sampling; measurement heights vary by site (Zm; mostly fixed, raised to ~5 m for maize in croplands).
  - Ancillaries: TA, RH at 2 m; NETRAD and SW components; soil heat flux at 0.03 m; soil moisture and temperature at various depths; precipitation with tipping bucket or weighing rain gauge; peatlands include water table depth measurements.
  - Vegetation: biomass sampling (desiccated and weighed for carbon export) and manual canopy height/LAI measurements.

## Data processing, quality control, and processing details
- Flux calculation: EddyPro software (v7.0.6) used to derive 30-minute fluxes; includes angle-of-attack corrections, coordinate rotation, spectral corrections, density corrections, and wind diagnostics.
- Quality control (QC): outlier removal (median absolute deviation), stationarity tests, turbulence checks (Mauder & Foken 2006), and multiple friction velocity thresholds; footprint analysis (Kljun et al. 2015) ensuring >80% flux originates within target ecosystem; visual QC applied.
- Gap filling and partitioning:
  - Gaps in EC fluxes and ancillary data filled via Marginal Distribution Sampling (Reichstein et al. 2005).
  - NEE partitioned into GPP and RECO using light-response approaches (Reichstein et al. 2005; Lasslop et al. 2010) with REddyProc (R) for processing.
  - Ancillary data gap-filling cross-checked with co-located COSMOS-UK sites when available.
- Data structure and documentation:
  - Time series provided per site; vegetation data as non-continuous time series; complete coverage between START_DATE and END_DATE where available.
  - Variables and units documented in the Data Dictionary; site-specific metadata may include NA where not applicable.

## Provenance, documentation, and governance
- Data origin: primary UK-SCAPE meteorology, soil physics, and eddy covariance measurements; COSMOS-UK contributions; funded by Natural Environment Research Council and Defra, with additional support for peatland sites and specific plots.
- Documentation and metadata accompany the data to support understanding, reproducibility, and reuse (Site Metadata, Data Dictionary, methodology references, calibration notes).
- Calibration and maintenance:
  - Sensors repaired/replaced as faults detected; gas analysers calibrated per manufacturer specs; calibrations may be performed in-house or by manufacturers; details available on request.

## Access, availability, and updates
- Data are organized in site-specific CSV files with explicit START_DATE and END_DATE windows defined in UK-SCAPE_Site_Metadata.csv.
- Vegetation data are non-continuous time series where available.
- Missing data are clearly flagged (-9999); where metadata do not apply, NA is used.
- Data processing and QC steps are described, enabling informed reuse and potential reprocessing if needed.

## Data governance and reuse considerations for Data Stewards
- Metadata completeness: ensure all fields in UK-SCAPE_Site_Metadata.csv are populated and up-to-date to enable discovery and interoperability.
- Standardization: consistent file naming conventions and alignment with UK-SCAPE_Data_Dictionary.csv aid cross-site data integration.
- Data quality provenance: users should reference the QC methods (stationarity, turbulence tests, footprint analysis) and gap-filling/ partitioning approaches (Marginal Distribution Sampling, REddyProc) when analyzing fluxes.
- Interoperability: data from multiple sites and instruments are harmonized via standardized processing (EddyPro, REddyProc) but note site-specific variations (e.g., measurement heights, soil types, land uses).
- Availability and limitations: be transparent about data windows, gaps, and any site-specific issues (e.g., water table sensor reliability in peatlands) when sharing or aggregating datasets.
- Documentation access: provide access to the Data Dictionary and methodology references to support correct interpretation and reuse.
- Licensing and access controls: confirm and communicate data licensing terms and any access restrictions beyond what is documented, to facilitate reuse and redistribution.

## Endnotes and references
- Processing and QC references include Mauder & Foken (2006), Papale et al. (2006), Reichstein et al. (2005, 2016), Lasslop et al. (2010), Kljun et al. (2015), and related EddyPro documentation; COSMOS-UK and Met Office data integration referenced where applicable.