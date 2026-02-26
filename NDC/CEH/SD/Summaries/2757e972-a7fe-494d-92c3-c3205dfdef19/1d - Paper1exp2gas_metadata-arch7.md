# Soil Gas Flux Measurement Dataset - Field Descriptions and Metadata

- The document lists field names and descriptions for a soil gas flux dataset collected from soil cores, including cumulative gas flux values, initial gas concentrations, sampling timing, and soil/substrate properties.
- Included fields cover core identifiers, timepoints, biochar treatment, gas flux measurements for CO2, CH4, N2O, and CO, initial headspace concentrations, environmental conditions, soil physical properties, chamber geometry, and biochar details.
- Units and derived metrics are defined (e.g., ug CO2-C flux g-1 dry soil; ng CH4-C flux g-1 dry soil; gravimetric water content, bulk density, and related waterholding concepts).

## Key data categories

- Core and timing
  - soilcoreno: Unique soil core/sample identifier
  - timepoint: Timepoint of measurements
  - dayfromstart, hourfromstart: Time since the start of measurements

- Treatment and amendments
  - biochartreatment: Whether biochar was added (un-amended vs amended)
  - biocharweight: Dry biochar weight added to the soil
  - biocharfraction: Proportion of biochar relative to dry soil weight

- Gas flux (cumulative)
  - ugCO2-Cfluxg-1cumu: Cumulative CO2 flux (micrograms of CO2-C per gram dry soil)
  - ngCH4-Cfluxg-1cumu: Cumulative CH4 flux (nanograms of CH4-C per gram dry soil)
  - ngN2O-Nfluxg-1cumu: Cumulative N2O flux (nanograms of N2O-N per gram dry soil)
  - ugCO-Cfluxg-1cumu: Cumulative CO flux (micrograms of CO-C per gram dry soil)

- Initial gas concentrations (headspace at t0)
  - CO2ppmt0, CH4ppmt0, N2Oppmt0, COppmt0: ppm in static chamber headspace at t0

- Environmental and soil state at sampling
  - tempair: Air/soil temperature at measurement time
  - gravwatercontentproportion: Gravimetric water content (as a proportion)
  - bulkdensitygcm3: Soil bulk density
  - wfpsproportion: Water-Filled Pore Space fraction (derived: gravimetric wc * (bulk density / total porosity))
  - maximumwhc: Maximum water holding capacity
  - proportionofwhc: Proportion of maximum WHC at sampling

- Chamber and sample geometry
  - chambaream2: Soil chamber area (m^2)
  - headvolm3: Chamber headspace volume (m^3)
  - datetimefirst: Date/time of the first soil gas flux measurement
  - drysoilweightg: Weight of dry soil in the core (g)

## GIS integration considerations

- Represent each soil core as a point feature with:
  - Core metadata: soilcoreno, biochartreatment, datetimefirst, dayfromstart, hourfromstart
  - Chamber/soil properties: chambaream2, headvolm3, drysoilweightg, bulkdensitygcm3, gravwatercontentproportion, wfpsproportion, maximumwhc, proportionofwhc
  - Biochar context: biocharweight, biocharfraction
  - Gas measurements: initial concentrations (CO2ppmt0, CH4ppmt0, N2Oppmt0, COppmt0) and cumulative fluxes (ugCO2-Cfluxg-1cumu, ngCH4-Cfluxg-1cumu, ngN2O-Nfluxg-1cumu, ugCO-Cfluxg-1cumu)
  - Environmental context: tempair, datetimefirst, dayfromstart, hourfromstart

- Time-series handling:
  - Option A: Store per-timepoint measurements as wide attributes (one column per timepoint) for rapid access - may lead to wide tables with many columns as the experiment scales.
  - Option B: Normalize into a related time-series table (core_id, timepoint, dayfromstart, hourfromstart, gas_flux_values, initial_ppms, environmental fields carried as static attributes) to support scalable GIS analyses and temporal visualizations.

- Derived fields to aid visualization:
  - wfpsproportion, maximumwhc, proportionofwhc (for quick soil moisture-aware mapping)
  - Total cumulative flux per core over time (computed in post-processing)

- Visualization approaches:
  - Point maps colored by latest cumulative flux (e.g., ug CO2-C flux g-1 dry soil) with time slider to animate across timepoints
  - Overlay with soil properties (bulk density, WHC) and treatment (biochar vs control)
  - Choropleth or heatmap layers for spatial patterns of gas flux
  - Time-series charts per core or per region to show gas flux trends

## Data quality, standards, and challenges (GIS perspective)

- Data sources are distributed; ensure consistent data standards and units across all fields.
- Units are explicit but watch for unit consistency during integration (e.g., ug vs ng, C-flux vs N-flux).
- Data gaps and missing values common; plan for missing-value handling in GIS workflows.
- Large or complex datasets require data partitioning or related-table designs to keep workflows efficient.
- Data cleaning and transformation are essential before GIS modeling (standardize field names, harmonize timepoint references, align sampling dates).

## Practical workflow for GIS specialists

- Ingest the dataset as a tabular source (CSV/CSV-like) and create a point feature class using core identifiers and spatial coordinates.
- Add static attributes (core metadata, soil properties, chamber geometry, treatment) to the point features.
- Create a related time-series table for gas flux measurements if using the normalized approach; link via core ID.
- Compute derived metrics (e.g., wfpsproportion, total cumulative flux up to a selected timepoint) within the GIS environment or via an external data processing step.
- Build visualization layers:
  - Map layer: cores colored by latest cumulative CO2-C flux or other gas metric
  - Time-enabled layer: animate flux changes across timepoints
  - Overlay layers: soil properties (bulk density, WHC) and treatment status
- Validate data alignment across spatial, temporal, and attribute dimensions to ensure accurate representations.