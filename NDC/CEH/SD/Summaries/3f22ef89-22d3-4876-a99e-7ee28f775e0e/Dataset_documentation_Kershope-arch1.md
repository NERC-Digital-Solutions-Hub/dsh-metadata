# Solute concentrations in water samples from clearfelled and standing Sitka spruce forest ecosystems, Kershope Forest

- Overview
  - Dataset from Kershope Forest, Cumbria, England, documenting solute concentrations and related water chemistry in clearfelled and standing Sitka spruce plantations.
  - Aims to understand how clearfelling and forest stand condition affect nutrient fluxes and soil-plant-water interactions, with implications for forest fertility across rotations.

- Study design and site
  - Experimental setup: six plots within Block 1 of a long-running drainage experiment; three plots felled (in 1983), three remain standing.
  - Location: peaty gley soils, upland Britain; slope 1–5 degrees; mean altitude ~225 m.
  - Drainage: drains from each plot channeled to a single exit drain; weekly drainage-water sampling began 2 years before felled plots and continued after removal of felled debris.
  - Plot treatments and layout: six plots with varying drain spacing (10–40 m) and depths (60–90 cm); felled vs. unfelled design to assess pre- and post-felling conditions.

- Data collected and variables
  - Solutes in drainage water: potassium (K), calcium (Ca), magnesium (Mg), iron (Fe), sodium (Na), aluminium (Al), phosphate (PO4-P), nitrate (NO3-N), ammonium (NH4-N), chloride (Cl), sulphate (SO4-S); plus pH, suspended solids (TSS), and total organic carbon (TOC).
  - Additional water sources sampled: soil solution samplers, lysimeters (soil horizons L and O; eluviated E; organic horizons), rainfall, stemflow, throughfall, Knapp throughflow (though Knapp data flagged as unreliable), and needle trays.
  - Sampling frequency and scope:
    - Drainage water: weekly samples from main exit drains; discharge measured with a V-notch weir; occasional flood-time samples added.
    - Soil solution and lysimeters: fortnightly samples.
    - Rainfall: weekly samples from bulk collectors.
    - Stemflow and throughfall: biweekly to fortnightly bulked samples.
    - Needle trays: biweekly samples.
  - Analytical methods: a mix of atomic absorption, flame emission, colorimetric assays, and ion chromatography across years; cross-method comparisons performed to ensure compatibility.

- Data files and metadata
  - Drainsker.csv: solute data for drainage water from six drains; includes discharge (m3 s-1), pH, TSS, TOC, and all solutes (K, Ca, Mg, Fe, Na, Al, PO4-P, NO3-N, NH4-N, Cl, SO4-S, plus unit indicators).
  - Soilsker.csv: solute data from soil solution samplers and lysimeters, along with horizon-specific data (L, O, E, B horizons) and throughfall-related samples (volume and concentration codes).
  - Kershope_sampling_points.csv: sampling locations and description for plots, blocks, felled status, drainage spacing/depth, and coordinates (easting/northing).
  - Kershope_codes.csv: key to sample codes used in Soilsker.csv (maps sample types, horizons, and events such as felled/unfelled, stemflow, rainfall, throughfall, knapped throughflow, lysimeters, etc.).
  - Dataset period and coverage: drainage water data from 17/6/1981 to 30/12/1987; water-sample data (soil solution, lysimeters, rainfall, stemflow, throughfall, needle trays) collected mainly from 1981–1985; full dataset includes derived references and related publications.

- Temporal and geographic coverage
  - Time period: 1981–1987 (with some sampling specifically 1981–1985 for water samples); pre- and post-felling phases captured.
  - Geography: Kershope Forest, Cumbria, England; upland peat gley soils with minimal prior fertilization.

- Purpose, uses, and context
  - Facilitates analysis of how clearfelling influences solute fluxes and soil-plant-water dynamics, informing potential nutrient losses and changes in soil fertility across forest rotations.
  - Related publications cited include studies on changes in solute chemistry following clearfelling and broader implications for soil fertility and water acidity.

- Methods, challenges, and considerations
  - Longitudinal design with multiple sampling media across standing and felled plots enables attribution of observed changes to felling.
  - Variations in sampling methods and analytical techniques over the study period require careful data harmonization.
  - Some data (e.g., Knapp throughflow) are noted as not entirely reliable due to instrumentation issues.
  - The dataset is designed to support cross-source integration, with explicit metadata on sampling points, plots, and block configurations to aid reproducibility and secondary analyses.

- References and further reading
  - Key publications detailing the environmental impact of clearfelling on drainage solute concentrations and related hydrological processes (e.g., Adamson et al. 1987, 1990; Pyatt et al. 1985; Rowland 1983; Allen 1989; Neal et al. 1999).
  - Contextual background on Sitka spruce plantations established in upland Britain and nutrient dynamics in drainage waters.