# HYDRUS-1D simulations of soil moisture and metal transport in a rice lysimeter

- Objective and scope
  - Simulate soil moisture and metal concentration in the root zone of a 100 cm deep lysimeter planted with rice using the HYDRUS-1D one-dimensional finite element model.
  - Run for 90 days to study temporal dynamics.

- Data produced and file structure
  - Boundary conditions and input data are provided in HydrusInputData.csv.
  - Column-wide outputs saved every 9 days in HydrusOutputDay0.csv through HydrusOutputDay90.csv, including:
    - Soil moisture (cm3/cm3)
    - Pressure head (cm)
    - Dissolved metal concentration (mg/cm3)
    - Sorbed metal concentration (ppm)
  - High-temporal-resolution time series for specific nodes saved in:
    - HydrusOutputNode5.csv
    - HydrusOutputNode11.csv
    - HydrusOutputNode22.csv
    - HydrusOutputNode100.csv
  - The soil column is discretized into 101 nodes (0–100 cm).

- Spatial and temporal sampling
  - Spatial: 0 to 100 cm depth, 101 nodes.
  - Temporal: daily boundary/column data every 9 days; node-specific time series at very fine temporal resolution for selected nodes (5, 11, 22, 100).

- Variables and units
  - Soil moisture: cm3/cm3
  - Pressure head: cm
  - Dissolved metal concentration: mg/cm3
  - Sorbed metal concentration: ppm
  - Units definitions provided within the description.

- Software and provenance
  - Simulation tool: HYDRUS-1D (one-dimensional movement of water, heat, and multiple solutes in variably-saturated media).
  - Software reference: Simunek et al., 2003; Simunek et al., 2005; Version 3.0.
  - Documentation and citations included to support reproducibility.

- Implications for data strategy (Data Leaders perspective)
  - Data system view
    - Demonstrates end-to-end data generation: input boundary conditions, full-column outputs, and node-specific high-resolution data.
    - Clear separation of dataset types by file (input vs. day-wise outputs vs. node-specific outputs).
  - Data discoverability and metadata
    - Names and contents of files are explicit (HydrusInputData.csv, HydrusOutputDay*.csv, HydrusOutputNode*.csv) aiding discoverability.
    - Variable definitions and units are explicitly stated, supporting proper interpretation.
  - Data quality and standards
    - Provenance is documented via software references and authors.
    - Reproducibility supported by detailed discretization (101 nodes) and explicit output definitions.
    - Consider formal metadata for dataset-level schema, versioning, and methodological notes to facilitate reuse.
  - Collaboration and reuse
    - Data could be shared with partners studying soil-plant-atmosphere interactions or contaminant transport under rice cultivation.
    - Potential to integrate with broader data systems (catalogs, metadata standards) for cross-study comparisons and scaling to other depths, crops, or conditions.

- References
  - Simunek, J.; Jarvis, N.J.; van Genuchten, M.Th.; Gardenas, A. (2003). Review and comparison of models for describing non-equilibrium and preferential flow and transport in the vadose zone. J. Hydrol.
  - Simunek, J.; van Genuchten, M.Th.; Sejna, M. (2005). The HYDRUS-1D software package for simulating the one-dimensional movement of water, heat, and multiple solutes in variably-saturated media. Version 3.0. Hydrus-1D Software Series.