# Soil methane sink capacity response to a long-term wildfire chronosequence in northern Sweden

- Study context
  - investigates soil methane (CH4) fluxes and oxidation across a wildfire-driven chronosequence on 30 freshwater islands in a boreal forest archipelago (lakes Uddjaure and Hornaven, northern Sweden).
  - Islands vary in size (0.02 to 15 ha) and fire history; retrogressive chronosequence with island size as a proxy for successional stage.
  - Baseline climate shared across islands: mean annual precipitation ~750 mm; July mean temp +13°C; January mean temp -14°C.
  - All islands at similar distance from shore to minimize erosion/wind/radiation confounding.

- Data collected and measurements
  - In situ CH4 fluxes
    - method: static chamber (volume 0.0054 m3; base ring installed 5 cm into humus); multiple headspace samples over 30 minutes.
    - analysis: CH4 quantified by gas chromatography; detection limit ~0.05 ppm CH4; fluxes computed by standard linear regression.
    - sampling: n=5 per island during a one-week campaign (Aug 2006).
  - Ex situ CH4 fluxes from intact soil cores
    - 2006: top 25 cm or to bedrock; four cores per island (n=40 per island size class); maintained at field moisture; chamber volumes smaller for cores; sampling at multiple time points up to 150 minutes.
    - 2007: full humus profile cores (0.15 m diameter) to bedrock; similar chamber method.
    - analyses mirror in situ approach with exetainers and GC.
  - In situ depth profiles of isotopes and concentrations
    - measured CH4 and CO2 concentrations and δ13CH4 within humus profiles at depths 15, 35, 55, 75 cm (4 probes per island; samples collected over 4 days in July 2007).
    - δ13C-CH4 analyzed by isotope ratio mass spectrometry after gas pre-treatment; precision ≤ 0.2‰.
  - Isotopic method to quantify CH4 oxidation
    - uses Top-to-Bottom δ13C-CH4 approach to estimate aox (isotopic fractionation during methanotrophy).
    - Mass balance model adapted from landfill studies to estimate fraction oxidised Fo, accounting for diffusion/transport fractionation (trans). atrans treated as 1.0195 (diffusion-based value from temperate forest soils) due to inability to directly measure it.
    - Fo × 100 gives percentage CH4 oxidised.
  - Ecosystem and soil properties
    - 2006 cores: soil pH, %C, %N (pH by soil:water 1:3; elemental analysis for C/N).
    - July 2007: humus depth measured along transects; additional data on vegetation mass, shrub productivity, tree productivity, and humus mass referenced from prior work.
  - Temporal and spatial scope
    - measurements span 2006–2007 across 30 islands, enabling assessment of successional-stage and depth-related differences in CH4 flux and oxidation.

- Data processing and statistical analyses
  - software: R
  - modelling approaches
    - simple regression for relationship between CH4 flux/oxidation and successional age (inferred from 14C dating) or humus development.
    - differences among successional stages (Early, Mid, Late) tested with generalized linear models (glm); non-negative data adjustment applied (constant shift).
    - differences in CH4 metrics across depths and stages analysed with linear mixed-effects models (nlme), with Island as a random effect to account for repeated measures per core.
  - quality checks
    - diagnostic plots to assess residuals and heteroscedasticity.

- GIS-relevant insights and potential map-based data products
  - Spatial layers to develop
    - CH4 flux maps (in situ and ex situ) by island, linked to successional stage and island size.
    - CH4 oxidation fractions (Fo) and deconvoluted oxidation rates using isotopic approach per island and depth profile.
    - δ13CH4 and CH4 concentration depth profiles across humus layers for each island.
    - associated soil properties maps: pH, %C, %N, humus depth, vegetation productivity indicators.
  - Data integration opportunities
    - align flux measurements with island geometry, area, successional stage, and fire history to explore spatial patterns in CH4 cycling.
    - combine isotopic oxidation estimates with flux data to map spatial gradients of methane sink strength.
    - use the chronosequence design (age proxy from 14C dating) to infer temporal trajectories across a spatially distributed set of islands.
  - Considerations for GIS workflows
    - ensure consistent island-level identifiers to link flux measurements, depth profiles, and soil properties.
    - account for sampling dates and year-specific conditions when comparing spatially distributed measurements.
    - handle depth-resolved data by creating layered raster/vector representations or multi-table linked datasets.

- Limitations and assumptions relevant to mapping
  - In situ measurements reflect short-term fluxes (one-week window) and may not capture longer-term variability.
  - Isotopic oxidation estimates depend on assumed trans value; atrans treated as a fixed diffusion-based value due to measurement constraints.
  - Island-level random effects imply potential non-independence of cores within the same island.
  - Spatially, data are tied to discrete islands within a limited geographic region; extrapolation beyond this archipelago should be cautious.

- Summary takeaway for GIS-focused use
  - The study provides a rich, island-scale dataset linking CH4 fluxes, methane oxidation, isotopic signatures, and soil/vegetation properties across a boreal wildfire chronosequence.
  - Suitable for producing map-based data products that visualize spatial variation in methane uptake and oxidation capacity, and how these relate to successional stage, soil chemistry, and humus depth across the island archipelago.