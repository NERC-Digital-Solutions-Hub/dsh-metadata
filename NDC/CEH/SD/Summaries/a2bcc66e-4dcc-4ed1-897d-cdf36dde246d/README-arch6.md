# Satellite-derived geomorphic river mobility for ten catchments in the Philippines, 1988-2019

- What this collection contains
  - Codes and data linked to the study of satellite-derived geomorphic river mobility across ten catchments in the Philippines (1988–2019).
  - A worked example for the Abulug catchment, demonstrating:
    - GEE code to generate binary active channel images
    - MATLAB code to calculate per-pixel locational probabilities
    - MATLAB code to calculate and plot along-valley locational probabilities using TopoToolbox 2.4
  - Processed data products: raster images of per-pixel locational probabilities for the analysed catchments, intended for GIS visualization.

- How this supports data work
  - Provides a reproducible workflow combining code and outputs to explore river mobility data.
  - Enables self-serve analysis and GIS visualization through ready-to-use raster outputs.
  - Facilitates cross-catchment comparisons and potential adaptation to additional catchments.

- Data formats and tools required
  - GEE (Google Earth Engine) scripts for binary active channel generation
  - MATLAB scripts for probability calculations and plotting
  - TopoToolbox 2.4 for along-valley probability plotting
  - Raster images for GIS visualization

- Practical considerations for data support
  - Clear, example-driven structure (01_Abulug_Example) to help users understand and reproduce methods.
  - 02_Processed_Locational_Probabilities provides ready-made outputs to accelerate data exploration and application in GIS.