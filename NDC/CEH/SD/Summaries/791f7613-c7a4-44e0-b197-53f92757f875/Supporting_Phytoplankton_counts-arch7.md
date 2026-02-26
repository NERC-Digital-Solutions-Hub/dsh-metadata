# BLEL_Phytoplankton_counts.csv

## Overview
- Supporting information for a dataset of phytoplankton counts from Blelham Tarn, collected in 2016 (weekly June–November).
- Focus: taxonomic identification and biovolume estimation of phytoplankton using map-derived data concepts for GIS-style analysis (species, depth, date, biovolume).

## Sampling and Laboratory workflow
- Water samples collected at metre intervals in the water column from 1 m to 6 m using the automated monitoring buoy (deepest point ~14.5 m).
- Preserved in Lugol's iodine; stored away from light and in a cool environment; checked for evaporation losses.
- Analysis performed with PlanktoMetriX (PMX) software for counting and measuring organisms (1–1000 μm) and computing biovolumes.
- A species database (2011–2015 data) used to identify species common to Blelham Tarn; 142 phytoplankton species identified.
- Biovolume calculations guided by CEN (2014) guidelines; geometric shapes and equations assigned per species.
- Count efficiency enhanced by subsampling from 1 m to identify present species; ten measurements per species used to derive average biovolumes for samples from 1–5 m.
- Counting performed with an Olympus BX45 inverted microscope in a Lund chamber; larger cells counted at x100, nanophytoplankton at x400.
- Counting protocol: random field selection; field-of-view-based counts; 50% visibility rule for borderline cells; initial limit of 100 individuals per count, beyond which counting stops.

## Data and Measurements (file contents)
- Sampling date.
- Depth in water column (1–6 m).
- Species name.
- AvX, AvY, AvZ: mean dimensions of phytoplankton in μm (x, y, z) based on 10 measurements.
- Biovolume: μm³/mL.

## Spatial and Temporal Context
- Location: Blelham Tarn, Lake District, NW England; figure indicates lake location and the monitoring buoy at the deepest point.
- Sampling regime: weekly from June to November 2016.
- Depth-specific data linked to a fixed bathymetric context for potential GIS mapping (depth layers, time series).

## Data Quality, Standards, and Limitations
- 142 phytoplankton species identified; biovolume estimates aligned with European standard guidelines (CEN 2014).
- Data derived from subsampling (1 m) to identify species; biovolume applied to samples 1–5 m.
- Counting capped at 100 individuals per field/observation to maintain manageability.
- Measurements are mean values from 10 observations per parameter.

## GIS/Codatapoints and Potential Uses
- Enables map-based visualization of species distribution and biovolume by depth and time.
- Suitable for integrating with bathymetric data and other lake health indicators.
- Supports temporal analyses (seasonal phytoplankton dynamics) and spatial analyses across depth strata.

## References
- CEN (2014) Water quality - Guidance on the estimation of phytoplankton biovolume.
- Lund, J. W. G. (1959) A Simple Counting Chamber for Nannoplankton.
- Ramsbottom, A. (1976) Depth charts of the Cumbrian lakes.
- Zohary, T., Shneor, M. and Hambright, D. (2016) PlanktoMetrix - a computerized system to support microscope counts and measurements of plankton.