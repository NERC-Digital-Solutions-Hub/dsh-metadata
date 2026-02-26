# ESPA p4ges PROJECT Work Package Carbon (WP4-Carbon)

- Context and aim
  - Malagasy project to influence the implementation of payments for ecosystem services at international scale.
  - Carbon survey within the Ankeniheny-Zahamena Forest Corridor (CAZ) focuses on carbon stock in five IPCC pools, with emphasis on Aboveground Biomass (AGB), Litter, Dead Wood (DW), and Soil Organic Carbon (SOC; BGB and soil pools are covered in related work).
  - Manual describes sampling design, field data collection, laboratory analysis, and initial data handling to quantify carbon stocks across CAZ.

- Spatial design and Zones of Interest (ZOI)
  - Four Zones of Interest selected to represent CAZ conditions: ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana/Ambalarondra, ZOI4 Didy.
  - Each ZOI contains 3–4 campsites, forming 16 plots per ZOI (4 land-use types × 4 replicates) to capture variability.
  - Additional plots were surveyed within each ZOI to better capture carbon stock variability (total plots: Lakato 28, Andasibe 48, Anjahamana 28, Didy 28).
  - Site locations identified via remote sensing; GPS coordinates used for GIS-ready data.

- Land use classification and site selection criteria
  - Land uses (per Styger et al. 2007) include: Closed canopy, Tree fallow, Shrub fallow, Tany maty/Degraded land; reforestation included based on NGO/community input.
  - Site criteria (beyond land-use type): slope < 45 degrees; sites ≥ 120 m × 120 m; avoid edge effects and unusual disturbances (e.g., mining); transects not across streams; minimum 500 m between sites.
  - Field reconnaissance verified suitability and indicator species; documented land-use history.

- Field sampling design and plot structure
  - Minimal area test established 16 m² as the representative unit for C stock quantification.
  - Overall plot design includes a central circle with four nested subplots (2 m, 5 m, 10 m, and 20 m radii) for biomass components.
  - In closed canopy and fallows:
    - Forest inventory across four subplots; saplings (DBH < 5 cm, H > 1.30 m) counted and weighed for several species.
    - Trees measured for DBH and height in progressively larger circles; standing and lying dead wood recorded with density classifications (Sound, Intermediate, Rotten).
    - Direct aboveground biomass for a subset of trees (54) via felled weight measurements; subsamples for moisture; allometric estimates applied to estimate plot-level biomass.
    - Understorey, litter, root mat sampled with 25 cm × 25 cm quadrats and 1 m × 1 m plots; biomass weighed and lab-subsamples prepared.
    - Root descriptions in a central soil pit; roots categorized as Medium Root (2–10 mm) or Coarse Root (>10 mm); density and depth documented.
    - Percent cover estimated for indicator species in a 5 m radius using Braun-Blanquet scale.
  - In degraded land (tany maty): no tree inventory beyond sapling/understorey; biomass, litter, root mat, and soil sampling proceed with same design (no large trees).

- Soil sampling and soil analysis
  - Soil sampling at four subplots (points 1–4) with two methods:
    - Auger sampling for carbon content at 0–100 cm in 10 cm increments.
    - Cylinders for bulk density at 0–10, 10–20, 20–30, 50–60, and 80–90 cm depths.
  - Soil profile description in a central pit (1.30 m depth) to capture horizons, color (Munsell), texture, structures, root density, and porosity.
  - Soil analyses:
    - Moisture via oven-drying (105°C).
    - Walkley-Black method for baseline soil organic carbon; calibration with MIRS (Mid Infrared Spectroscopy) for predicting SOC from spectra.
    - δ13C stable isotope analyses on selected samples (France-based LBMP) to study carbon dynamics across land uses.
  - SOC stocks calculated for 30 cm (SOC30) and 100 cm (SOC100) depths using bulk density, carbon content, coarse fraction, and layer thickness; equivalent mass method considered to account for density differences across land-use types.

- Data handling, storage and data flow
  - Field forms scanned and archived; data entered into Excel; photos stored in project data center.
  - Data organized into series and deposited in Environmental Information Data Centre (EIDC) for long-term storage and valorization.
  - Field-to-lab sample tracking: samples assigned lab and provenance numbers; lab worksheets linked to field data.
  - LRI laboratory processes store and dry biomass samples; weight and moisture data feed into biomass and C stock calculations.
  - Data outputs intended as GIS-ready inputs for mapping carbon stocks across CAZ.

- Biomass and soil carbon stock estimation approaches
  - Aboveground biomass (AGB): use allometric equations (based on DBH, height, and wood density) to estimate tree-level biomass; sum across trees per plot; convert to Mg C ha−1 using standard conversion factors.
  - Subplot and strata biomass: understorey, litter, and root mat converted to plot-level and then to per-hectare stocks.
  - Dead wood: volume calculations for lying wood along 100 m transect; standing dead wood biomass computed from volume and density; total plot biomass aggregated.
  - Soil organic carbon: SOC Stock = sum across layers of (bulk density × carbon content × (1 − coarse fraction) × layer thickness) adjusted to target depths (SOC30 and SOC100).

- Data publication and references
  - Data and analyses linked to several publications on soil organic carbon mapping and land-use change effects in Madagascar; dataset and methods documented for future reuse and GIS mapping.

- GIS-relevant outputs and applications
  - Spatially explicit carbon stock estimates across CAZ by pool and land-use type.
  - Zone and site metadata (ZOI, coordinates, land-use type, slope, distance constraints) to support reproducible map products.
  - Foundation for carbon stock maps, change detection over time, and integration with policy-oriented GIS dashboards for payments for ecosystem services and conservation planning.