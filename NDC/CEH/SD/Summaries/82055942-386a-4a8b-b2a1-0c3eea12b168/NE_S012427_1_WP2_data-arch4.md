# Flood risk assessment of the Luanhe river basin under different development strategies and climate scenarios

- Overview
  - A dataset describing inputs and results for flood risk assessment in the Luanhe river basin under various development strategies and climate scenarios up to 2030.
  - Uses HiPIMS hydrodynamic modelling, validated with a 2012 flood event, and linked to population exposure via GPWv4.
  - Data are largely open and produced by the authors, with open licensing (Open Government Licence).

- Data inputs and generation methods
  - Climate uplifts to 2030 derived from NASA NEX-GDDP to represent future 100-year design rainfall.
  - Validation of the flood model (HiPIMS) using a 2012 historical flood event with remote sensing observations.
  - Flood inundation predictions to 2030 under different development strategies and climate scenarios, using uplifts and future land use data as inputs.
  - Population exposure assessment by overlaying inundation results with the Gridded Population of the World (GPWv4) dataset.

- Data products and formats
  - Climate uplifts: CSV files (rcp45.csv, rcp85.csv); first column is city, second column uplift value.
  - Validation and remote sensing: TIFF files (Validation.tif, RemoteSensing_validation.tif).
  - Inundation maps: TIFF files detailing flood simulations under various scenarios (see Tab. 2 in the source).
  - Population data: GPWv4-derived population density (persons/km^2), TIFF/grid format.
  - Land use and scenario configurations include Baseline and multiple 2030 scenarios (Trend, Expansion, Sustainability, Conservation) under RCP4.5 and RCP8.5, with reservoir components denoted by P and S.
  - Licensing: Open Government Licence for the data components.

- Data structure and documentation
  - Data described across two tabs (Tab. 1 and Tab. 2) detailing datasets and formats.
  - Datasets include: flood model validation data, climate change uplifts, inundation maps, and population data.
  - Contributing authors: Loughborough University; data are described as well-documented and open.

- Quality, provenance, and reuse
  - HiPIMS model has established use in flood risk assessments (supported by prior studies).
  - The dataset is documented and has been submitted to peer-reviewed journals, with robust estimate support.
  - NEX-GDDP and GPWv4 are widely used, open datasets.
  - Reuse considerations include model assumptions, scenario choices (land use, reservoirs, RCPs), and the need to align temporal and spatial resolution with user goals.

- Relevance for data strategy and governance
  - Demonstrates end-to-end data pipeline: climate projections -> hydrodynamic flood modelling -> exposure mapping -> risk assessment.
  - Supports cross-sector planning in the Beijing-Tianjin-Hebei region by providing harmonised inputs and open data for risk mapping.
  - Highlights needs around data standardisation, metadata quality, and ongoing updates as scenarios and datasets evolve.

- Limitations and considerations for implementation
  - Results depend on model assumptions and chosen scenarios; require careful interpretation for policy decisions.
  - Data granularity and alignment across climate, land use, hydrodynamics, and population layers to ensure coherent risk maps.
  - Potential data gaps or uncertainties in validation data or future land-use projections that may affect risk estimates.