# Frame Modelling

- FRAME (Fine Resolution Multi-pollutant Exchange) is a Lagrangian atmospheric transport model used to estimate annual mean deposition of reduced and oxidised nitrogen and sulphur over the United Kingdom.
- Domain and resolution: British Isles, 5 km grid, 172 x 144 grid.

- Emissions inputs:
  - From UK National Atmospheric Emissions Inventory (NAEI): 160 sub-sectoral categories; includes 22 point sources and background 'area' emissions split into 11 SNAP sectors; includes international shipping and European emissions.
  - Ammonia inputs from the National Ammonia Reduction Strategy Evaluation System (NARSES) model, split into 5 sectors (e.g., livestock, fertiliser, non-agricultural NH3 sources, waste sector).

- Source regionalisation:
  - Regional land masks separate sources by England, Scotland, Wales, and Northern Ireland to aid regulator oversight.

- Model runs and footprint calculation:
  - A base scenario (all sources) is run, then the model is run with each emission source abated one at a time (25% reduction per run to mitigate non-linearities in chemistry).
  - Final footprints are scaled by a factor of 4; footprints are computed as the difference between the baseline deposition and the deposition with the specific source abated.
  - For every 5 km grid square, deposition of SOx, NOy, and NHx is calculated across all footprints, including a breakdown into short-range and long-range contributions for various source types.

- Short/long-range and ecosystem splits:
  - Depositions are further partitioned into 11 source-attribution categories (e.g., livestock, fertiliser, shipping) into short-range and long-range components.
  - Deposition data are output for three ecosystem types due to surface roughness effects: forest, moorland, and grid average (arable, grassland, urban, forest, moorland).

- Post-processing and calibration:
  - Individual source footprints are normalised so their sum matches the baseline to account for non-linearities.
  - Calibration against the CBED (Concentration Based Estimated Deposition) dataset for 2011–2013 is applied to align FRAME outputs with measured deposition (year 2012 used for calibration).
  - Calibration equations ensure the calibrated footprints, when summed, reproduce official CBED totals for 2012.

- Spatial mapping and outputs:
  - FRAME produces 160 files per footprint type for each pollutant; these are aggregated to 90 footprint files to ease processing.
  - Output data include 5 x 5 km grid deposition for SOx (sulphur), NOy (oxidised nitrogen), and NHx (reduced nitrogen), with detailed breakdowns by short/long-range and ecosystem type (grid average, forest, moorland).
  - Data fields cover coordinates (Easting/Northing), footprint IDs, source locations (by country), and deposition components for each footprint (local grid, forest, moorland) in both short and long-range forms.

- Data quality, access, and formats:
  - Quality control includes normalising footprints, national budget checks for total deposition, and generating a jpg for each footprint to flag potential errors.
  - Data are provided as x90 footprint datasets, with ecosystem-specific source attribution for moorland or forest/woodland or grid average.
  - Access and field definitions are documented via the project resource: http://www.pollutantdeposition.ceh.ac.uk/node/319.