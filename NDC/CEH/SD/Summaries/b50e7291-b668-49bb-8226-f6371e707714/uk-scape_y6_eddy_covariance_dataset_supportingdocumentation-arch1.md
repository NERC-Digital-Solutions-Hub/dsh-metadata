# Meteorology, soil physics, and eddy covariance measurements of carbon dioxide, energy, and water exchange from a distributed network of sites across England and Wales, 2023 to 2024

- A dataset (UK-SCAPE_Y6_Flux_Dataset) containing time series of land surface–atmosphere exchanges of sensible heat (H) and latent heat (LE), plus supporting meteorological and soil physics data from six eddy covariance (EC) flux tower sites across England and Wales.
- Site metadata (UK-SCAPE_Y6_Site_Metadata.csv) summarises site characteristics and supports data interpretation.

## Study sites

- Six flux monitoring sites with varied land use:
  - Three croplands (two on peat, one on mineral soils)
  - One grassland on peat
  - One lowland fen under conservation management
  - One relatively intact upland raised bog
- Elevation range: from -2 m to 565 m above sea level.
- Mean annual temperature: 5–10 °C; Mean annual precipitation: 534–1815 mm (HadUK-Grid derived, Met Office 2018).
- Site-level metadata described in UK-SCAPE_Y6_Site_Metadata.csv (e.g., location, land use, soil type, measurement height, instruments).

## Sampling regime

- Automated flux, meteorological, and soil observations aligned to START_DATE and END_DATE in the site metadata.
- Data logged as 30-minute means (with precipitation sums); high-frequency data at 20 Hz for EC measurements.

## Flux data acquisition

- Open-path EC systems measuring turbulent fluxes above the canopy.
- Instruments: sonic anemometer plus LI-7500 IRGA (CO2 and H2O).
- Data rates and processing: 20 Hz observations; data logged to a CR3000 micrologger and telemetered to a secure server.
- Measurement height (Zm) varied by site; typically fixed, with adjustments during certain crop phases (e.g., maize).
- Sensor geometry: specific horizontal/vertical offsets between sonic and IRGA sensors described.

## Ancillary data acquisition

- Air temperature (TA) and relative humidity (RH) at 2.0 m; barometric pressure (PA) from IRGA internal sensors.
- Net radiation (NETRAD) and its components (SW_IN, SW_OUT, LW_IN, LW_OUT).
- Soil heat flux (G) at 0.03 m depth; soil moisture (VWC) and temperature (TS) at various depths.
- Precipitation (P) via tipping-bucket rain gauge.
- Peatland water table depth (WATER_TABLE_DEPTH) where possible.
- Observations scanned at 0.1 Hz and logged as 30-minute means.

## Vegetation data

- Manual measurements of canopy height, LAI (LAI-2000/LAI-2200C), and biomass.
- Destructive biomass sampling processed to estimate carbon export and, where applicable, carbon allocation to leaves, stems, roots, and grains.

## Flux data processing

- Processing with EddyPro software (Version 7.0.6) to derive fluxes from raw EC data.
- Fluxes computed as 30-minute block averages.
- QC and corrections applied: quality control of 20 Hz data, angle-of-attack correction, 2D rotation for terrain, high/low-frequency cospectral attenuation corrections, density corrections, and wind speed/direction at measurement height.

## Quality control

- Sensor repairs/replacements as needed; calibrations performed per manufacturer specs.
- QC procedures:
  - Remove statistical outliers (MAD method; Papale et al. 2006).
  - Test stationarity and turbulent conditions (Mauder & Foken 2006).
  - Filter periods of low turbulence using U* thresholds (Papale et al. 2006).
  - Assess flux footprint with the Kljun et al. (FFP) model; require >80% target-ecosystem representation.
  - Visual checks of all flux and ancillary data with manual removal of clearly erroneous values.

## Data gap-filling and flux partitioning

- Gaps in EC (NEE, LE, H) and ancillary data filled using Marginal Distribution Sampling (Reichstein et al. 2005).
- Partitioning of Net Ecosystem Exchange (NEE) into Gross Primary Production (GPP) and ecosystem respiration (Reco) using day/night methods (Reichstein et al. 2005; Lasslop et al. 2010).
- Gap-filling/partitioning performed with REddyProc (R) (Reichstein et al. 2016).
- Where possible, ancillary data gap-filled using collocated COSMOS-UK data (Cooper et al. 2021).

## Details of data structure

- Time series data provided as separate CSV files for each of the six sites.
- Data include complete time series from START_DATE to END_DATE; missing records denoted by -9999.
- TIMESTAMP_START/END may appear in scientific notation in some software; vegetation data provided as non-continuous time series where available.

## Nature and units of recorded values

- Described in UK-SCAPE_Data_Dictionary.csv; contains units and definitions for fluxes, micrometeorological, and soil-physics variables.

## Acknowledgments

- Thanks to landowners and partner organisations (e.g., Natural Resources Wales, RSPB, Natural England, Great Fen Project) for site access.
- Data collection funded by NERC UK-SCAPE programme (NE/R016429/1); capital funding acknowledged for Grange Farm flux tower.

## References

- Key methodological references for QC, processing, footprint analysis, and gap-filling (e.g., Reichstein et al. 2005; Lasslop et al. 2010; Mauder & Foken 2006; Papale et al. 2006; Moncrieff et al. 1997/2004; Vickers & Mahrt 1997; Schotanus et al. 1983; Webb et al. 1980; Wilczak et al. 2001; Cooper et al. 2021; Met Office HadUK-Grid data).