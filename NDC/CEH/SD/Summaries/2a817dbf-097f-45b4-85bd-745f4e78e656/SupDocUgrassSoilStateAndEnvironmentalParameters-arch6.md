# U-GRASS (Understanding and enhancing soil ecosystem services and resilience in UK grass and croplands) UK grasslands: Soil state and environmental parameters across geo linked sampling locations

- Scope and purpose
  - Data describe soil state and environmental parameters from 32 UK grassland sites with contrasting land uses (low vs high intensity) sampled across winter–spring 2015–2016.
  - Aimed to understand how soil function changes under different management and climatic scenarios; part of the NERC U-GRASS project.

- Sample collection and provenance
  - 32 sites across the UK; land-use contrasts near each other.
  - Soil cores (15x5 cm) collected along 100 m transects with sampling every 25 m, yielding 5 paired replicates per site.
  - Samples collected Nov 2015–Feb 2016 and stored frozen at -20°C prior to analysis.

- Analyses and laboratories
  - Analyses performed for: total nitrogen (N), total carbon (C), total organic carbon (OC), total phosphorus (P), soil pH, soil moisture, loss on ignition (LOI), particle size (sand/silt/clay), FT-IR spectra, and bulk density.
  - Chemical/physical analyses conducted by CEH Lancaster, CEH Wallingford, and NRML (as listed in the executive summary) with results compiled into an Excel sheet and exported to CSV for deposition into the EIDC.

- Key data content (parameters)
  - Geographic and basic identifiers: unique Id, latitude, longitude.
  - Soil chemical/physical properties: organic_C, total_C, total_N, total_P, pH, soil_moisture, LOI, sand, silt, clay, bulk_density (with appropriate units).
  - FT-IR spectroscopy indicators: clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR (area under specified MIR-ATR peaks).
  - Data units and descriptions are provided per variable (e.g., percentages for C/N components, mg/kg for P, pH units, etc.).

- Data structure and format
  - File type: flat CSV.
  - Size: 450 data rows and 19 columns.
  - Columns include: Id, latitude, longitude, organic_C, total_C, total_N, total_P, pH, soil_moisture, LOI, sand, silt, clay, clay1_IR, clay2_IR, clay_quality_IR, sat_C_IR, calc_IR, bulk_density (with descriptive notes for each).

- Associated data product
  - Analysis outputs file: UgrassSoilStateAndEnvironmentalParameters.csv
  - Deposition: data exported to the Environmental Information Data Centre (EIDC).

- Context and broader relevance
  - Addresses soil security and ecosystem services, highlighting relationships among soil biodiversity, properties, and functionality under varying management and climate contexts.
  - Provides a geo-referenced, multi-parameter soil dataset suitable for cross-site comparisons, modeling of soil functions, and informing land-management decisions.