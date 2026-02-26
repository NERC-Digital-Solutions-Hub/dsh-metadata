# Ozone flux POD 1 IAM dataset for grasslands, 2018 – UK and USA

- A dataset describing daily ozone flux (POD 1 IAM) for grassland vegetation, derived from the EMEP-WRF modelling framework for the year 2018, focusing on the UK and USA.
- Purpose: enabling assessment of ozone stomatal uptake and potential impacts on semi-natural vegetation, plant productivity, and related ecological/auditory outcomes; supports risk assessment and policy-relevant analyses via CLRTAP methodologies.

## Data and modelling lineage

- Modelling framework:
  - EMEP-WRF global model, version 4.45 (based on EMEP MSC-W), using WRF version 4.2.2 to generate hourly 3D meteorology.
  - Forcing data: GFS-FNL reanalysis (initialisation and six-hour nudging).
  - Emissions: IIASA ECLIPSE v6a GAINS (2015) emissions data.
  - Ozone flux calculation: DO 3 SE stomatal-flux model embedded within EMEP, parameterised for vegetation types (e.g., crops, trees, grasslands).
- Output metric:
  - POD1 IAM: accumulated daily ozone flux above a threshold, for the growing season, expressed as mmol m^-2.
  - For this dataset, POD1 IAM values are summed over the 90-day grassland growing season (mid-April to mid-July) in 2018.
- Applications:
  - Enables estimation of impacts on crop yield, tree biomass, and flower number via dose–response relationships (CLRTAP Mapping Manual, 2017).
  - Provides inputs for risk assessments using established ozone flux–response frameworks (e.g., Figure 3 in the CLRTAP manual).

## Data scope and structure

- Spatial domain: global model domain, 1° x 1° grid resolution.
- Temporal scope: the year 2018; 90-day grassland growing season window selected per grid cell (April 1 to September 30 as a guiding frame, with the actual 90-day window chosen to optimize flux estimates locally).
- Geographic coverage in the dataset: USA and UK grid cells (NAME attribute).
- Data format and structure:
  - Shapefile with gridded data (1° x 1° resolution).
  - Attributes (5 fields):
    - FID: Unique grid cell identifier.
    - Lon: Longitude of grid cell center (decimal degrees).
    - Lat: Latitude of grid cell center (decimal degrees).
    - NAME: Country (USA or UK).
    - POD1: Accumulated POD1 IAM for the grassland growing season in 2018 (mmol m^-2) per grid cell.
- Coordinate system and units:
  - Geographic Coordinate System: WGS 1984.
  - POD1 IAM units: mmol m^-2.

## Data quality and validation

- Quality control: Model output undergoes quality assurance/control prior to analysis; validation against Global Atmosphere Watch (GAW) observational data to assess seasonal ozone patterns and regional variations.
- Validation highlights:
  - Modelled vs. observed daily maximum ozone (ppb) across six GAW sites shown to capture spatial and temporal ozone variability, including peak episodes.
  - Proxy validation for stomatal uptake demonstrated by a strong correlation (r^2 = 0.63) between POD3 IAM (growing-season ozone flux proxy) and a vegetation/evapotranspiration-based proxy (AET/PET) for grid cells with substantial wheat cover, indicating the model reasonably estimates stomatal uptake.

## Data use and interpretation guidance

- Background and context:
  - Ozone flux data underpin calculations of impacts on semi-natural vegetation (grasslands) using response functions from CLRTAP manuals.
  - Example application: dose–response functions for grassland vegetation link POD1 IAM values to reductions in flower number and biomass.
- Parameterisation notes:
  - DO3 SE model inputs include hourly ozone concentrations, temperature, VPD, irradiance, and soil moisture; canopy-level parameters (e.g., gmax) are vegetation-specific.
  - The time window for accumulation should be selected to maximize flux relevance for the local growing-season context, typically within 1 April to 30 September.
- Data provenance and usage references:
  - CLRTAP (2017) Mapping Manual; Emberson et al. (2000) stomatal flux modelling; Mills et al. (2018) model validation; Hayes et al. (2021) ozone-flux-based grassland impact relationships; Simpson et al. (2012) EMEP MSC-W description; Vieno et al. (2016) EMEP-WRF context.

## Practical considerations for Data Stewards (governance and stewardship)

- Data completeness and interoperability:
  - Dataset covers 2018 with a 1° grid; users may require additional years or different vegetation types, necessitating clear metadata around season definitions and parameter choices.
- Metadata and provenance:
  - Document model versions, forcing data sources, emission datasets, parameterisations (DO3 SE), and season-definition rules to ensure reproducibility.
- Data formats and accessibility:
  - Provide machine-readable shapefile with accompanying metadata; consider linking to the original model documentation and background manuals (CLRTAP, EMPEP/WFF sources) for users needing deeper methodological details.
- Update and maintenance:
  - If updates or reprocessing occur (e.g., new years, different vegetation covers), implement versioning, changelogs, and consistent metadata schemas.
- User needs alignment:
  - Ensure documentation clarifies the exact seasonal window used per grid cell, the handling of atypical climates, and any regional defaults when local information dictates a different growing-season length.

## References and background

- CLRTAP (2017) Mapping critical levels for vegetation. CLRTAP Modelling and Mapping Manual.
- Emberson, L.D., et al. (2000) Modelling stomatal ozone flux across Europe.
- Hayes, F., et al. (2021) Ozone critical levels for (semi-) natural vegetation dominated by perennial grassland species.
- Mills, G., et al. (2018) Ozone pollution and wheat production implications.
- Simpson, D., et al. (2012) The EMEP MSC-W chemical transport model – technical description.
- Vieno, M., et al. (2016) The EMEP-WRF framework and its applications.