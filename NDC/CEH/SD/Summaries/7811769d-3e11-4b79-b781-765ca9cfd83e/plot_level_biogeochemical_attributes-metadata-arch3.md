# Definition of sites and plots in this experiment

## Overview
- Describes a structured field experiment in Kielder Forest aimed at assessing disturbance (windthrow) and soil properties across defined sites and plots.
- Each site is unique and defined by common stand type and topography (as per Fig 1).

## Sampling design
- Plot size: 50 m2 per plot.
- Transects: 2 per plot, each 10 m long, located perpendicular to each other.
- Disturbance assessment: Every 20 m along a ~200–400 m transect spanning a known intact and windthrown stand (as per Fig 2).
- Plot placement and transect layout enable comparison between intact and windthrown forest areas.

## Measurements and variables
- disturbance_score: Categorical windthrow disturbance score (from transects).
- nitrogen: Soil nitrogen content (%).
- carbon: Soil carbon content (%).
- Soil.Moisture: Gravimetric soil moisture (%).
- root_mg_per_cm3: Dry root mass in a 10 x 10 x 20 cm soil core (mg).
- Latitude and Longitude: Geographic coordinates for sample location.
- All measurements are tied to a defined site/plot with standardized descriptors (see Fig 1 for site/plot definitions).

## Data structure and definitions
- site: Unique site in Kielder Forest, defined by stand type and topography.
- plot: Individual 50 m2 area within a site.
- transect: 10 m line spanning a plot, with two orthogonal transects per plot.
- Disturbance scoring and soil measurements are associated with transect locations along the transects.

## Figures (context for implementation)
- Fig 1: Definition of sites and plots in this experiment.
- Fig 2: Decision tree for assessing degree of disturbance every 20 m along a transect across intact and windthrown stands.

## Relevance for monitoring frameworks
- Provides a standardized, geo-referenced data collection protocol suitable for monitoring environmental health indicators (disturbance, soil nutrients, carbon, moisture, root biomass).
- Enables cross-site comparability and temporal tracking if repeated measurements are conducted.
- Facilitates clear reporting through defined variables and units, supporting dashboards and formal assessments.

## Data governance and practical considerations
- Metadata clarity: Units are specified for key variables (percentages, mg, coordinates), aiding data verification.
- Data sharing and openness: Underlying data should be publicly accessible where appropriate; consistency of metadata is crucial to enable reuse.
- Data quality: Structure supports methodical quality assurance, transformation, and analysis; explicit definitions help reduce misinterpretation.
- Potential challenges (aligned with monitoring frameworks): achieving timely data access, avoiding data silos, ensuring up-to-date metadata, and communicating complex disturbance findings effectively.