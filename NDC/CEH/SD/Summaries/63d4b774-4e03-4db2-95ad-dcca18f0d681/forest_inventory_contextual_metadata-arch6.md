# Tree census in permanent forest plots across the Amazon Basin

- Data overview
  - Dataset: tree_data.csv with Diameter at Breast Height (DBH) for 8,729 trees.
  - Location: 29 RAINFOR network forest plots across the Brazilian Amazon (Acre, Mato Grosso, Pará).
  - Forest type: terra-firme, nonflooded lowland forests.
  - Time frame: measurements collected between 2017 and 2019.

- Collection methods
  - Plot setup: plots sized 0.25 ha or 1 ha, established in prior campaigns.
  - Tree identification: each tree tagged; DBH measured with measuring tape.
  - New recruits: trees with DBH > 100 mm receive a new tag and are added to the census.
  - Dead trees: cause of death and decomposition stage recorded.
  - Living trees: state noted (health/condition).
  - Protocol: data coded according to the RAINFOR protocol; fieldwork details available at forestplots.net.

- Data flow and analysis
  - Post-fieldwork: field sheets digitised, error-checked, and uploaded to ForestPlots.net.
  - Integration: data compiled with previous censuses to analyze long-term forest dynamics.

- Context and funding
  - Part of research on whether past fires explain current carbon dynamics in Amazonian forests.
  - Supported by multiple Brazilian and international funding sources and projects (e.g., CAPES, CNPq, PELD programs, FORAMA, PPBio).

- Units
  - DBH is recorded in millimeters (mm).

- Quality control
  - Adheres to ForestPlots.net quality control protocol; DBH verified for each tree with corrective actions as needed.

- Data structure and access
  - CSV columns:
    - Plot_number: plot code
    - Tree_ID: tree code within the network
    - Tag_No: field tag code
    - DBH: diameter at breast height
    - Latitude, Longitude: geographic coordinates
  - Access: data available via ForestPlots.net; linked to long-term forest dynamics analyses.

- References
  - ForestPlots.net et al. Taking the pulse of Earth's tropical forests using networks of highly distributed plots. Biological Conservation 260 (2021) 108849. https://doi.org/10.1016/j.biocon.2020.108849

- Potential data products (Data Support perspective)
  - Self-serve dashboards or pivot tables to explore DBH distributions, recruitment, mortality, and growth over time.
  - Longitudinal analyses across plots to assess carbon dynamics and responses to fire history.
  - Spatial analyses integrating coordinates for regional pattern exploration.