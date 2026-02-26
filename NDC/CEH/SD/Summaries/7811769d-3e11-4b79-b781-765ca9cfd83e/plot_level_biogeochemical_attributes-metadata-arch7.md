# Dataset describing sites, plots, transects and soil measurements in Kielder Forest

- Overview
  - Unique site in Kielder Forest defined by common stand type and topography (refer to Fig 1).
  - Within each site, individual plots are defined; each plot is 50 m².
  - Within each plot, two 10 m transects span the plot perpendicularly, from which soil cores are taken.
  - Disturbance is recorded as a categorical windthrow disturbance score along transects.

- Data structure and hierarchy
  - site: A unique site within Kielder Forest, characterized by stand type and topography.
  - plot: An area within a site (50 m²) with a disturbance score.
  - transect: A 10 m line spanning a plot; two transects per plot (perpendicular).
  - disturbance_score: Categorical rating of windthrow disturbance along transects (Fig 2 reference).

- Variables and measurements
  - nitrogen: Soil nitrogen content, in percent (%).
  - carbon: Soil carbon content, in percent (%).
  - Soil.Moisture: Gravimetric soil moisture, in percent (%).
  - root_mg_per_cm3: Dry root mass in a 10 x 10 x 20 cm soil core, in milligrams (mg).
  - Latitude: Latitude of sample collection.
  - Longitude: Longitude of sample collection.

- Sampling and spatial design
  - Sampling along transects occurs every 20 m along a transect typically spanning ~200–400 m across a known intact and windthrown forest stand (as per Fig 2).
  - Each plot contains two transects to capture spatial variability within the stand.

- Figures and interpretation
  - Fig 1: Definition of sites and plots in this experiment (used to anchor GIS layers for site and plot boundaries).
  - Fig 2: Decision tree for assessing degree of disturbance along transects (used to derive standardized disturbance scores and comparability across plots).

- GIS-focused considerations
  - Data can be represented as layered spatial features: sites (polygons), plots (polygons within sites), transects (lines within plots), and sample points (points along transects with measurements).
  - Attributes to map and analyze: disturbance_score, nitrogen, carbon, Soil.Moisture, root_mg_per_cm3, and coordinates (Latitude/Longitude).
  - Suitable for exploring spatial patterns of soil properties and disturbance (windthrow) across forest structure.

- Potential uses for policy and public-facing GIS products
  - Visualize spatial distribution of soil properties and disturbance across Kielder Forest.
  - Compare intact vs windthrown stands and assess recovery trajectories or management needs.
  - Support decision-making on habitat restoration, monitoring, and forest resilience.

- Data quality and limitations (GIS perspective)
  - Data originate from multiple spatial scales and resolutions (site, plot, transect, point-level measurements); standardization of units and coordinate references is important.
  - Disturbance scores are categorical and may require clear legend and consistency checks (Fig 2 guidance).
  - Spatial sampling along transects assumes representative coverage within each plot; ensure transect placement is consistently recorded for reproducibility.