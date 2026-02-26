# UplandLowlandMetabolomics.csv

## Overview
- Metabolomics dataset derived from sheep urine samples collected in autumn from two pasture-site types: semi-improved and improved.
- Total samples: 8 (n=4 per site).
- Purpose: untargeted primary metabolism analysis to profile metabolite peak intensities.

## Data collection and processing
- Sample collection: urine from sheep, autumn season, at semi-improved and improved pasture sites.
- Sample handling: syringe filtering (< 0.2 μm), flash freezing; blanks processed with ultra-pure water and blank-corrected.
- Storage and shipping: stored at -80 °C, shipped on dry ice to West Coast Metabolomics Center, UC Davis.
- Analytical method: untargeted primary metabolism analysis using ALEX-CIS GC-TOF-MS (Gerstel Inc.).
- Data produced: peak intensity values for all identified metabolites from the untargeted analysis.

## Data structure and contents
- Headers:
  - Sample: combines sheep ID and site of urine collection.
  - Site: either semi-improved or improved pasture.
  - Other headers: identified metabolites; each contains the corresponding peak intensity values.
- Data format: wide-format table with samples as rows and metabolite intensities as columns.
- Data processing note: data are blank-corrected using procedural blanks.

## Provenance and metadata
- Project: Uplands-N2O
- Grant: NE/M015351/1
- Authors: Karina A Marsden et al. (list includes multiple researchers)
- Data reuse: please ensure full citation if data are reused.

## GIS-focused insights and potential visualizations
- Site-level comparisons:
  - Map-based comparisons of metabolite intensities by site (semi-improved vs improved) if geolocation data are available for sample sites.
  - Spatial aggregation of metabolite patterns by pasture type to identify regional differences.
- Environmental layering:
  - Overlay metabolite profiles with environmental layers (soil type, elevation, climate, land-use maps) to explore spatial drivers.
- Visualization concepts:
  - Choropleth or category-based maps by sample group (site) for selected metabolites.
  - Heatmaps or clustered visualizations linked to geographic groupings when sample coordinates are present.
  - Spatial persistence or dispersion analyses of key metabolites across sites.
- Data transformation for GIS:
  - Convert to long format (sample, site, metabolite, intensity) for compatibility with GIS analytics.
  - If locations are unknown, combine with site polygons or centroid locations of pasture areas to enable spatial visualization.

## Data quality, limitations, and considerations
- Small sample size: 8 samples total, which may limit statistical power for spatial comparisons.
- Site categorization is coarse (semi-improved vs improved pasture) without explicit geolocations in the dataset.
- Analytical method is untargeted; metabolite identification and quantification carry typical uncertainties inherent to GC-TOF-MS workflows.
- Data are blank-corrected, but cross-sample batch effects or instrument variations should be considered in any GIS-based interpretation.

## Reuse and citation
- If reusing the data, provide full citation to the project and authors as listed.
- Acknowledge the data provenance: Uplands-N2O project, grant NE/M015351/1, and the West Coast Metabolomics Center at UC Davis for analysis.