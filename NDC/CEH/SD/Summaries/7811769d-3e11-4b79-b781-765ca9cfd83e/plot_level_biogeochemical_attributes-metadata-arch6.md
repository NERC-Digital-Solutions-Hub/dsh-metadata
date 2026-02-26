# site, Description = Unique site in Kielder Forest, defined by common stand type and topography (see Fig 1)

## Overview
- Describes a forest disturbance sampling dataset from Kielder Forest, spanning unique sites, plots within sites, and transects used to collect soil and disturbance data across an intact and windthrown stand.

## Data structure and scope
- Hierarchy:
  - site: Unique site in Kielder Forest, defined by stand type and topography (see Fig 1)
  - plot: Within a site; each plot measured as 50 m2 (defined in Fig 1)
  - transect: Ten-metre transect spanning a plot; two transects per plot placed perpendicular to each other (from which soil cores are taken) (Fig 1)
- Data elements collected per transect/plot:
  - disturbance_score: Categorical windthrow disturbance score (Fig 2 describes assessment)
  - nitrogen: Soil nitrogen content (%)
  - carbon: Soil carbon content (%)
  - Soil.Moisture: Gravimetric soil moisture (%)
  - root_mg_per_cm3: Dry root mass in a 10 x 10 x 20 cm soil core (mg)
  - Latitude, Longitude: Coordinates of sample collection

## Sampling design and methodology
- Fig 1 defines the spatial definitions of sites and plots.
- Each plot is 50 m2.
- For each plot, two 10 m transects are used, oriented perpendicularly, from which soil cores are taken.
- Disturbance assessment is conducted every 20 m along a transect that spans roughly 200–400 m across a known intact and windthrown stand (as described in Fig 2).

## Variables and units
- disturbance_score: Categorical score (windthrow disturbance)
- nitrogen: percent (%) soil nitrogen content
- carbon: percent (%) soil carbon content
- Soil.Moisture: percent (%) gravimetric soil moisture
- root_mg_per_cm3: milligrams per cubic centimeter (mg) dry root mass
- Latitude, Longitude: geographic coordinates (units not specified beyond latitude/longitude)

## Data use and potential products
- Enable exploration of disturbance gradients and soil properties across sites and plots.
- Create self-service data products such as dashboards, reports, charts, and maps to compare intact vs windthrown stands.
- Facilitate spatial analysis of disturbance alongside soil chemistry and root metrics; potential to aggregate by site or plot and to cross-reference with topography (as defined in Fig 1).

## notes and references
- Key figures:
  - Fig 1: Definition of sites and plots in this experiment
  - Fig 2: Decision tree for assessing degree of disturbance every 20 m along a ~200–400 m transect spanning a known intact and windthrown forest stand
- The document structure emphasizes a hierarchical sampling design (site → plot → transect) with standardized measurements along transects for disturbance and soil properties.