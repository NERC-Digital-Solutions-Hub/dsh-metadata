# HYDRUS-1D Simulations of Soil Moisture and Metal Transport in a Rice Lysimeter

- Overview
  - One-dimensional HYDRUS-1D simulations of water and solute movement in variably-saturated media.
  - 90-day simulations for a 100 cm deep lysimeter planted with rice.
  - Input boundary conditions and setup data are provided in HydrusInputData.csv.
  - Outputs cover the entire soil column and selected nodes, enabling both bulk and site-specific analyses.

- Simulation setup and data captured
  - Soil column discretized into 101 nodes (0–100 cm depth).
  - Variables recorded for the full column: soil moisture (cm3/cm3), pressure head (cm), dissolved metal concentration (mg/cm3), and sorbed metal concentration (ppm).
  - Temporal sampling:
    - Whole-column data recorded every 9 days, stored in HydrusOutputDay0.csv through HydrusOutputDay90.csv.
    - Very fine temporal resolution data recorded for nodes 5, 11, 22, and 100, stored in HydrusOutputNode5.csv, HydrusOutputNode11.csv, HydrusOutputNode22.csv, and HydrusOutputNode100.csv respectively.

- File and unit details
  - Output files: HydrusOutputDay0.csv, HydrusOutputDay9.csv, HydrusOutputDay18.csv, HydrusOutputDay27.csv, HydrusOutputDay36.csv, HydrusOutputDay45.csv, HydrusOutputDay54.csv, HydrusOutputDay63.csv, HydrusOutputDay72.csv, HydrusOutputDay81.csv, HydrusOutputDay90.csv; node-specific: HydrusOutputNode5.csv, HydrusOutputNode11.csv, HydrusOutputNode22.csv, HydrusOutputNode100.csv.
  - Units:
    - Soil moisture: cm3/cm3
    - Pressure head: cm
    - Dissolved metal concentration: mg/cm3
    - Sorbed metal concentration: ppm

- Context and references
  - Software and methodology: HYDRUS-1D (Simunek et al., 2003; 2005) for one-dimensional movement of water, heat, and solutes in variably-saturated media.
  - Key references:
    - Simunek, J., Jarvis, N.J., van Genuchten, M.Th., Gardenas, A., 2003. Review and comparison of models for describing non-equilibrium and preferential flow and transport in the vadose zone. J. Hydrol. 272, 14-35.
    - Simunek, J., van Genuchten, M.Th., Sejna, M., 2005. The HYDRUS-1D software package for simulating the one-dimensional movement of water, heat, and multiple solutes in variably-saturated media. Version 3.0.

- Relevance to monitoring frameworks
  - Demonstrates structured generation of environmental monitoring data, with clear input and multi-resolution output files suitable for model validation, scenario analysis, and policy evaluation.
  - Highlights the importance of documenting boundary conditions, discretization, and variable definitions to enable reuse in monitoring frameworks.
  - Illustrates data richness (column-wide and node-specific temporal detail) that can support dashboards, reports, and decision-support tools.

- Potential considerations for data governance and reuse
  - Metadata clarity: ensure definitions of variables, units, and file naming conventions are explicit to facilitate data sharing and reuse.
  - Data accessibility: consider making input and output datasets publicly accessible with accompanying metadata to reduce barriers.
  - Data quality and provenance: maintain records of boundary conditions, calibration, and software version to support traceability and reproducibility.