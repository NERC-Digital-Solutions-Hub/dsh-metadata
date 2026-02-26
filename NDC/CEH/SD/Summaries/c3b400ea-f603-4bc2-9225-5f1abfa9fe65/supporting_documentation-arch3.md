# Mean and variability of topsoil organic carbon concentrations across Great Britain derived at 1 km resolution from an ensemble of eight digital soil maps

- Purpose: Provide a national-scale comparison of topsoil organic carbon (SOC) concentration predictions by contrasting eight published map products to understand agreement, uncertainty, and drivers of differences. This supports monitoring, policy evaluation, and informing future soil-carbon decisions.

- Context and scope:
  - GB-wide analysis at 1 km resolution, focusing on the top 0–15 cm (except LUCAS 20 cm and OCTOP 30 cm).
  - Maps sourced in 2020 and harmonised to a common extent, resolution, and CRS for comparison.
  - The study compares SOC in g kg-1 and includes statistical summaries to quantify variability and disagreement among products.

- Eight primary maps included (names indicate creator and soil survey used):
  - CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, ISRIC-2017, ISRIC-2020, LUCAS, OCTOP
  - Depth coverage: most maps cover 0–15 cm; LUCAS is 20 cm; OCTOP is 30 cm.
  - SOC prediction methods among maps include pedotransfer rules, upscaling, ordinary kriging, machine learning, and various covariates.

- Harmonisation and data processing:
  - All maps were harmonised to Great Britain, 1 km grid, EPSG:27700.
  - ISRIC and LUCAS maps resampled to 1 km; snapping performed to align with Countryside Survey (CS) grid.
  - Depth adjustments applied to obtain 0–15 cm SOC where required.
  - Data units converted to g kg-1; specific value-range corrections applied (e.g., 0 g kg-1 treated as predictions, not missing data; some maps required scaling conversions).

- Ensemble statistics and outputs:
  - For grid cells with data from all eight maps (n = 208,752), the following statistics are calculated:
    - Mean SOC (g kg-1)
    - Standard deviation (SD) of SOC
    - Coefficient of Variation (CoV = SD/Mean)
    - Signal-to-noise ratio (SNR = Mean/SD)
    - Most deviant map from the mean (per cell; 1–13 coding for which map is most deviant; some ties)
    - Greatest deviation from the mean expressed as a percentage
    - Greatest deviation from the mean expressed as the number of SDs exceeded
  - These metrics help identify where maps agree or disagree and which products drive discrepancies.

- Data structure and access:
  - Dataset: SOC_map_summaries.tif, a single 1 km-resolution geotiff with 7 bands covering GB (excluding Northern Ireland).
  - Band descriptions:
    1) Mean SOC (g kg-1) across the 8 maps
    2) SD of SOC across the 8 maps
    3) CoV (SD/Mean)
    4) SNR (Mean/SD)
    5) Most deviant map from the mean (1–13 mapping to specific maps)
    6) Greatest deviation from the mean as a percentage
    7) Greatest deviation from the mean as the number of SDs exceeded
  - Cells with missing data in any map are marked as no data; only cells with complete data across all eight maps are included in the statistics.

- Quality control and data checks:
  - Performed 19 October 2022 prior to submission.
  - Consistent spatial resolution, extent, and CRS across layers.
  - All bands stacked into a single raster; validation of pixel counts, extents, and coordinate system.
  - Data ranges checked (SOC 0–550 g kg-1). Negative values in CSGB-AIC reset to no-data where applicable; some 0 g kg-1 values acknowledged as predictions, not missing data.
  - Some ties in most-deviant maps exist (205 ties across 5 map-pair combinations).

- Third-party datasets and accessibility:
  - Maps sourced from CSGB-AIC, CSGB-GAMM, CSGB-KRGS (limited public release due to sampling-point confidentiality concerns), CSGB-MLRF, LUCAS, OCTOP, ISRIC-2017, ISRIC-2020.
  - Third-party data references and DOIs provided for proper citation.
  - Public availability varies: CSGB-KRGS restricted due to reverse-engineering concerns; other maps and derived data are cited with sources and links.

- Usage notes and citations:
  - When using the derived dataset, cite the eight primary maps as follows: CSGB-AIC, CSGB-GAMM, CSGB-KRGS, CSGB-MLRF, OCTOP, LUCAS, ISRIC-2017, ISRIC-2020, with the respective original sources and DOIs.
  - Original study context: Feeney et al., Multiple soil map comparison highlights challenges for predicting topsoil organic carbon at national scale. Scientific Reports (2022); related open-access paper for background and detailed methods.

- Relevance for monitoring frameworks:
  - Provides a transparent, ensemble-based way to monitor soil carbon predictions and their uncertainty at national scale.
  - Delivers clear, governance-friendly metrics (mean, SD, CoV, SNR, and map-specific deviations) to scrutinise policy-relevant soil-health indicators and identify data gaps or methodological biases.
  - Highlights data governance considerations (public data sharing vs. data privacy) and the practicalities of harmonising diverse map products for decision support.