# Supporting information for: Eddy Covariance measurements of carbon dioxide, energy and water flux at an intensively cultivated lowland deep peat soil, East Anglia, UK, 2012 to 2020.

## Overview of dataset
- Time series of land surface–atmosphere exchanges: net ecosystem CO2 exchange (NEE), sensible heat (H), latent heat (LE), and momentum (τ) measured above an intensively cultivated lowland deep peat field (site EF-DA) from 2012-06-22 to 2020-01-01.
- Ancillary observations: meteorology and soil-physics data, plus variables describing atmospheric turbulence.
- Data processing outputs include gap-filled and partitioned fluxes (GEP and TER) and associated uncertainties.
- Data are organized as thirty-minute means, with raw 20 Hz observations used for processing; footprint-based quality control ensures fluxes originate from the target ecosystem (>70% footprint from the site).
- File format: time-series data in CSV with -9999 marker for missing values; includes both unfilled (raw) and filled (gap-filled) variables/columns.

## Study site and context
- Location: EF-DA flux site in the East Anglian Fens, UK (52°31'N, 0°29'E; 0 m a.s.l.).
- Environment: large contiguous area of lowland peatland; drained and converted for agriculture after WWII; peat is deep with high bulk density and low C/N ratio due to drainage and fertiliser use.
- Climate: temperate maritime (mean 10.4°C; ~564 mm annual rainfall, 1981–2010 baseline).
- Land use: trapezoidal arable fields with hedgerows and ditch systems; diverse crops over the study period (lettuce, leek, celery, sugar beet, potatoes).
- Collaboration and stewardship: long-term site support from universities, farmers, and multiple funding sources; permissions from farm owners.

## Sampling regime and instruments
- Flux data: automated EC flux system at 1.5 m height; open-path CO2/H2O analyzer (LI-7500) and CSAT3 sonic anemometer oriented to SW wind.
- Ancillary meteorology and soils: radiometers (NRLite2, CNR4) for net radiation; PAR sensor; air temperature and RH; precipitation; two soil-instrument arrays (soil heat flux, soil temperature, volumetric water content) 2 m apart.
- Data logging: 30-minute means (and sums for precipitation) recorded by CR3000 Micrologger; fluxes sampled at 20 Hz.

## Data processing and quality control
- Processing: EddyPRO v6.1 used for QC, coordinate rotation, co-spectral corrections, density corrections, and flux calculations; outputs include derived fluxes, u*, TKE, Obukhov length, stability parameter, and flux footprints.
- Quality control (QC):  
  - Outliers removed using median absolute deviation;  
  - Non-stationary turbulence periods removed;  
  - Flux ranges applied: H (-200 to 400) W m^-2, LE (-200 to 600) W m^-2, NEE (-40 to 40) μmol CO2 m^-2 s^-1;  
  - NEE excluded at night when fluxes are negative;  
  - Fluxes retained only if >70% of footprint originates from the target ecosystem (ART footprint tool).
- Gap-filling and partitioning:  
  - Gaps filled with Marginal Distribution Sampling (Reichstein et al. 2005);  
  - NEE partitioned into GEP and TER using Reichstein et al. (2005) framework driven by air temperature;  
  - Gap-filling and partitioning performed with REddyProc (R package, Reichstein et al. 2016).

## Data structure and content
- Primary data: CSV time-series with thirty-minute records; columns include NEE, NEE_unc, LE, LE_unc, H, H_unc, Tau, Tau_unc, and related storage and uncertainty terms.
- Additional fields: CO2 storage term, storage terms for LE and H, pressure (Pa), air temperature (Ta), relative humidity (RH), vapor pressure deficit (VPD), net radiation (Rnet), radiation components (Rg, etc.), soil heat flux (G) at multiple locations, soil temperature (Tsoil), soil moisture (VWC), precipitation, wind speed/direction, footprint fraction, updated footprint from Neftel et al. (2008), friction velocity (Ustar), Turbulent Kinetic Energy (TKE), Obukhov length (L), stability parameter (z/L), and gap-filled flux values and their standard deviations (NEE_filled, LE_filled, H_filled, with corresponding_sd).
- Two-location structure: some variables provided for location 1 and location 2 in the same dataset (as indicated in the variable naming and table descriptions).
- Missing data: denoted by -9999; includes gaps due to system downtime or QC exclusions.
- Documentation: extensive variable descriptions and units aligned with LI-COR conventions and REddyProc outputs; references provided for methods and processing tools.

## Data quality, limitations, and governance
- Strengths: long-term, well-documented, standardized processing pipeline; clear QC criteria and footprint-based data filtering; open methodology for gap-filling and flux partitioning; comprehensive ancillary data enabling context for fluxes.
- Limitations and challenges: intermittent radiometer downtime and calibration periods; occasional data gaps requiring gap-filling; some periods with complex non-ideal conditions requiring careful interpretation; dual-location data structure adds complexity to metadata and usage.
- Governance and reuse considerations: appropriate acknowledgment of data sources and processing tools; metadata includes site description, instrumentation details, temporal coverage, and processing steps; data suitable for community use with proper citation to original publications and REddyProc/EddyPRO references.

## Availability, metadata, and references
- Acknowledgements: site established and supported by NERC and Defra projects; gratitude extended to farm owners and co-operating staff.
- References: methodological and processing references include Reichstein et al. (2005, 2016), Foken et al. (2004), Moncrieff et al. (1997, 2004), Neftel et al. (2008), Papale et al. (2006), and related instrument and data-processing literature.
- Related materials: site and crop details, data availability statements, and research outputs are linked to the EF-DA flux dataset and associated publications (e.g., Cumming 2018; Evans et al. 2017) for broader context and reuse.