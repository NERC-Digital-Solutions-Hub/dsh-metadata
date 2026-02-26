# River (fluvial) and surface water (pluvial) flooding maps for the Central Highlands of Vietnam and surrounding Provinces

- Purpose and coverage
  - Flood maps for the Central Highlands and surrounding provinces in Vietnam (11 provinces in total)
  - Provide flood inundation depth (in metres) for 10 design return periods, from 1 in 5 to 1 in 1000 years
  - Useful for planners and policymakers to identify high-risk areas and support policy planning (including SDGs)

- Data content and structure
  - 330 GeoTiff files plus 1 readme document
  - For each province: 30 maps (10 per flood type)
  - File naming convention: Province_FloodType_ReturnPeriod.tif
    - Flood types:
      - FD: fluvial defended
      - FUD: fluvial undefended
      - P: pluvial
  - Flood depth values in metres; 0 m depth represents no flooding
  - 10 return periods simulated: 1in5, 1in10, 1in20, 1in50, 1in75, 1in100, 1in200, 1in250, 1in500, 1in1000

- Methods and model details
  - Based on updated Fathom 3.0 global flood model (Sampson et al. 2015)
  - Key updates: channel conveyance capacity (Neal et al. 2021), design flood estimation (Zhao et al. 2021), FABDEM 30 m elevation dataset (Hawker et al. 2022)
  - Model validation against satellite imagery and household survey data (Hawker et al., in prep)
  - Distinctions among flood types reflect assumed flood defence standards (FD vs FUD); in this region, differences are small due to how defence standards are estimated
  - Not all flood defences are captured if not visible in the 30 m FABDEM elevation data

- Quality control and validation
  - Validation described via article in press comparing Fathom 3.0 with Fathom 2.0 using satellite flood observations and household data
  - Ability to compute skill metrics (e.g., critical success index, hit rate, false alarm ratio, bias)

- Practical guidance for use
  - Visualization: open GeoTiff files in GIS software like QGIS or ArcMap
  - Data considerations: treat 0 m as no flood; consider adjusting the color ramp to start above zero to highlight flooded areas
  - Analytical workflows: suitable for GIS analysis in R or Python; used to support spatial risk assessment and decision-making

- Limitations and considerations for data governance
  - Defences are approximated based on regional standards and may not reflect all real-world structures
  - Pluvial flood estimates are challenging to validate due to short event durations
  - No explicit global database of flood defences; reliance on elevation data means some defences may be missed

- Provenance and references
  - Data generation and model lineage: Sampson et al. (2015), Neal et al. (2021), Zhao et al. (2021), Hawker et al. (2022)
  - Validation and quality context: Hawker et al. (in prep); Martinis et al. (2015) and related references on flood detection and SAR-based approaches
  - Relevant to methodological improvements and validation against observed flood data and surveys