# ESPA p4ges PROJECT Work Package Carbon (WP4-Carbon) (Manual n°1)

- Purpose and context
  - The p4ges project aims to evaluate whether paying for global ecosystem services can reduce poverty, focusing on carbon stock assessments in the Ankeniheny-Zahamena Forest Corridor (CAZ), eastern Madagascar.
  - WP4 conducts carbon stock surveys across land uses (AGB, litter, dead wood, SOC) with data archived at Environmental Information Data Centre (EIDC).

- Study area and GIS-relevant framing
  - Four Zones of Interest (ZOI) identified to capture representativeness: Lakato (ZOI1), Andasibe (ZOI2), Anjahamana/Ambalarondra (ZOI3), Didy (ZOI4).
  - ZOIs defined by biophysical criteria (altitude, slope, bioclimate, dry-season length, soil type), deforestation history, and access.
  - Field data collection includes GPS coordinates, slope, land-use history, and site characteristics; remote sensing was used to locate sites and compile spatial datasets.

- Land use classification and site criteria
  - Land uses defined for sampling: Closed canopy, Tree fallow, Shrub fallow, Tany maty (Degraded land), plus reforestation (identified via NGOs and communities).
  - Site selection criteria beyond land use: slope < 45 degrees, patch center proximity to reduce edge effects, minimum area of 120 m x 120 m, avoidance of disturbances (e.g., mining), transects not crossing streams, and minimum 500 m between sites.

- Sampling design (plot-level)
  - A single sampling design covers all carbon pools, with a plot-level radius of 5 m for degraded land (and a consistent approach for soil sampling across land uses).
  - In closed canopy and fallows, four concentric subplots within a circular area:
    - 2 m radius: saplings (DBH < 5 cm, H > 1.3 m) by species; 5 randomly selected saplings weighed and sampled.
    - 5 m radius: trees with 5–10 cm DBH; measure DBH and height; record local names.
    - 10 m radius: trees with 10–20 cm DBH; measure DBH and height; record local names.
    - 20 m radius: trees >20 cm DBH; measure DBH, height, local names; standing dead wood also recorded with DBH/height and wood density category (S, I, R); lying dead wood measured along a 100 m transect (intercept diameter and density).
  - Aboveground biomass (AGB) by direct measurement in 54 trees across four species in closed canopy (felled, weighed by component, lab moisture analysis).
  - Understorey vegetation, litter, and root mat sampled in central subplots and along designated points; sampling via 25 cm x 25 cm quadrats (litter/root mat) and 1 m x 1 m quadrats (understorey) with subsequent lab processing.
  - Root description: 1 m^2 pits at plot center to classify roots by diameter (<2 mm, 2–10 mm, >10 mm) and describe root distribution with soil depth.

- Soil sampling and profiling
  - Soil samples collected at four subplots (points 1–4) using two methods:
    - Auger sampling for carbon content at depths 0–100 cm (0–10, 10–20, ..., 90–100 cm).
    - Cylinder sampling for bulk density at specific depths (0–10, 10–20, 20–30, 50–60, 80–90 cm).
  - Soil profile description conducted in deeper pits (1.30 m) to document horizons, color (Munsell), texture, structure, and root depth.
  - Additional data: GPS coordinates, slope, deforestation history.

- Data handling and storage
  - Field forms scanned and stored in project numeric archive; data entered into Excel; photos renamed and stored in project data center.
  - Collected data organized into series and uploaded to EIDC for long-term storage and valorization.
  - Field-to-lab samples managed with traceability between field and lab identifiers.

- Laboratory analyses and carbon pools
  - Biomass analyses: samples air-dried, oven-dried at 75°C to determine dry biomass; wood specific gravity (WSG) determined later (Manual n°4); direct biomass measurements for selected trees in closed canopy.
  - Litter, understorey, and root samples: oven-dried to determine biomass; upscaling to per-hectare C stocks.
  - Dead wood: calculations for lying and standing dead wood using volume-based and density-based methods; site-level biomass and carbon stocks aggregated per plot.
  - Soil analyses: moisture determination (105°C drying); Walkley-Black method for soil organic carbon (SOC) as calibration reference; Mid Infrared Spectroscopy (MIRS) for SOC content prediction; δ13C stable isotope analysis for selected soil samples (Montpellier LBMP) to support land-use classification and carbon dynamics studies.

- Data processing and carbon stock calculations
  - Aboveground biomass (AGB) and carbon stock per tree computed via allometry (multiple equations, including Chave et al.; Brown 2002 conversion to carbon).
  - Plot-level and per-hectare carbon stocks derived from summing component biomasses and applying scaling factors.
  - Soil carbon stocks calculated using bulk density, carbon content, layer thickness, and coarse fraction corrections; SOC30 and SOC100 reported to reflect depth-specific stocks.
  - Litter, understorey, and root mat stocks converted from dry weights to carbon using standard conversion factors.
  - Standard references and equations used for consistency with IPCC guidelines and prior Madagascar carbon work.

- Data publication and references
  - Published outputs include multiple papers on soil organic carbon mapping, carbon stock variability, and land-use impacts on carbon stocks in Madagascar.
  - Data and methods documented with references to Braun-Blanquet, IPCC guidelines, and foundational carbon measurement literature.

- Key insights for GIS specialists
  - Spatial sampling design (ZOIs, land-use strata, and site distribution) is configured to capture spatial variability across CAZ, enabling downstream mapping of carbon stocks.
  - Remote sensing informed site selection; field data integrated with GIS-ready datasets (GPS coordinates, land-use types, slope, altitude) for GIS analyses and carbon stock mapping.
  - Data archiving pipeline (field sheets, Excel, photos, EIDC) supports reproducible GIS data layers and future data sharing.
  - Carbon stock surfaces depend on multi-pool measurements (AGB, BGB, litter, DW, SOC) and depth-specific SOC (SOC30, SOC100), enabling detailed GIS-based carbon budgeting and scenario analysis.