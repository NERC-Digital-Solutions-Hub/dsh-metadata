# Soil pyrogenic carbon (PyC) data from across the Amazon Basin

## Data scope and purpose
- Dataset (pyc.csv) contains measurements of soil pyrogenic carbon (PyC), the ratio of PyC to bulk organic carbon (Cpyc_Cbulk), and organic carbon (OC) across a soil fertility gradient in old-growth forests of the Amazon Basin.
- Totals: 49 forest plots sampled (395 soil samples in total); 37 plots previously sampled (TOC data), 12 plots sampled in 2017.
- Data collected under specified funding and collaboration networks; linked to published research on Amazon soil carbon dynamics.

## Collection methods and design
- Sampling approach:
  - Plots ≥ 1 ha: minimum of five locations (four corners and center).
  - Plots < 1 ha: three locations (two corners and center).
  - Depth to 2 m, with samples allocated into discrete depth intervals.
  - Composite samples created per depth interval per plot.
- Field protocol:
  - Soil collected with an auger.
  - Depth intervals typically include 0–5, 5–10, 10–20, 20–30, 30–50, 50–100, 100–150, 150–200 cm.
- Sample processing:
  - Air-dried and sieved; PyC quantified using hydropyrolysis (HyPy) technique.
  - TOC and OC measured; PyC fraction quantified within TOC.
- Data correction:
  - Cpyc correct ed from %Bulk Carbon using equation from Wurster et al. (2012).
  - Failed runs discarded (no convergence).

## Measurements and units
- Cpyc: Pyrogenic carbon concentration as a percentage of the sample.
- OC: Organic carbon percentage of the sample (non-pyrogenic fraction).
- Cpyc_Cbulk: Ratio of PyC to bulk carbon, expressed as a percentage.
- All values reported as percentages where applicable.

## Data structure and fields
- File: pyc.csv
- Columns:
  - Plot_number: plot code number
  - Latitude: geographic latitude
  - Longitude: geographic longitude
  - depth_range: depth interval where the sample was taken
  - Cpyc: PyC concentration (%)
  - Cpyc_Cbulk: PyC to bulk carbon ratio (%)
  - OC: Organic carbon (%)
  - forests_status: forest type (old-growth or disturbed)
  - Rep: number of replicates for the same plot and depth range

## Quality control and data quality
- PyC percentage corrected for BC following Wurster et al. (2012).
- Non-converging or failed runs removed from the dataset.

## Context, usage, and references
- Data linked to peer-reviewed work:
  - de Oliveira et al. (2022) Frontiers in Forests and Global Change
  - Koele et al. (2017) Geoderma
- References for methods included in the dataset documentation:
  - Ascough et al. (2009) Hydropyrolysis for PyC quantification
  - Quesada et al. (2010) soil properties in Amazon soils
  - Wurster et al. (2012) PyC quantification using hydrogen pyrolysis

## Access and integration for GIS
- Data is geolocated (Plot_number, Latitude, Longitude) with depth-specific measurements, enabling:
  - Spatial mapping of PyC distribution across the Amazon Basin.
  - Depth-resolved spatial analyses (3D GIS) when combined with other soil/climate layers.
  - Stratification by forest status and plot replication for uncertainty assessment.
- Suitable for integration with ancillary GIS data (soil properties, climate, vegetation, topography) to explore drivers of PyC distribution and storage.