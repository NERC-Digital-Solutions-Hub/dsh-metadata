# Supporting documentation for Kampala Flood Extents

- Purpose and scope
  - Documents the creation of flood extent data for Kampala district using hydrodynamic modelling and rainfall scenarios.
  - Utilizes a 5m Digital Elevation Model (DEM) to simulate flood depths and extents; DEM provided by Makerere University.
  - Incorporates infiltration effects within green areas using spatial data from Makerere University.
  - Provides extents defined by depth thresholds and multiple rainfall depths/durations for decision-support and risk assessment.

- Modelling and processing workflow
  - 2D finite-volume hydrodynamic model used to simulate rainfall events.
  - Maximum water depths converted to flood extents using defined thresholds (in meters).
  - Extents simplified with Douglas-Peucker algorithm (tolerance 5m) to reduce file size.

- Data assets and structure
  - GeoPackage containing polygons describing flood extents above a threshold for each rainfall depth and duration.
  - Fields (with units):
    - Threshold: meters (m) – the depth threshold used to define flooded areas from the model grid.
    - Rainfall: millimeters (mm) – total rainfall for the event.
    - Duration: seconds (s) – duration of the rainfall event.
  - Data described and organized to enable retrieval of extents across combinations of rainfall depth and duration.

- Accessibility and reuse
  - Web view for the extents: http://shear.ncl.ac.uk/flood
  - Source code available for download: Zenodo DOI 10.5281/zenodo.3949902
  - Modelling framework reference: Glenis, Kutija & Kilsby (2018) describing a fully hydrodynamic urban flood modelling system that accounts for buildings, green space, and interventions.

- Implications for data governance and use (Data Leaders perspective)
  - A single, discoverable data asset that integrates DEM, infiltration assumptions, and multiple rainfall scenarios into polygon extents.
  - Provides transparent provenance via published methodology and an accessible codebase.
  - Supports policy, planning, and risk management activities through explicit thresholds and scenario-based extents.
  - Emphasizes data accessibility and potential for reuse in wider urban flood risk applications.