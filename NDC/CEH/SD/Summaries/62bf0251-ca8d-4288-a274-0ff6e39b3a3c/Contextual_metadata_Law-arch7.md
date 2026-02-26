# Data on bait use of arboreal ants from an experiment in Malaysian Borneo, 2015-2018.

## Overview
- Dataset records ant abundance at baited traps set on 12 trees in a lowland tropical rainforest in Maliau Basin Conservation Area, Sabah, Malaysia.
- Traps arranged at 5 m vertical intervals across trunk and canopy strata; two bait types per trap: carbohydrate (C) and protein (P).
- Specimens identified to genus and morphospecies; data collected February–May 2016.
- 416 traps in total (208 C, 208 P) across four control plots, contributing to a larger BALI consortium project on biodiversity and land-use impacts.
- Purpose: describe patterns of bait use and species co-occurrence in arboreal ant assemblages.

## Experimental context and sampling design
- Location: old-growth dipterocarp rainforest in Maliau Basin, Sabah, Malaysia; four central control plots used for this bait study (total area protected from edge effects).
- Plot and tree sampling: 12 experimental plots originally established; this dataset uses data from four control plots.
- Baiting and traps:
  - Each trap pair contains one carbohydrate bait (honey and oats) and one protein bait (tuna), hung on opposite sides of the trunk.
  - Pairs located at each height interval; height sampled from ground level upward to canopy.
  - Traps open for 24 hours; specimens preserved in 70% ethanol.
  - Canopy traps defined as above the first branch; trunk traps below the first branch.
- Identification and storage: ants identified to subfamily, genus, and morphospecies; voucher specimens stored in reference collections at University of Liverpool and Universiti Malaysia Sabah.

## Data structure and variables
- Source: BaitUseData.csv
- Columns and meanings:
  - Plot: experimental plot identifier
  - Tree code: unique ID for each sampled tree
  - Tree genus / Tree species: taxonomic identification
  - Height: vertical height above ground (meters) where traps were placed
  - Bait: type of bait with values 'C' (carbohydrate) or 'P' (protein)
  - Repetition: indicates which pair (1 or 2) on a given height
  - Sample: unique trap identifier
  - Strata: 'Trunk' or 'Canopy'
  - Subfamily: ant subfamily
  - Genus: ant genus
  - Morphospecies: morphospecies ID within genus
  - Ant species: species designation, corresponding to morphospecies
  - Abundance: number of individuals of the morphospecies in the trap

## Spatial and GIS-ready considerations
- GIS-ready attributes:
  - Plot and Tree code provide hierarchical spatial context that can be linked to a plot-level shapefile and tree location data.
  - Height and Strata enable 3D visualization of vertical distribution (trunk vs canopy).
  - Bait type allows spatial comparisons of bait preference across the study area.
- Geographic coordinates are not included in the dataset; to map traps, link to external plot/tree geolocation data or a provided GIS layer that contains tree coordinates and plot boundaries.
- Suitable for map-based visuals showing:
  - Trap locations by tree with canopy/trunk classification
  - Abundance or species richness by height and stratum
  - Bait-type effects across spatial units (plots/trees)

## Data quality, provenance, and access
- Provenance: collected by S.J. Law; interpretation by S.J. Law and C.L. Parr; part of the UK NERC-funded Biodiversity And Land-use Impacts on Tropical Ecosystem Function (BALI) consortium.
- Sampling rigor:
  - 12 trees, 4 plots (control condition), 416 traps total; balanced design with two bait types per trap
  - Systematic vertical sampling with clear trunk/canopy delineation
  - Standardized trap exposure (24 h) and preservation
- Limitations:
  - Geographic coordinates not embedded; requires linking to external spatial data for precise mapping
  - Confined to four control plots (limited spatial replication within this dataset)
  - Focused on arboreal ants in one rainforest region; results may not generalize to other ecosystems

## Potential GIS analyses and applications
- Visualize spatial distribution of ant abundances by species and morphospecies across trees and plots.
- Analyze bait preference (C vs P) across canopy and trunk strata and across heights.
- Explore vertical stratification patterns of dominant morphospecies and genera.
- Create interactive maps/visualizations showing trap locations, strata, and abundance hot spots.
- Integrate with additional environmental layers (e.g., canopy height, tree diameter, plot-level treatments if extended data are available) for multivariate spatial analyses.
- Combine with other BALI dataset components to assess how treatment (ant vs termite suppression) may influence bait-use patterns in adjacent plots, though this specific dataset uses only control plots.

## Notes and caveats
- Data reflect only the control plots for the bait-use study; does not include results from ant or termite suppression plots within this dataset.
- To produce precise maps, users should obtain corresponding spatial coordinates or tree geolocations from project metadata or associated GIS layers.