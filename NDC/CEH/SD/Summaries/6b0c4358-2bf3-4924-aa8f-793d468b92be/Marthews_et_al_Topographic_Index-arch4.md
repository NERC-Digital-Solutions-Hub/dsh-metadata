# A high-resolution global dataset of topographic index

- Global, high-resolution dataset of topographic index for large-scale hydrological modelling
- Source and format: ga2_Global_15s_netcdf.zip containing a single NetCDF file (ga2.nc) that conforms to Climate and Forecast (CF) conventions
- Variable: only the topographic index value; calculated with the GA2 program using a global DEM, with minor modifications
- Resolution and size: 15 arc-second global layer, approximately 11.0 GB
- Spatial coverage: global, with defined corner coordinates (upper left, lower left, upper right, lower right) and center coordinates provided
- Intended use: topographic ancillary data for the TOPMODEL routing option within the JULES land surface model
- Comparability: directly comparable to the HYDRO1k topographic index at 30 arc-second resolution

- Data structure and access
  - One GIS data layer (ga2.nc) included in the archive; file is zipped as ga2_Global_15s_netcdf.zip
  - Corner coordinates and center provided to aid spatial context and integration into workflows
- Data quality and standards
  - Metadata notes indicate the variable is the topographic index, derived from a standard algorithm with minor global DEM adjustments
  - Alignment with CF conventions supports interoperability and discoverability across platforms
- Implications for Data Leaders
  - Supports comprehensive data-system thinking: a globally consistent, single-variable dataset that can underpin larger hydrological modelling workflows
  - Valuable for cross-team collaboration and co-ownership of model inputs, given its relevance to policy and modelling outputs
  - Requires substantial storage, processing power, and careful data handling due to its 11.0 GB size
  - Directly supports interoperability with existing data products (e.g., HYDRO1k) for validation and benchmarking
  - Clear use-case in teaching, planning, and implementation of TOPMODEL-based routing within JULES, enabling more robust data-driven decision-making