# Introduction

- Study of 51 sites in three regions (ZOIs) within the Corridor Ankeniheny-Zahamena (CAZ) in Madagascar.
- At each site: measurements and samples taken at five locations along ~60 m transects, from upslope (location 1) to downslope (location 5).
- Measurements and samples at the surface and two depths below the soil surface.
- Soil texture samples collected at each measurement location and combined to form one bulk sample per depth per site (i.e., per transect).
- Missing data are denoted NaN.
- The document describes the data collection methods and the contents of the data file.

## Study design and scope

- Transect number used by the P4GES hydrology team for all measurements and samples.
- Land use classified into six categories based on dominant species and local owner interviews:
  - CC: closed canopy forest
  - RF: reforestation
  - TSA: tree fallow
  - SSA: shrub fallow
  - TM: degraded grassland
  - EUC: eucalyptus plantation
- Site location name linked to transect and land use; P4GES site name provided for cross-dataset comparisons.
- Brief soil description (texture) provided; dominant species listed; site description includes average slope aspect and angle, and transect-specific slope.

## Measurements and samples

- Sample locations: each of the five measurement points includes position, latitude/longitude (decimal degrees, WGS84), and local slope measured with an inclinometer.
- Soil surface saturated hydraulic conductivity (Ksat 0–10 cm) measured with a double-ring infiltrometer; results per measurement point (1–5) plus site-level average, median, and standard deviation.
- Ksat at depth: Ksat (10–20 cm) and Ksat (20–30 cm) measured with an Amoozemeter; results per measurement point plus site-level statistics.
- Soil texture: samples taken at 2.5–7.5 cm, 12.5–17.5 cm, and 22.5–27.5 cm; combined to one bulk sample per depth per transect. Analysis performed at:
  - VU University, Amsterdam (Helium-Neon Laser Optical System) for most samples
  - University of Zürich for transects 55–57 (sieving and Sedigraph)
  - For transects 1–10, bulk samples from 12.5–17.5 cm and 22.5–27.5 cm were combined prior to analysis
  - Reported percentages of clay, silt, and sand for each sample.
- Other soil hydrological characteristics:
  - Undisturbed soil core (100 cm³) collected at each measurement location for the three depth ranges (2.5–7.5, 12.5–17.5, 22.5–27.5 cm).
  - Measured weights at: sampling, after saturation (5 days), after gravity drainage (3 days), and after oven drying (105 °C for 24 h).
  - Derived metrics reported per sample (1–5) plus site-level statistics:
    - Bulk density (g/cm³) = dry weight / 100 cm³
    - Porosity (%) from saturated vs. dry weights and water density
    - Moisture content at field capacity (%) from drainage and dry weight
- Figure 2 referenced to illustrate saturation and gravity drainage behavior.

## Data structure and contents

- For each site and transect:
  - Per-point measurements: Ksat at multiple depths, texture components (clay/silt/sand), coordinates, slope, and core sample results.
  - Summary statistics: per-site average, median, and standard deviation for Ksat and other measures.
- Data are organized per measurement location (points 1–5) within each transect.
- Units and methods are described to enable reproducibility and cross-site comparisons.
- Data provenance notes:
  - Coordinate reference: decimal degrees, WGS84
  - Lab analyses conducted across two institutions (VU Amsterdam; University of Zürich)
- Missing data explicitly marked as NaN.

## Data quality, limitations, and usage notes

- Data come from field measurements with multiple depths and sample types, requiring careful aggregation (per-depth bulk samples, site-level statistics).
- Some soils were analyzed at different laboratories; inter-lab variability should be considered when comparing texture data.
- Certain transects (1–10) had specific preprocessing (combining samples before analysis) affecting direct comparability of some texture depth data.
- Data quality depends on measurement conditions (infiltrometer setup, ponding depth, core sampling) and documentation of transect-specific contexts.

## References

- Styger E, Rakotondramasy HM, Pfeffer MJ, Fernandes ECM, Bates DM. 2007. Influence of slash-andburn farming practices on fallow succession and land degradation in the rainforest region of Madagascar. Agriculture, Ecosystems & Environment, 119:257-269. DOI: http://dx.doi.org/10.1016/j.agee.2006.07.012.
- Zwartendijk BW, van Meerveld HJ, Ghimire CP, Bruijnzeel LA, Ravelona M, Jones JPG. 2017. Rebuilding soil hydrological functioning after swidden agriculture in eastern Madagascar. Agriculture, Ecosystems & Environment, 239:101-111. DOI: http://dx.doi.org/10.1016/j.agee.2017.01.002.