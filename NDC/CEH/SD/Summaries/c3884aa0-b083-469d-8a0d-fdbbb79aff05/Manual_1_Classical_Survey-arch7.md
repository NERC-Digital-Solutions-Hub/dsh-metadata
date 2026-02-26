# ESPA p4ges PROJECT Work Package Carbon (WP4-Carbon)

- Context: The p4ges project in Madagascar aims to influence pay-for-ecosystem-services schemes at international scale. WP4 focused on carbon stock assessment within the Ankeniheny Zahamena (CAZ) forest corridor, evaluating Aboveground Biomass (AGB), Belowground Biomass (BGB), litter, dead wood, and Soil Organic Carbon (SOC) across five IPCC pools. The manual outlines design, sampling, preliminary data handling, and archiving processes for carbon quantification, with datasets archived at the Environmental Information Data Centre (EIDC).

## Spatial design and scope

- Zones of Interest (ZOI): Four zones identified to capture CAZ representativeness
  - ZOI1 Lakato, ZOI2 Andasibe, ZOI3 Anjahamana/Ambalarondra, ZOI4 Didy
- Biophysical and contextual criteria:
  - Altitude, slope, bioclimate, dry season length, soil type
  - Deforestation history and access
- Land-use classification within sites
  - Closed canopy, tree fallow, shrub fallow, tany maty (degraded land), plus reforestation
- Site criteria for sampling
  - Slope < 45 degrees
  - Patches near habitat center; minimum 120 m x 120 m
  - Edge effects avoided; no transect crossing streams; at least 500 m between sites
- Number and layout of sites
  - 16 plots per ZOI (4 land uses x 4 replicates)
  - Additional plots for WP4 to capture C-stock variability
  - Totals: ZOI1 28 sites, ZOI2 48 sites, ZOI3 28 sites, ZOI4 28 sites
  - Remote sensing used to identify site locations; one site per land use

## Field reconnaissance and sampling design

- Field reconnaissance
  - Multi-WP verification (Carbon, Hydrology, Biodiversity) and CI participation
  - Confirm suitability, indicator species, land-use history, accessibility
- Minimal area test
  - Quadrat-based species inventory starting at 1 m x 1 m, expanded until no new species appeared
  - Result: 16 m² identified as the minimal representative area for C stock quantification
- Administrative and field preparation
  - Permits, mission orders, insurances
  - Data collection sheets, field materials, sample bags, labeling, scales

## Plot design and sampling by land use

- General plot design
  - Plot: 5 m radius; four subplots within the circular area
- Biomass and vegetation measurements
  - Saplings (DBH < 5 cm, height > 1.30 m): 2 m radius area; 5 species sampled and weighed
  - Trees 5–10 cm DBH to 20 cm DBH: concentric circular areas (5 m, 10 m radii) for DBH and height with local names
  - Trees > 20 cm DBH: 20 m radius area; full DBH and height; local names recorded
  - Standing dead wood: measurements at 1.3 m height; wood density category (Sound, Intermediate, Rotten)
  - Lying dead wood: 100 m transect; diameter intercepts and wood density recorded
- Aboveground biomass by direct measurement (closed canopy)
  - 54 trees chosen by contribution to density; trees felled and weighed by trunk, branches, leaves; moisture analysis of subsamples
- Understorey, litter, and root mat
  - Understorey: 1 m x 1 m quadrats; biomass weighed and sampled
  - Litter and root mat: 25 cm x 25 cm quadrats; biomass collected and recorded
- Root description and sampling
  - 1 m² soil pit per plot center; roots categorized as medium (2–10 mm) and coarse (>10 mm); depth distribution described
- Percent cover estimation
  - Braun-Blanquet scale (0 to >95%) within a 5 m radius around indicator species
- Degraded land (tany maty)
  - No large trees; biomass sampling, root description, and percent cover only

## Soil sampling and analysis

- Soil sampling design
  - Sampling points collocated with understorey plots (points 1–4)
  - Two methods: auger for carbon content (0–100 cm, in 10 cm increments) and cylinders for bulk density (0–90 cm, specific depths)
  - Soil profile description in a central soil pit (1.30 m depth) to characterize horizons, color (Munsell), texture, structure, root density
- Soil laboratory procedures
- Soil analysis approaches
  - Walkley-Black method for SOC (calibration reference)
  - Mid Infrared Spectroscopy (MIRS) for prediction of soil carbon
  - δ13C stable isotope analyses for selected samples (Montpellier LBMP)

## Data handling and storage

- Field and lab data workflow
  - Field forms scanned and stored; data entered in Excel; photos stored in project data center
  - Data organized into data series and archived at EIDC
  - Lab analyses managed at LRI; sample-to-lab tracking with field and lab identifiers
- Sample management
  - Lab numbers linked to field provenance; worksheets prepared prior to analysis

## Biomass, soil, and carbon stock analysis

- Aboveground biomass (AGB)
  - Use allometry: biomass per tree estimated via equations (based on DBH, height, WSG)
  - Tree-level biomass aggregated to plot level and scaled to per hectare (Mg ha⁻¹)
  - Carbon stock inferred by converting biomass using a standard factor (0.5)
- Litter, understorey, and root mat
  - Dry weight from field samples scaled to per hectare; carbon stock via 0.5 conversion
- Dead wood
  - Lying dead wood: volume and density-based biomass calculations using transect data
  - Standing dead wood: volume and density-based biomass calculations
- Soil carbon stocks
  - SOC stock per depth (0–30 cm, 0–100 cm) computed using:
    - SOC stock = sum(BD_i × C_i × (1 − CF_i) × t_i × 0.1)
    - Where BD = bulk density, C_i = carbon content, CF_i = coarse fraction, t_i = layer thickness
  - Consideration of equivalent mass method to account for soil density differences across land uses
  - SOC30 and SOC100 treated as key depth-specific stock metrics
- Integration
  - All pools combined to yield total carbon stock per plot per hectare

## Data publication and references

- Outputs and publications
  - Several peer-reviewed papers and conference outputs cited (soil carbon mapping, carbon stock changes, methodology challenges)
- Data archiving and availability
  - Datasets archived at EIDC; data prepared for long-term valorization
- References and methodological baseline
  - IPCC (2006) guidelines; Braun-Blanquet scale; Brown (2002); Walkley-Black method; Wood density and allometry references; relevant Madagascar-specific studies

Note: The document emphasizes a GIS-relevant workflow, including site selection and plot geolocation via remote sensing, detailed spatial design (ZOIs and land-use classes), multi-paceted field measurements, and a robust data pipeline suitable for map-based carbon stock visualization and regional analyses.