# Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models

## Objective and scope
- Assess yield potential and soil carbon impacts of large-scale Miscanthus bioenergy using three models: MiscanFor, JULES, and IMAGE.
- Use a single climate/ socio-economic pathway: SSP2-RCP2.6.
- Explore early low-cost bioenergy scale-up and later bioenergy with carbon capture and storage (BECCS) in 21st century mitigation scenarios.
- Focus outputs on bioenergy yield and soil carbon changes as key determinants of life-cycle carbon balance.

## Models and driving data
- Models involved:
  - MiscanFor (Miscanthus-specific crop growth)
  - JULES (Dynamic Global Vegetation Model)
  - IMAGE (Integrated Assessment Model)
- Climate forcing:
  - MiscanFor and JULES: downscaled, bias-corrected HadGEM2-ES RCP2.6 (ISIMIP-based)
  - IMAGE: MAGICC-calculated RCP2.6 downscaled to grid
- Land-use pathway:
  - SSP2-driven bioenergy expansion defined within IMAGE; rapid growth in 2020s-2030s, peak around 300 Mha by 2040, with a maximum expansion rate of 24 Mha/yr (2035–2040)
- Focus regions and periods:
  - Tropics: 2040–2049
  - Europe: 2090–2099
- Purpose:
  - Illustrate bioenergy’s role as an inexpensive energy source and as a sustainable feedstock for BECCS
- Primary outputs:
  - Yield and soil carbon projections

## Data structure and content
- Dataset contains variables for bioenergy crop yield and soil carbon for all three models.
- File organization:
  - {model}_{variable}_{period}.csv
  - MiscanFor: CSV; JULES and IMAGE: NetCDF
  - Data processed in MATLAB; regridded to a common 0.5-degree grid; units standardized
- Spatial coverage:
  - 6,858 grid cells selected from global 0.5-degree grid; include any bioenergy land use during the simulation
  - Represents ~11% of global land area ( Antarctica excluded); remaining 89% not modeled due to no bioenergy land use
- Grid alignment:
  - All files share the same 6,858 cell order; some cells may be NaN in certain models/periods
- Coordinates and units:
  - Columns: latitude, longitude, value
  - Latitude/Longitude: grid cell centers (degrees)
  - Yield units: tonnes dry matter (DM) per hectare of planted area per year
  - MiscanFor yields: direct DM
  - JULES/IMAGE yields: biomass t C converted to DM with 48% carbon content
  - Soil carbon change units: tonnes C per hectare per year
  - MiscanFor: per hectare of planted area
  - JULES/IMAGE: per grid cell (including effects of other land cover/environmental change)
- Interpretation note:
  - Differences in denominators (planted area vs grid cell area) affect soil carbon interpretation; see Littleton et al. (2022)

## Quality control and provenance
- Models are state-of-the-art and subjected to rigorous validation across sites.
- Versions and related works:
  - JULES: Littleton et al. (2020)
  - MiscanFor: Shepherd et al. (2020)
  - IMAGE: Daioglou et al. (2019); Doelman et al. (2019)
  - Publication underpinning dataset: Littleton et al. (2022), GCB Bioenergy
- Code availability:
  - JULES public repository; used version: r12164_biotiles_harvest

## Usage notes and limitations
- Spatial scope:
  - Only 11% of global land modeled due to bioenergy land-use presence; cautions against broad extrapolation to global scales
- Data coverage:
  - Some cells have missing data (NaN) in one or more models/periods
- Scale and resolution:
  - 0.5-degree grid; may limit local-level inferences and policy-relevant specificity
- Unit and methodological differences:
  - Distinctions in yield and soil carbon accounting across models require careful cross-model comparison
- Reproducibility and access:
  - Dataset documents raw model outputs, enabling reproduction and further analysis of Miscanthus bioenergy’s climate mitigation potential
- Practical application:
  - Useful for exploring cross-model consensus on Miscanthus yield, soil carbon changes, and implications for bioenergy-based mitigation under SSP2-RCP2.6

## References and related materials
- Littleton et al. (2022). Uncertain effectiveness of Miscanthus bioenergy expansion for climate change mitigation explored using land surface, agronomic and integrated assessment models. GCB Bioenergy, 15, 303-318.
- JULES model and related mutation/version details: Littleton et al. (2020); code availability via Met Office repository
- Supporting methodological references: Daioglou et al. (2019); Doelman et al. (2019); Hempel et al. (2013); Riahi et al. (2017); Shepherd et al. (2020)