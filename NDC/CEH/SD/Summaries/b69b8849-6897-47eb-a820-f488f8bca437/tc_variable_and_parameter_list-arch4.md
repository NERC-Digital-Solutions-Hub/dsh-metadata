# PLOT-SCALE  SIMULATIONS  WITH  MAIN-FRAME

- A comprehensive data dictionary for a plot-scale ecological/s biogeochemistry model configured to run on a main-frame system.
- Presents an extensive set of variables across multiple biological and physical domains, including vegetation structure, carbon and nutrient pools, soil processes, water and energy balance, and environmental drivers.
- Variables are described with units, data types (e.g., time series, scalar, assigned/internal parameters), and detailed descriptions that cover per Crown and per Plant Functional Type (PFT) scales.
- Distinguishes inputs (Input Time series, Assigned Parameters, Internal Parameters) from outputs (e.g., Net Ecosystem Exchange, Net Primary Production, NDVI, NPPI integrals).
- Notes several special statuses, such as:
  - Not active (e.g., Axyl_H, Axyl_L; some leaf/wood processes)
  - Wrong or deprecated entries (e.g., CK2 (wrong))
  - Internal/elaborated parameters (e.g., CaseRoot, OPT_EnvLimitGrowth, OPT_SoilBiogeochemistry)
- Includes time-resolved data at hourly and daily resolutions, with per-Crown and per-PFT segmentation, as well as aggregated ecosystem-wide outputs.
- Contains input drivers for atmosphere, weather, deposition, fertilization, and land-use (e.g., Ca CO2, Date/time, Precipitation, PAR, DepN, FertN, Upl) to drive simulations.
- Provides a broad set of soil, vegetation, and biogeochemical parameters (e.g., LAI, NPP_H/NPP_L, B_H/B_L carbon pools, mineralization, nutrient uptakes, water potentials, hydraulic conductivities, and respiration terms).
- The document emphasizes the model’s data-rich nature, provenance, and the need for careful data governance to enable reproducibility and interoperability across networks and analyses.