# Diatom data:

## Overview
- Purpose: Assess diatom response to wildfire in restored vs unrestored sites of the South Fork McKenzie River, Oregon, post-Holiday Farm Fire (Sept 2020).
- Location: South Fork McKenzie River, Oregon; coordinates 44.17, -122.30.
- Data scope: Post-fire periphyton assessment across 23 sites (10 sites in Feb 2022; 13 sites in Sep 2021).

## Data collection and scope
- Sampling periods:
  - February 2022: 10 sites (5 restored, 5 unrestored).
  - September 2021: 13 sites (7 restored, 6 unrestored).
- Sites and transects: Restored transects T1 and T2; unrestored transects T8, T9, T10, T11 and T8.5.
- Sample unit: Transect-based composite of three rocks per transect.
- Environment: Includes pool, riffle, and off-channel habitats.
- Post-fire context: All sites burned; data reflect post-fire conditions.

## Dataset structure
- One CSV: SFMR_Diatom_Data.
- Key columns include:
  - Status (restored vs unrestored), date.coll, year, habitat, Season, transect, site.id.
  - AI (autotrophic index), mean.depth (cm), mean.velocity (m/s).
  - rock1.area.cm2, rock2.area.cm2, rock3.area.cm2 (rock surface area).
  - Diatom genus counts (e.g., Tabellaria, Epithemia, Fragilaria, Hannaea, Melosira, Nitzschia, Cocconeis, Gomphonema, Diatoma, Navicula, Achnanthes, Reimeria, Cyclotella, Cymbella, Frustulia, Synedra, Rhopalodia, Eunotia, Pinnularia, Rhicosphenia, Amphora, Caloneis, Surirella, Asterionella, etc.).
  - Additional columns for each genus count and for overall species-level/TF data.
  - Geography coordinates per transect end (leftLon/leftLat, rightLon/rightLat).

## Measurements and calculations
- Diatoms: Identified to the genus level; counts include a wide set of genera listed in the dataset description.
- Auto trophic metrics: Autotrophic Index (AI) = organic mass per cm2 in periphyton divided by chlorophyll a (Chl a) per cm2 in periphyton.
- Biomass proxies: Chl a and ash-free dry mass (AFDM) analyzed from subsamples to estimate Chl a per unit organic biomass.
- Sample quality: Diatoms counted to standard laboratory procedures with a robust minimum (at least 500 valves per sample).

## Methodology
- Periphyton collection: Scrub five randomly selected cobbles per sample location with a toothbrush, rinse, and composite into a single sample; split into three subsamples (one preserved for diatoms, two for Chl a and AFDM).
- Diatom processing: Count and identify at least 500 diatom valves per sample to genus level.
- Standards referenced: Baird et al. (2017) and Kelly et al. (1998) for sampling protocols.

## Quality control
- Diatoms processed and counted per standard laboratory procedures; minimum sample size of 500 valves per sample to ensure robustness.

## Collection dates and samples
- February 2022: 10 sites (n=5 restored, n=5 unrestored).
- September 2021: 13 sites (n=7 restored, n=6 unrestored).

## Location details
- Lat/Long: 44.17, -122.30 (South Fork McKenzie River, Oregon).
- Transect-level coordinates provided for sampling locations (left and right bank endpoints).

## How this data supports analysis and decision-making
- Enables comparisons of diatom community composition and AI between restored and unrestored sites under post-fire conditions.
- Allows examination of relationships between diatom genus abundances and physical/biological variables (mean depth, velocity, rock surface area, habitat type, season).
- Supports evaluation of restoration effectiveness and wildfire impacts on periphyton structure and productivity.