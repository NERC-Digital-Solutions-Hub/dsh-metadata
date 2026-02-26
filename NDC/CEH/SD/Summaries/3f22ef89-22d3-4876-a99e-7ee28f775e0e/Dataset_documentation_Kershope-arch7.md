# Solute concentrations in water samples from clearfelled and standing Sitka spruce ( Picea sitchensis ) forest ecosystems, Kershope Forest

- Purpose and scope
  - Dataset documenting solute concentrations (various cations, anions, nutrients, pH, suspended solids, TOC) in drainage and related waters from a Sitka spruce forest at Kershope, England.
  - Focus on differences between clearfelled and standing forest within Block 1 of a drainage experiment.

- Geographic and site context
  - Location: Kershope Forest, Cumbria, England; peaty gley soils on gentle slopes (1–5 degrees; ~225 m altitude).
  - Experimental design: six plots in Block 1 (drainage experiment), with three plots felled in 1983 and three remaining unfelled.
  - Drainage network: open drains with a single exit drain per plot; sampling equipment installed to channel all plot outflow through a defined point.

- Experimental design and sampling framework
  - Plot treatments and layout
    - Block 1: six plots with varying drain spacing and depths; three plots felled (in 1983) and three unfelled controls.
    - Drain parameters: combinations of spacing (10, 20, 40 m) and depth (60–90 cm).
  - Sampling regimes
    - Drainage water: weekly samples from main exit drains (1981–1987; 1981–1987 for drains; 1981–1985 for water samples in some components).
    - Other water sources: soil solution samplers, lysimeters, rainfall, stemflow, throughfall, Knapp throughflow (notably some Knapp data flagged as unreliable), and needle trays; sampling frequency ranges from fortnightly to weekly depending on source.
  - Data collection and analysis
    - Sample collection and chemical analyses conducted by ITE Merlewood; cross-checks of methods across years to ensure comparability.

- Datasets and file descriptions
  - Drainsker.csv
    - Contains solute concentrations and related measurements from the six main drains, plus discharge, pH, TSS, TOC, and ion concentrations (K, Ca, Mg, Fe, Na, Al, PO4P, NO3N, NH4N, Cl, SO4S) across sampling occasions.
  - Soilsker.csv
    - Contains solute data from soil-related samplers (lysimeters and soil solution samplers) across horizons and samplers, with a weekly-to-fortnightly cadence.
  - Kershope_sampling_points.csv
    - Spatial locations and metadata for sampling points (easting/northing coordinates, plot/block identifiers, felled status, sampling point descriptions).
  - Kershope_codes.csv (referenced as codes for sample interpretation)
    - Key to sample codes used in the dataset, detailing associations between sample types, horizons, plot descriptors, and sampling equipment.
  - Additional context
    - Datasets include detailed field metadata for drains, sampling points, and sample types, with explanations of sampling gear (e.g., PVC pipe sampling at drains), and sample codes for ease of GIS integration.

- Measurements, variables, and units
  - Analytes and properties
    - Solutes: potassium (K), calcium (Ca), magnesium (Mg), iron (Fe), sodium (Na), aluminium (Al), phosphate (PO4P), nitrate (NO3N), ammonium (NH4N), chlorine (Cl), sulphate (SO4S)
    - Other metrics: pH, suspended solids (TSS), total organic carbon (TOC), plus water discharge (flow) from drains.
  - Units and data structure
    - Concentrations in mg L-1 (various ions), pH (unitless), discharge in m^3 s^-1, TSS and TOC in mg L^-1, with additional fields for sampling date and sampling occasion.
  - Temporal coverage
    - Drainage water sampling: 17/6/1981 – 30/12/1987
    - Water sample analysis (varied by component): 17/6/1981 – 23/12/1985

- Methods and data quality
  - Analytical methods
    - Calcium, magnesium, aluminium, iron by atomic absorption spectrophotometry; sodium and potassium by flame emission spectrometry.
    - Phosphate-P by molybdenum blue; ammonium-N by indophenol blue.
    - Chloride by thiocyanate (early years) and later ion chromatography; nitrate by reduction and Griess-Hosvay method; sulphate by turbidity (later by ion chromatography).
    - TOC and suspended solids measured by standard methods; cross-method checks during transition periods to ensure comparability.
  - Data considerations for GIS use
    - Some historical methods differed; come with notes on comparability checks across methods.
    - Knapp throughflow data noted as unreliable due to sampling issues; treat accordingly in analyses.

- GIS-focused considerations and use cases
  - Spatial layers to create
    - Drainage network layer: lines representing drains and a defined main exit channel per plot; attributes for plot, block, drain spacing, drain depth, and felled status.
    - Plot polygons: delineate the six plots (≈2–3 ha each) within Block 1; include felled vs unfelled attribute.
    - Sampling points layer: point features from Kershope_sampling_points.csv with coordinates (Easting/Northing) and descriptions; link to drain and soil sampling data.
    - Soil and lysimeter sampling layers: point or polygon representations for sampler locations and horizons; connect to Soilsker.csv data.
  - Temporal data handling
    - Time-enabled (longitudinal) GIS analysis: join Drainsker.csv and Soilsker.csv to sampling points by date or sampling occasion; create time series of solute concentrations per plot/drain.
  - Analytical context
    - Use Kershope_codes.csv to interpret sample types, horizons, and collection methods when integrating into GIS layers.
  - Potential outputs
    - Maps of nutrient flux through the drainage network by plot and timing (pre- vs post-felling comparisons).
    - Spatial-temporal dashboards showing changes in solute concentrations across treatments and over time.
    - Comparability-aware visualizations due to method transitions (document method notes in metadata).

- References and further reading
  - Key publications and methodological references underpinning the dataset (e.g., Adamson et al. on drainage chemistry, Rowland and Allen for analytic methods, Pyatt et al. for site description and experimental design).

- Practical notes for users
  - Data originate from a historical forest hydrology experiment (1981–1987) with careful sampling across multiple ecosystem components; spatial coordinates are provided for sampling points to support GIS integration.
  - The dataset supports analysis of nutrient flux changes due to clearfelling and can inform map-based visualizations of spatial patterns and temporal trajectories in soil and drainage chemistry.