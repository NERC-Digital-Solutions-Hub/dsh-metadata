# Bunce Woodland Survey of Great Britain 2020-2022

## Aim
- Revisit 97 broadleaved woodlands across Britain to enable analyses of ecological change since earlier Bunce surveys (1971; 2000–2003; 2001) using consistent field methods and standardized data outputs.
- Provide data suitable for monitoring environmental health and policy performance over time, with a focus on dataset quality, standardization, and long-term comparability.

## Scope and Coverage
- Time period: 2020–2022 repeat survey.
- Area: Great Britain (97 woodland sites; some sites previously visited in 1971, 2000–2003).
- Site-level and plot-level data collected:
  - 16 randomly placed 200 m² plots per site (canopy and ground flora, soils, habitat management, and other descriptors).
  - Vegetation data: vascular plants, bryophytes, lichens.
  - Soil data: pH and Loss on Ignition (LOI/soil organic matter).
  - Tree data: diameter at breast height (DBH) and other tree characteristics.
  - Site information: slope, aspect, habitat categories, locations, and descriptive notes.

## Datasets Included
- WOODLANDS_SURVEY_SITES_2022.csv
  - Approximate locations of surveyed woodlands (site ID, name, Easting/Northing, grid reference).
- WOODLANDS_SURVEY_SITE_INFORMATION_2022.csv
  - Descriptions of surveyed sites and plots, habitat and tree descriptions, site/plot metadata.
- WOODLANDS_SURVEY_TREE_DATA_2022.csv
  - Tree-level data per plot: site, plot, quarter, tree type, multi-stem indicators, dead status, species, DBH.
- WOODLANDS_SURVEY_GROUND_FLORA_2022.csv
  - Ground flora records for plots: species, cover estimates, growth form, and related plot information.
- WOODLANDS_SURVEY_SOIL_DATA_2022.csv
  - Soil measurements by plot: soil type, date, fresh/air-dried pH, LOI, missing data codes, notes.

## Survey Design & Methods
- Design: Stratified sampling across each woodland area.
- Methods: Based on Bunce & Shaw (1973) standardized ecological survey procedure; field handbook: National Woodland Survey & Native Pine Survey Field Handbook (Smart & Wood, 2021).
- Sampling: 16 plots per site, each 200 m²; plots chosen randomly within each site.
- Data collection scope mirrors earlier surveys (1971; 2000–2003; “2001”) to enable long-term comparison.

## Data Content Details
- Site list: 103 possible sites historically; 97 surveyed in 2020–2022 (7 sites not accessed).
- Data are organized into multiple interrelated CSV files with field codes and groupings designed for standardised reporting and subsequent analysis.
- Nomenclature and coding align with established field methods and referenced handbooks.

## Data Quality, Access & Provenance
- Data prepared by UKCEH Lancaster; authors include S.M. Smart and C.M. Wood and collaborators.
- Data quality: verification, QA, cleaning, and transformation expected as part of the standard workflow; outputs formatted for reuse in reports, maps, and charts.
- Related datasets and baselines provide context for longitudinal analyses (see Related Datasets).
- Supporting documentation includes field handbook and methodological references.

## Related Datasets and Provenance
- Bunce National Woodland Survey 1971; repeated 2000–2003 (baseline comparisons).
- Countryside Survey; Scottish Pinewood Survey 1971 (baseline) and 2018–2022 repeat.
- References for methods and analysis: Bunce & Shaw (1973); Smart & Wood (2021); Stace (1997).
- Further reading on long-term ecological change and landscape-scale drivers (Corney et al. 2004; Kirby et al. 2005; Wood et al. 2015).

## References
- Bunce R.G.H. & Shaw M.W. (1973). A Standardized Procedure for Ecological Survey. Journal of Environmental Management.
- Smart, S. M. and Wood, C. M.: National Woodland Survey & Native Pine Survey Field Handbook, UK CEH, 2021.
- Stace, C.: New flora of the British Isles, Cambridge University Press, 1997.

## Further Reading
- Corney, P.M. et al. (2004) The effect of landscape-scale environmental drivers on the vegetation composition of British woodlands. Biological Conservation.
- Kirby, K.J. et al. (2005) Measuring Long Term Ecological Change in British woodlands (1971-2001). English Nature Research Reports.
- Wood, C. M. et al. (2015) Woodland Survey of Great Britain 1971–2001. Earth System Science Data.

## Notable Limitations and Considerations for Analysts
- Access constraint: seven sites were not granted access in the 2020–2022 survey.
- Data completeness: some soil samples indicated by missing codes; 7 samples with missing plot numbers noted in the dataset.
- Time-series context: designed for long-term comparison with earlier Bunce surveys; users should consult field handbooks and prior publications for analytical methods and historical baselines.
- Data integration: designed to be combined with related datasets (Countryside Survey, Scottish Pinewood Survey) to enhance environmental health monitoring and policy evaluation.