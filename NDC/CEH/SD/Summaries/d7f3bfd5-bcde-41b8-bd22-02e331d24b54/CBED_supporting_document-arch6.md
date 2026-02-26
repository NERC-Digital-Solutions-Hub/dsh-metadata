# Concentration Based Estimated Deposition (CBED) methodology

- Purpose: Generate 5x5 km resolution maps of wet and dry deposition for sulphur, oxidised and reduced nitrogen, and base cations in the UK, using measured air/gas/ PM concentrations and precipitation data.
- Data sources: Measurements from the UK Eutrophying and Acidifying Pollutants (UKEAP) network; additional modelling inputs for ammonia and other components.

## How the data are produced

- Site measurements are interpolated to create UK concentration maps.
- Wet deposition: combine ion concentrations in precipitation with an annual precipitation map to estimate wet deposition; includes occult deposition (direct cloud droplet deposition to vegetation).
- Dry deposition: combine gas/PM concentration maps with spatially distributed habitat-specific deposition velocities to estimate deposition to five land cover categories (forest, moorland, grassland, arable, urban); deposition to each 5x5 km grid square is weighted by land cover proportions.
- Dry deposition components include:
  - Gases: SO2, HNO3, NO2, NH3
  - Particulate matter: sulphate, nitrate, ammonium, calcium, magnesium
- For critical load exceedance, moorland deposition is applied to non-woodland habitats and forest deposition to woodland habitats.

## Temporal and ecosystem outputs

- Calculations are annual but presented as rolling 3-year means to smooth inter-annual variability.
- Outputs are ecosystem-specific with two sets of values per grid square:
  - Moorland deposition
  - Forest/woodland deposition
  - Grid-average deposition
- Gridded mapping: 5x5 km UK grid; data provided as 3-year means.

## Data structure and fields

- Three dataset types (3-year mean):
  - Moorland: deposition fields (nox_m, nhx_m, nms_m, nm_ca_m) plus easting/northing
  - Forest/woodland: deposition fields (nox_f, nhx_f, nms_f, nm_ca_mg_f) plus easting/northing
  - Grid average: deposition fields (nox_ga, nhx_ga, nms_ga, nm_ca_mg_ga) plus easting/northing
- Each record includes:
  - easting and northing: centre coordinates of the 5x5 km square (OS Great Britain grid)
  - deposition values expressed in keq ha-1 year-1 for oxidised nitrogen (nox), reduced nitrogen (nhx), non-marine sulphur (nms), and non-marine base cations (nm_ca_mg)

## Units and data conversions

- All values are in kilo-equivalents per hectare per year (keq ha-1 year-1).
- Conversions to kilograms per hectare per year:
  - Oxidised/reduced nitrogen: multiply keq ha-1 year-1 by 14 to obtain kg N ha-1 year-1
  - Sulphur deposition: multiply keq ha-1 year-1 by 16 to obtain kg S ha-1 year-1
  - Base cations (Ca+Mg): multiply keq ha-1 year-1 by 20 to obtain kg Ca ha-1 year-1

## Quality control and validation

- Methods follow QA procedures aligned with Government analytical model QA standards.
- CBED data and calculations have undergone extensive peer review and participated in Defra model inter-comparisons.
- Version control, documentation, and central storage of code are maintained.
- Mass balance checks are routinely performed and results are compared with previous years.
- Methods and outputs have been widely published in peer-reviewed literature.

## Data usage and accessibility

- Purpose-built for assessing deposition and ecosystem impacts (e.g., critical loads exceedance) and for informing policy and environmental management.
- Data structure supports easy integration into spatial analyses and dashboards for end users.
- Primary data sources and supporting information are accessible via the UK EAP/UK-air portals:
  - CEH UKEAP deposition data pages
  - Defra/UK-air network information and model documentation

## Supporting details and references

- Key references underpinning the methodology include:
  - Interpolation and modelling approaches for oxidised nitrogen, ammonia, and related deposition processes
  - FRAME atmospheric transport model and PCM model components
  - Peer-reviewed studies of long-term ion concentration and deposition trends
  - Documentation on regional transport and deposition modelling for the UK

- Notes on data interpretation:
  - Deposition values to forest vs moorland depend on habitat-specific deposition velocities
  - The separation of anthropogenic and marine sea-salt components relies on ion ratios relative to sodium in sea water
  - Inter-annual variability is substantial due to weather patterns; rolling 3-year means help stabilize estimates