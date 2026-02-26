# Historic reconstructions of monthly groundwater levels for 54 boreholes in the UK (1981-2015)

## Project context and aims
- Historic Droughts project (2014–2018) aimed to develop cross-disciplinary understanding of past UK droughts to improve future drought management.
- Acknowledges droughts are influenced by hydrometeorological, environmental, regulatory, and socio-economic factors; seeks integrated insights across these perspectives.
- Output includes the Historic Droughts Inventory, a knowledge base of past drought characteristics, impacts, and responses spanning multiple sectors.

## Inventory context
- Eight UK institutions contributed: British Geological Survey (BGS), Centre for Ecology & Hydrology (CEH), Cranfield University, University of Exeter, HR Wallingford, Lancaster University, Met Office, and University of Oxford.
- Historic Droughts Inventory comprises:
  - Hydro-meteorological timelines (rainfall, river flows, groundwater) with consistent drought indicators extending back to the 19th Century.
  - References to past droughts from newspapers, legislation, agricultural media, and oral histories, describing drivers, impacts, and responses.

## Dataset description
- Reconstructed groundwater levels for 54 observation boreholes in the UK, relative to Ordnance Datum (maOD).
- Each site includes 90th and 10th percentile confidence bounds for the reconstructed time series.
- Time period: 1891–2015; most sites located on Principal Aquifers (predominantly Chalk in southern/eastern England).
- Part of the Historic Droughts Inventory alongside the Standardised Groundwater Level Index (SGI) dataset.

## Data sources and inputs
- Groundwater level (GWL) data from the National Groundwater Level Archive (NGLA).
- Precipitation (PPT) data and temperature data used to estimate potential evapotranspiration (PET); sourced from UKCP09-derived data developed for the project.
- Temperature-based PET estimation uses the McGuinness-Bordne method, calibrated for the UK.

## Methodology and uncertainty
- Groundwater levels reconstructed with BGS AquiMod model following established methods.
- Monte Carlo (MC) simulations used to calibrate model parameters; one million parameter sets generated within published aquifer-property ranges or expert judgment.
- Uncertainty quantified with Generalised Likelihood Uncertainty Estimation (GLUE); parameter sets deemed behavioural if Nash–Sutcliffe Efficiency > 0.5.
- For each date, 10th and 90th percentile bounds derived from the distribution of behavioural reconstructions.

## Dataset format and delivery
- Per-site CSV files with headers:
  - Date (YYYY-MM-DD; first day of each month)
  - GWL (groundwater level in metres above Ordnance Datum, maOD)
  - Cl90_GWL (90th percentile of GWL)
  - Cl10_GWL (10th percentile of GWL)
- Filenames follow a structured pattern, e.g. HistoricDroughts_BGSAquiMod_Output_Feb2018_GWL_Rockleyver1.
- A separate metadata file, Metadata_forGWLandSGI_reconstructions.csv, provides site-level metadata such as:
  - Site_name, Easting, Northing
  - BGS_WellMaster_ID, Full_BGS_site_name
  - Aquifer, MORECS_ID, and related location/classification data
- The dataset includes a complete list of the 54 reconstructed sites with associated aquifer information and coordinates.

## Documentation and references
- Acknowledgement of funding: Natural Environment Research Council (NERC) grant NE/L010151/1.
- References support the modelling approach, data sources, and background methods (AquiMod, GLUE, Nash–Sutcliffe metrics, UKCP09 data, etc.).
- The work situates the groundwater reconstructions within the broader Historic Droughts Inventory framework.

## Practical considerations for data stewardship
- Provenance and reproducibility:
  - Source data from NGLA and UKCP09-based inputs; model and calibration steps clearly documented (AquiMod, MC, GLUE).
  - Versioning implied by file naming and project outputs; maintain an explicit version history for updates.
- Metadata completeness:
  - Rich site-level metadata provided; ensure ongoing alignment with inventory standards and cross-referencing to SGI and other drought indicators.
- interoperability and reuse:
  - Standardized data format (monthly GWL with uncertainty bounds) facilitates integration with other hydroclimate datasets and drought indicators.
  - Clear unit conventions (maOD) and time step (monthly) support cross-dataset analyses and meta-analyses.
- Data availability and sharing:
  - Data are shared as CSVs with accompanying metadata within the Historic Droughts Inventory; consider documenting licensing and usage rights for downstream sharing and reuse.
- Maintenance and updates:
  - If updates occur (new observations, revised inputs, or extended time series), follow the established pipeline (re-run AquiMod with updated inputs; regenerate MCGLUE uncertainty) and append versioned files with clear release notes.

## Potential applications and impact
- Enables long-term, cross-site drought analyses and drivers research across hydrological and socio-economic dimensions.
- Supports utility planning and drought management by providing historical context and confidence bounds for groundwater levels prior to major drought events.