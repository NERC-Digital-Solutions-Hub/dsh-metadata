# ESPA p4ges PROJECT Work Package Carbon (WP4-Carbon) (Manual n°1)

- Context and aim
  - The p4ges project in Madagascar investigates paying for global ecosystem services to reduce poverty, focusing on carbon stocks within the CAZ (Ankeniheny Zahamena Forest Corridor) in eastern Madagascar.
  - WP4 performs carbon stock assessments across five IPCC pools: Aboveground biomass (AGB), Belowground biomass (BGB), litter, dead wood (DW), and soil organic carbon (SOC).
  - The manual documents the first step of carbon quantification design, focusing on AGB, litter, deadwood, and soil surveys, with datasets archived at the Environmental Information Data Centre (EIDC).

- Study design and data architecture
  - Four Zones of Interest (ZOIs) selected to represent CAZ conditions: Lakato, Andasibe, Anjahamana/Ambalarondra, Didy.
  - Land uses characterized as: Closed canopy, Tree fallow, Shrub fallow, Tany maty (degraded land); reforestation added from NGO/community input.
  - Field sites defined per ZOI to capture variability; 16 plots per ZOI (4 land uses × 4 replicates) with extra plots for carbon stock variability (WP4); totals: ZOI1 had 28 sites, ZOI2 had 48, ZOI3 had 28, ZOI4 had 28.
  - Site selection criteria include slope (<45 degrees), patch-centered transects to avoid edge effects, minimum plot size (≥120 m × 120 m), avoidance of disturbances (e.g., mining), non-crossing streams, and ≥500 m between sites.
  - Remote sensing used for initial site locations; field reconnaissance confirms suitability and land-use type.

- Field data collection and site setup
  - General field design: plot with a 5 m radius used for C pool surveys; degraded land uses also sampled with this method.
  - Forest inventory and biomass sampling in closed canopy and fallows:
    - Four subplots per site within circular area.
    - Saplings (DBH < 5 cm, H > 1.30 m) counted; 5 randomly selected species weighed and sampled.
    - Trees in concentric circular zones (2 m, 5 m, 10 m, 20 m radii) measured for DBH, height, and species names; standing and down(dead) wood recorded; wood density categorized as Sound, Intermediate, or Rotten.
    - Lying dead wood measured along a 100 m transect; diameters and densities recorded.
    - Direct AGB: 54 trees across four species felled and weighed; components (trunk, branches, leaves) weighed; moisture samples collected.
    - Understorey, litter, and root mat: 25 cm × 25 cm quadrat for litter/root mat; 1 m × 1 m quadrat for understorey; samples weighed and lab-subset collected.
    - Root description in central plot: 1 m² pit to classify roots by diameter (<2 mm; 2–10 mm; >10 mm) and depth distribution.
    - Percent cover estimated for indicator species (Braun-Blanquet scale) within a 5 m radius around sapling inventory.
  - Degraded land (tany maty) sampling: no large trees; biomass, root mat, litter, understorey sampled per the same design; soil sampling and soil profile description still conducted.
  - Soil sampling and profiling:
    - Subplots in each site used for soil sampling at 0–100 cm in 10 cm increments.
    - Bulk density measured with 8.1 cm diameter, 10 cm high cylinders (depths 0–10, 10–20, 20–30, 50–60, 80–90 cm).
    - Soil profile described in a dedicated 1.30 m pit (color, texture, structure, root depth, porosity).
    - Two methods: soil carbon via auger (0–100 cm) and bulk density via cylinders (0–90 cm).
  - Administrative and field readiness:
    - Permits, mission orders, insurances, data collection sheets, equipment, sample bags, and labeling prepared before field work.
    - Data sheets cover site characteristics, inventory, coverage (Braun-Blanquet), sapling/litter/root sampling, and soil profiles.

- Data handling, storage, and data workflow
  - Field forms and data are scanned and stored; data entered in Excel; photos organized and stored in Bangor University data center.
  - All collected data organized into data series and archived at the Environmental Information Data Centre (EIDC) for long-term storage and valorization.
  - Samples sent to LRI laboratory; linked to field data with lab numbers and provenance; stored at room temperature and air-dried; correlation checks between field and lab records maintained.
  - Metadata and datasets prepared to support subsequent carbon stock calculations across all pools; data as part of ESPA WP4 data for dissemination.

- Laboratory analyses and data processing
  - Biomass analysis:
    - Drying of biomass samples (air then oven at 75°C) to constant weight; moisture corrections applied.
    - Wood Specific Gravity (WSG) determined (referenced in Manual n°4).
  - Soil analyses:
    - Preparation includes air-drying, sieving to 2 mm, and grinding to 200 microns for analysis.
    - Moisture content via 105°C drying.
    - Walkley-Black method for initial soil organic carbon (as calibration reference).
    - Mid Infrared Spectroscopy (MIRS) for rapid SOC prediction, calibrated against Walkley-Black results.
    - Carbon stable isotope analysis (δ13C) on selected samples (LRI-Montpellier) to inform land-use type and carbon dynamics; data archived at EIDC.

- Calculation approaches and data products
  - Aboveground biomass (AGB) and carbon stocks:
    - Allometry-based estimates per tree (using equations from Chave et al., Vielledent et al., etc.) to derive kg tree−1; plot-level biomass (Mg ha−1) scaled from tree densities and area; conversion to carbon stock (Mg C ha−1) using established factors.
    - Biomass for lower strata (understorey, litter) quantified from Quadrat weights; carbon stock calculated using a Brown (2002) coefficient (0.5) to convert biomass to carbon.
  - Dead wood and litter:
    - Lying dead wood biomass from volume calculations and wood density categories; standing dead wood biomass via standard volume–density equations; sums per plot.
  - Soil carbon stock:
    - SOC stocks calculated per layer using bulk density, carbon concentration, coarse fraction correction, and layer thickness; SOC30 and SOC100 computed to reflect depth-specific stocks and land-use changes.
  - Data publication and references:
    - Data linked to main publications and reports; outputs include national-scale soil organic carbon mapping and analyses on land-use change impacts on carbon stocks.

- Data assets, governance, and accessibility
  - Primary data repositories:
    - Environmental Information Data Centre (EIDC) for long-term storage of field and lab data.
    - Bangor University data center for photos and project-wide data assets.
  - Metadata quality, discoverability, and reuse:
    - Comprehensive field and lab metadata collected (site characteristics, land-use history, protocols, depth intervals, soil analyses).
    - Clear traceability between field samples and laboratory analyses (lab numbers, provenance).
  - System thinking and coordination:
    - Cross-WP collaboration (Carbon, Hydrology, Biodiversity) to define Zones of Interest and ensure representative sampling across land-use types.
    - Data products designed to support broader carbon stock assessments and policy-relevant analyses (e.g., land-use change effects, national SOC mapping).

- Key takeaways for data leaders
  - Robust sampling design that captures within- and between-zone variability across multiple land uses and depths.
  - Integrated data workflow from field data collection to lab analyses and centralized archival in a dedicated data center with clear metadata.
  - Use of standard allometric and carbon conversion methods to translate measurements into comparable carbon stock metrics per plot and per hectare.
  - Emphasis on data discoverability, reproducibility, and long-term stewardship through established repositories (EIDC, Bangor) and cross-WP coordination.
  - Documentation and planning for data publication, with explicit references to methodological foundations and data provenance.