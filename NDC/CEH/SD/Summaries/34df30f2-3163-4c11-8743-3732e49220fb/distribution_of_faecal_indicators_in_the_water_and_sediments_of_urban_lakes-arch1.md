Rationale Contamination of waterbodies in urban areas with FIOs from diffuse and point sources is of significant concern to human health, as well as waterbody quality and ecology, due to the potential for exposure to a large audience of formal and informal recreational users.

- Objective
  - Examine spatial patterns of fecal indicator organisms (FIOs) and their drivers in water and sediment across multiple urban lakes with variable connectivity to vectors (birds, wastewater inputs, etc.).
  - Assess how FIO distributions relate to environmental variables and land use, and identify hotspots for potential exposure.

- Study area and design
  - Location: Greater Glasgow conurbation, central Scotland, spanning a rural-urban land cover gradient.
  - Sampling: Summer (July) 6 sites; Winter (December) 15 sites (including all summer sites).
  - Timing: Samples collected 3 hours after sunrise; accompanying bird surveys conducted for about an hour per site.
  - Contextual data: Physical variables from the UK Lakes Portal (altitude, area, catchment size, perimeter, ratio of waterbody to catchment area, shoreline development index).
  - Bird data: Counts, identities, and activities of birds observed during surveys.
  - Land use: 100 m, 500 m, and 2 km buffers around each site using CEH Land Cover Map 2015; categorized into composites (urban, agricultural, wetland) to reflect riparian and aerial connectivity.

- FIO sampling and analysis
  - Sample collection: Spatially dispersed paired water and sediment samples; up to 60 sediment cores per lake; total 770 sample points.
  - Sediment sampling: Gravity corer; top 5 cm preserved; samples processed for microbial analyses.
  - Water sampling: Collected ~30 cm below surface; multiple volumes filtered to quantify bacteria in the water column.
  - Laboratory analyses:
    - Sediment: E. coli attached to sediment; total coliforms; E. coli (CFU g-1 dry weight); testing for Campylobacter, I. enterococci, and E. coli 0157 via enrichment and plating; moisture content and organic matter via standard loss-on-ignition methods.
    - Water: E. coli and total coliforms per 100 mL; processed via MLGA agar plates after filtration.
  - Quality and handling: Sterilisation of equipment between samples; cold chain maintained; standard incubation conditions applied.

- Data processing and analysis
  - Spatial mapping: Kriging in RStudio to produce maps of FIO distributions in water and sediment and to identify hotspots.
  - Spatial structuring: Semi-variance analysis to assess statistical independence and spatial autocorrelation; evaluation of distance-decay patterns from hotspots.
  - Interpretation: Comparison of hotspot locations with bird distributions and potential point sources (e.g., wastewater treatment plants); assessment of whether spatial patterns were consistent across lakes or largely local.

- Indicative results
  - Hotspots observed in both water and sediment across lakes; patterns linked to bird activity and point source inputs.
  - Spatial structuring was generally limited; no strong, consistent decline in FIO concentrations with distance from hotspots, indicating predominantly localised or irregular spatial dependence.
  - Patterns varied temporally (winter vs summer) and between lakes (e.g., Strathclyde Loch vs Bardowie Loch).

- Appendix and data details
  - Appendix lists major nutrients and metals measured in 500 mL water subsamples.
  - Data dictionary (Sediment_and_water_data_from_Glasgow.csv) includes fields for season, site, sample identifiers, coordinates, depth, turbidity, water and sediment bacterial counts, various chemical parameters, bird counts, land-use buffers, habitat metrics, and shore/perimeter metrics.
  - References and data sources for methods and land cover data:
    - R Core Team (2018) for R statistical software.
    - Rowland et al. (2017) Land Cover Map 2015 (GB).

- Implications for practice
  - Localised hotspots of FIOs require site-specific monitoring and management, rather than assuming uniform risk across connected urban waterbodies.
  - Integrating avian presence and proximity to potential point sources improves interpretation of FIO distributions.
  - Data-rich approach (combined water and sediment analyses with land-use and bird data) supports targeted risk assessment for recreational exposure and informs water quality management strategies.