# Dataset to examine spatial distribution of FIOs and their drivers in the standing waters of Hydroscapes within the UK

- Aim and scope
  - Investigates contamination of waterbodies with fecal indicator organisms (FIOs) and how their distribution is driven by landscape context and ecological factors.
  - Focuses on standing waters within a range of UK Hydroscapes, selected for contrasting landcover: Greater Glasgow (urban), Norfolk (agricultural), and Cumbria (upland/pastoral).
  - In each Hydroscape, 18 water bodies were chosen to cover gradients of size, productivity, hydrological connectivity, and ecological quality.

- Study areas and design
  - Three Hydroscapes: Greater Glasgow, Cumbria, Norfolk.
  - Sampling occurred in three seasons: spring, summer, and autumn.
  - Timeframe: 2016 or 2017.
  - Each Hydroscape contains 18 water bodies sampled, enabling spatial and temporal comparisons.

- FIO sampling and analysis
  - Sampling conducted 3 hours after sunrise to standardize UAV exposure timing.
  - Water samples were spatially dispersed within each lake from three discrete locations ~100 m apart.
  - At each location, three subsamples were collected (total of nine samples per water body per visit).
  - Overall, 1,278 unique samples were collected.

- Water sampling and laboratory processing
  - E. coli levels estimated from water samples taken ~30 cm below the surface using sterile 180 mL bottles.
  - Samples stored at 4°C and processed within 6 hours of collection.
  - Filtration: volumes of 100 mL, 10 mL, and 1 mL filtered through 0.45 μm membranes; filters placed on MLGA agar.
  - Incubation: plates incubated at 37°C and enumerated after 24 hours.
  - Results reported as colony-forming units (CFU) per 100 mL.
  - Additional measurement: heterotrophs CFU per 100 mL.

- Data structure and accompanying appendix
  - Dataset: Disease_distribution_data_UK_standing_waters.csv (field names and meanings provided in the Appendix).
  - Key fields include:
    - Hydroscape: landscape category (Greater Glasgow, Cumbria, Norfolk)
    - season: spring, summer, autumn
    - site: focal water body name
    - sample: code for the spatially discrete sample within a water body (1–3)
    - rep: sub-sample designation (a–c)
    - Ecoli: E. coli concentration (CFU per 100 mL)
    - Hetero: total heterotrophs concentration (CFU per 100 mL)

- Appendices and data documentation
  - Field name descriptions for Disease_distribution_data_UK_standing_waters.csv:
    - Hydroscape, Description = Landscape context (Greater Glasgow, Cumbria, Norfolk)
    - season, Description = Season of data collection (spring, summer, autumn)
    - site, Description = Water body name
    - sample, Description = Spatial sample code within the water body (1–3)
    - rep, Description = Sub-sample designation (a–c)
    - Ecoli, Description = E. coli concentration (CFU/100 mL)
    - Hetero, Description = Total heterotrophs concentration (CFU/100 mL)

- Relevance for data-driven analysis
  - Enables examination of spatial and temporal patterns in FIOs in relation to landscape type and ecological context.
  - Supports the development of correlations and predictive insights about drivers of water quality and potential risks to recreational users.