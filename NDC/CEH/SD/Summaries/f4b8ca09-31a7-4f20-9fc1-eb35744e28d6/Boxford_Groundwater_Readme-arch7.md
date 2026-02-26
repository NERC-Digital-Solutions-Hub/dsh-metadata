# Groundwater levels for piezometers at the Centre for Ecology & Hydrology River Lambourn Observatory wetlands at Boxford, Berkshire, 01/02/2012 to 16/01/2015

## Overview
- Dataset of logged and manual groundwater level observations for piezometers at the River Lambourn Observatory wetlands, Boxford, Berkshire.
- Coverage: 01/02/2012 to 16/01/2015.
- Includes datums and ground elevations (for each piezometer).
- Context and methods drawn from House et al. (2015a, 2015b, 2016) and related references.

## Site description and geospatial context
- Location: CEH River Lambourn Observatory, Berkshire, UK (approximately 51.445°N, 1.384°W).
- Size and environment: ~10 ha riparian wetland, bordered by a 600 m stretch of the River Lambourn; the Westbrook Channel divides the wetland into northern and southern meadows.
- Designations: Site of Special Scientific Interest (SSSI) and Special Area of Conservation (SAC) due to Desmoulin's whorl snail and MG8 vegetation community (NVC).
- Subsurface geology: bedrock Chalk; overlying discontinuous weathered 'putty' chalk, gravels, and peat.
- Spatial relevance for GIS: describable as a mapped wetland with a defined piezometer network; includes an explicit 3D context (ground elevations, datums) suitable for spatial analyses of groundwater heads.

## Instrumentation network and data collection
- Piezometer network: An existing gridded array originally installed in February 2012 (labeled 115) with supplemental piezometers added in May 2013 (locations 16–21) to target temperature-related observations.
- Piezometer types: peat (P) and gravel (G) piezometers; chalk boreholes (C) at sites 3, 22, 23.
- Installation depths:
  - Gravel piezometers typically screened 2.5–3.5 m blg.
  - Peat piezometers screened across peat thickness; peat screens sometimes extend above ground level (with bentonite seals on new installations).
  - Chalk boreholes screened at depths between roughly 5.0–10.0 m blg depending on site.
- Data logging: groundwater heads monitored at selected piezometers every 15 minutes using In-Situ Level Troll 500s or SWS Divers sensors, deployed to a consistent 3 m blg in gravel piezometers or to the base of peat in peat piezometers.
- Quality control: routine manual water level dips performed to validate logged data and mitigate drift (per Sorensen & Butcher, 2011).
- Data coverage per piezometer: Continuous 15-minute logs with some piezometers having NA where data are not available (as detailed in Table 1 of the source).

## Piezometer movement and datum considerations
- Issue: Piezometers are not bedrock-anchored; water-level datum could shift with peat expansion/contraction due to saturation.
- Assessment: Static surveys of selected piezometers conducted in low and high water-table periods (Nov 2013 and Apr 2014) using Trimble 5600 DR total station and Trimble R8 GPS.
- Survey approach: Three total-station setups with dGPS baselines to fixed benchmarks; piezometers chosen based on line-of-sight (see Table 2 for setup details).
- Findings:
  - Apparent systematic error linked to instrument setup (mean differences: Setup 1 = 0.019 m, Setup 2 = 0.000 m, Setup 3 = 0.006 m).
  - Overall vertical movement due to peat is minimal; variance around means ≤ 0.003 m, within instrument accuracy.
  - Conclusion: Piezometer movement due to peat compressibility with saturation was discounted; no datum corrections applied for peat-related movement.
- Table 3 (elevations): Provides November 2013 and April 2014 elevations (mAOD) for numerous piezometers, plus absolute differences, illustrating small relative changes.

## Data structure and considerations for GIS use
- Piezometer identifiers: 1G, 1P, 2G, 2P, 3G, 3P, 4G, 4P, 5G, 5P, 6G, 6P, 7G, 7P, 8G, 9G, 9P, 10G, 10P, 11G, 11P, 12G, 12P, 15G, 15P, 16G, 16P, 17G, 17P, 18G, 18P, 19G, 19P, 20G, 20P, 21G, 21P, 22C, 23C (and related NA entries).
- Data quality and completeness:
  - Some piezometers have NA entries in Table 1 where data were not collected or not available for the full period.
  - Continuous logs are 15-minute intervals; manual dips performed for QA.
- Spatial data considerations:
  - Site coordinates provided for the study area; piezometer coordinates are not explicitly listed in the summarized text but are implied by station setup and map references (Figure 1 and Tables 2–3 in the source).
  - Elevations provided in meters AOD (mAOD) for piezometer and chalk borehole locations, enabling 3D groundwater head analysis when combined with a digital elevation model (DEM).
- Use cases for GIS:
  - Map-based visualization of groundwater heads over time across peat and gravel piezometer locations.
  - Integration with surface-water features (River Lambourn, Westbrook Channel) to analyze groundwater–surface water interactions.
  - Cross-referencing with vegetation and hydrology-related layers (SSSI/SAC context) for ecological analyses.
- References and provenance: Dataset linked to multiple studies (House et al. 2015a, 2015b, 2016; Price & Schlotzhauer 1999; Rodwell 1991; Sorensen & Butcher 2011; Trimble guides; Younger 1989) for methodology and context.

## References
- House, A.; Sorensen, J.R.; Gooddy, D.; Newell, A.; Marchant, B.; Mountford, J.O.; Scarlett, P.; Williams, P.; Old, G. (2015a). Discrete wetland groundwater discharges revealed with a three-dimensional temperature model and botanical indicators (Boxford, UK). Hydrogeology Journal, 23(4): 775-787.
- House, A.R.; Thompson, J.R.; Acreman, M. (2016). Projecting impacts of climate change on a chalk valley riparian wetland. Journal of Hydrology, 534: 178-192.
- House, A.R.; Thompson, J.R.; Sorensen, J.P.R.; Roberts, C.; Acreman, M.C. (2015b). Modelling groundwater/surface-water interaction in a managed riparian chalk valley wetland. Hydrological Processes.
- Price, J.S.; Schlotzhauer, S.M. (1999). Importance of shrinkage and compression in determining water storage changes in peat: the case of a mined peatland. Hydrological Processes, 13(16): 2591-2601.
- Rodwell, J. (1991). British plant communities, Volumes 1-5. JNCC.
- Sorensen, J.P.; Butcher, A.S. (2011). Water Level Monitoring Pressure Transducers—A Need for Industry-Wide Standards. Ground Water Monitoring & Remediation, 31(4): 56-62.
- Trimble (various). R7/R8 GPS Receiver User Guide; 5600 Series User Guide.
- Younger, P. (1989). Devensian periglacial influences on the development of spatially variable permeability in the Chalk of southeast England. Quarterly Journal of Engineering Geology and Hydrogeology, 22(4): 343-354.