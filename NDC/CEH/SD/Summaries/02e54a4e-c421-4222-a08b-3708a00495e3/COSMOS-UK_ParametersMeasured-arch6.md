# COSMOS-UK (2018). Daily and sub-daily hydrometeorological and soil data (2013-2016) [COSMOS-UK]. NERC Environmental Information Data Centre.

- Introduction and scope
  - Describes data stored in the Environmental Information Data Centre (EIDC) from the COSMOS-UK network for 2013-2016.
  - Data are organized into four CSV files covering hydrometeorological/soil measurements, potential evapotranspiration, and soil volumetric water content (VWC) at daily and hourly resolutions.
  - Applicable to sites installed before end of 2016; further network details available in COSMOS-UK User Guide.

- Data files and content
  - Hydrometeorological and soil (COSMOS-UK_Hydrometeorological&Soil.csv)
    - 42 sites, 30-minute resolution, Oct 2013–Dec 2016.
    - Variables include: incoming/outgoing longwave and shortwave radiation, net radiation, precipitation, atmospheric pressure, air temperature, wind speed and direction, absolute and relative humidity, snow depth (site-dependent), wind components (X, Y, Z at select sites), soil temperature at multiple depths, volumetric water content (VWC) at sensors, soil heat flux, and derived soil temperature/heat flux values.
    - Some site-specific exceptions: snow depth measured only at a subset; wind components not measured at certain sites.
  - Potential evapotranspiration (COSMOS-UK_PotentialEvapotranspiration.csv)
    - Derived daily PET from the 30-minute hydrometeorological/soil data (Oct 2013–Dec 2016) using the Penman-Monteith method (FAO 56).
    - Variables: PET (mm) with daily totals.
  - Volumetric Water Content Daily (COSMOS-UK_VolumetricWaterContent_Daily.csv)
    - Derived at 42 sites, daily resolution for Oct 2013–Dec 2016.
    - Variables: Volumetric water content (%) and D86 depth (75 m distance from COSMOS sensor) with daily averages.
    - Derived from hydrometeorological data and Cosmic-ray sensing data (and background neutron counts from Jungfraujoch station).
  - Volumetric Water Content Hourly (COSMOS-UK_VolumetricWaterContent_Hourly.csv)
    - Derived at 42 sites, hourly resolution for Oct 2013–Dec 2016.
    - Variables: Corrected COSMOS neutron counts, Volumetric water content (%), D86 at 75 m depth.
    - Uses hourly cosmic-ray data; daily values also available via the Daily VWC file.
  
- How data were measured and processed
  - On-site measurements collected by various instruments; data logged locally and telemetered hourly to CEH Wallingford.
  - Quality control tests applied to all data; instrumentation details and which variables are measured by each instrument are described in the COSMOS-UK User Guide.
  - Derived data processes:
    - PET derived from the 30-minute dataset after a day’s data are collected (Penman-Monteith, FAO56).
    - VWC Daily derived from corrected cosmic-ray counts with the Evans et al. (2016) methodology; D86 (depth) values derived per Köhli et al. (2015).
    - VWC Hourly derived from hourly cosmic-ray data with corresponding corrections.

- Site coverage and notes
  - 42 calibrated sites (list includes Alice Holt, Easter Bush, Chimney Meadows, Plynlimon, Rothamsted, Wytham Woods, etc.).
  - Site metadata provided (SITE_ID, coordinates, start date, calibration status, altitude).
  - Snow depth measurement limited to a subset of sites; wind component measurements (X, Y, Z) not available at all sites.
  
- Usage and accessibility
  - Data are stored in the Environmental Information Data Centre (EIDC) and are suitable for cross-site analysis, trend assessment, and data product creation for exploration and self-service analysis.
  - Derived products (PET and VWC) enable water balance, soil moisture, and hydrological studies across multiple sites without needing to perform complex on-site data fusion.
  - For instrumentation details, data processing steps, and site-specific notes, refer to the COSMOS-UK User Guide.

- References and further information
  - Evans et al. (2016): COSMOS-UK soil moisture derived from cosmic-ray neutron sensing.
  - Köhli et al. (2015): D86 depth correction methodology.
  - FAO (1998): FAO-56 guidelines for crop evapotranspiration.
  - COSMOS-UK User Guide (2018) for full instrumentation details and data handling.