# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

## Data Overview
- Dataset pyc.csv contains measurements of soil pyrogenic carbon (PyC), the ratio of PyC to bulk carbon (Cpyc_Cbulk), and organic carbon (OC) in a soil fertility gradient across the Amazon Basin.
- Samples come from old-growth forests: 49 forest plots and 395 soil samples in total.
- Of the 49 plots, 37 had prior sampling for total organic carbon (TOC) under a prior protocol; 12 plots were newly sampled in 2017.
- Funded by NERC (Do past fires explain current carbon dynamics of Amazonian forests?), CAPES Brazil, CNPq, PPBio, FAPEMAT, and CAPES/Brazil postdoctoral fellowships.
- Related publications utilizing this dataset include studies in Frontiers in Forests and Global Change (2022) and Geoderma (2017).

## Data Content and Structure
- Recorded variables (columns in pyc.csv):
  - Plot_number, Latitude, Longitude
  - depth_range (sampling depth interval)
  - Cpyc (PyC concentration (%))
  - Cpyc_Cbulk (ratio of PyC to bulk carbon, %)
  - OC (organic carbon, %)
  - forests_status (old-growth or disturbed)
  - Rep (replications of sampling within the same plot/depth)
- Units:
  - Cpyc and OC expressed as percent of the sample
  - Cpyc_Cbulk expressed as a percent ratio
- Depth coverage spans multiple intervals from 0–5 cm to 150–200 cm
- All samples are composites by depth interval per plot

## Collection Methods
- Sampling tool: soil auger.
- Plot design:
  - Plots ≥ 1 ha: at least five sampling locations (four corners + centre)
  - Plots < 1 ha: three locations (two corners + centre)
- Depths: samples collected to 2 m depth, with the majority in 0–5, 5–10, 10–20, 20–30, 30–50, 50–100, 100–150, 150–200 cm intervals
- For each plot, samples were composited by depth interval to yield one sample per depth range per plot
- PyC quantification performed on air-dried, sieved samples at James Cook University using Hydrogen Pyrolysis (HyPy)

## Data Analysis and Quality Control
- PyC quantified via HyPy; TOC and OC measured for each sample
- PyC data corrected from %BC (black carbon) using equation 2 from Wurster et al. 2012
- Samples with failed runs or non-convergence were discarded and not included

## Nature of Data and Documentation
- Data file attached as pyc.csv
- Metadata fields include geographic coordinates, depth range, and sample status (old-growth vs disturbed)
- Detailed references linked to methods and prior work (HyPy technique; soils in Amazon forests; deep storage estimates)

## Provenance and References
- Primary methodological references:
  - Ascough et al. 2009: Hydropyrolysis (HyPy) for PyC quantification
  - Quesada et al. 2010: Variations in soil properties in Amazon forests
  - Wurster et al. 2012: Pyrogenic carbon quantification corrections
- Related publications using the dataset:
  - de Oliveira et al. 2022: Soil PyC in southern Amazonia
  - Koele et al. 2017: Amazon Basin forest PyC stocks (deep storage)

## Relevance for Data Leaders
- Demonstrates end-to-end data lifecycle: from field collection across multiple plots, through laboratory analysis and QC, to a shareable, well-structured CSV with clear metadata.
- Emphasizes data discoverability and usability:
  - Clear data model with explicit fields, units, and depth intervals
  - Composite sampling design and spatial metadata (Plot, Lat/Lon)
  - Documentation of methodologies (HyPy, TOC/OC measurements) and data corrections
- Highlights governance considerations:
  - Multiple funding sources and cross-institution collaboration
  - Documentation of data provenance and linkage to published research
  - QC practices (corrections, discarding failed runs) ensuring data reliability
- Useful for data strategy:
  - Enables integration with regional soil carbon datasets and broader carbon cycle analyses
  - Provides a model for managing data collected across varied field plots, depths, and years
  - Supports assessment of spatial and depth-related patterns in PyC for policy, climate, and ecological studies