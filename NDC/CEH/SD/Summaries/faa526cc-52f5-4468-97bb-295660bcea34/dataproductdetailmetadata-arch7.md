# Macroinvertebrate taxonomic abundance, water quality, river flow, air temperature and environmental site descriptors from English rivers, 1965 - 2018

## Overview
- Open data product combining macroinvertebrate taxonomic abundance for 1,519 English river monitoring sites (1965–2018) with 41 water quality determinands, river flow, air temperature, and static site descriptors.
- Purpose: enable environmental data and modelling analyses, including assessment of chemical exposure impacts on freshwater wildlife.
- Data assembled from multiple sources (EA, UKCEH, NRFA) and harmonised for national-scale analysis; contains gaps due to non-standardised origins and data availability.

## Key data sources (GIS-relevant)
- Macroinvertebrate time series and site variables: Environment Agency Freshwater river macroinvertebrate surveys (Biosys).
- Water quality: EA Water Quality Archive; pre-2000 data from EA-licensed database.
- River flow: National River Flow Archive (NRFA) gauging stations.
- Air temperature: CHESS-met meteorology dataset (Great Britain, 1961–2017).
- Wastewater exposure: LowFlows2000-WQX (LF2000-WQX) modelled effluent dilution factor (EDF).
- Habitat quality: River Habitat Survey (RHS) data.
- Land cover upstream: Land Cover Map 2015 (LCM2015).
- Catchment and river networks: UKCEH digital river network (1:50,000), Integrated Hydrological Digital Terrain Model (IHDTM), and river network tools in ArcGIS/GRASS.
- Tools: ArcGIS IRN extension, IHDTM flow direction/accumulation grids, Python (Pandas, NumPy, NetworkX, Geopandas), GRASS GIS, Linux bash, JASMIN.

## GIS workflow and data integration
- Three-step integration:
  - Spatial matching: pair environmental sampling locations with macroinvertebrate sites via nearest reach along the river network; distance-based matching along the network.
  - Spatial integration: extract modelled/derived variables (EDF, land cover, air temperature) at macroinvertebrate site coordinates.
  - Temporal matching: align time-series observations (water quality, river flow, air temperature) to the 6-month period preceding each macroinvertebrate sampling date; static site descriptors are used as-is.
- Spatial footprint: product matches the macroinvertebrate sampling network; time stamps align to sampling dates.
- Outputs are organized by region and data type, enabling region-specific GIS joins and map-based analyses.

## Data products and file structure (naming conventions)
- Macroinvertebrate abundance (taxon) files:
  - CP_REGION_MInv_taxonAbundance_startDate-endDate.csv (region-specific)
- Macroinvertebrate site descriptors (physical parameters, up/stream catchment): CP_REGION_MInv_siteVariables.csv
- Water quality statistics (41 determinands, 6-month window prior to sampling):
  - CP_REGION_MInv_<Determinant>Stats_startDate-endDate.csv (41 files; region-specific)
- River flow statistics:
  - CP_REGION_MInv_riverFlowStats_startDate-endDate.csv
- Air temperature statistics:
  - CP_REGION_MInv_airTempStats_startDate-endDate.csv
- Habitat quality descriptors (RHS-derived) are included as site descriptors; RHS data also provided in a separate multi-survey file for sites with multiple RHS surveys.
- Water quality and macroinvertebrate site matches:
  - CP_REGION_MInv_siteMatchedLocation.csv
- Supporting material references include Appendix heatmaps of data completeness and location maps.

## Processing and quality considerations (GIS-focused)
- Macroinvertebrate data (FRMS) cleaning:
  - Standardisation of taxonomic names using Davies & Edwards (2011) reference; reconciliation of EA-specific naming; removal of non-freshwater taxa.
  - Handling of abundance data: pre-2002 data semi-quantitative (log-like categories) transitioning to precise counts in 2002+.
- Data completeness and data gaps:
  - Some macroinvertebrate sites lack public water quality matches due to EA licensing; a few matched sites lack water quality data due to extraction errors.
  - CHESS-met temperatures end in 2017, limiting post-2017 temperature coverage.
- Effluent dilution factor (EDF):
  - Modelled via LF2000-WQX on a truncated river network; EDF represents percent wastewater in river flow; 0 does not always imply zero wastewater (headwater limitations and rounding).
  - EDF values provided as mean, SD, and high-percentiles (Q90, Q95) per site.
- Water quality statistics:
  - Matching: nearest water quality site along same river with no major sewage works in between; manual checks for proximity and data availability.
  - Handling below LoQ values: LoQ1 (use LoQ), LoQ2 (use 0), LoQ3 (LoQ/2); upper-range values kept as reported.
  - Statistics per date: min, max, median, mean, standard deviation; counts of samples and LoQ-based counts stored with Deteminand statistics files.
- River flow statistics:
  - Nearest gauging station along the river network; include POI (1974–2019) and 6-month preceding macroinvertebrate sampling periods.
  - Indicators of Hydrologic Alteration (IHA) metrics: threshold quantiles (5th, 25th, 75th, 95th), days exceeded, duration of exceedances, number of exceedance events, and average patch length.
- Air temperature:
  - Daily mean temperatures from CHESS-met; statistics computed for 6-month periods prior to sampling; note CHESS-met ends 2017, limiting later data.
- Habitat quality (RHS):
  - RHS metrics mapped to macroinvertebrate sites within 5 km along the river network; HMS, HMS_Class, RSB_SubScore, HQA, HQA_ADJ included as site descriptors.
  - RHS is a single-visit dataset; 72 sites have multiple RHS surveys; data integrated accordingly.
- Land cover upstream (LCM2015):
  - Upstream catchment land cover percentages and areas calculated for four categories (Woodlands, Arable, Seminatural, Urban) by snapping macroinvertebrate points to the IHDTM flow-accumulation network and using 50 m grid cells.
  - QA confirmed that land cover sums to ~100% with small rounding variance.

## Outputs, accessibility, and usage notes for GIS work
- Region-based CSVs allow straightforward GIS joins using:
  - BIO_SITE_ID (macroinvertebrate site) as a primary key
  - Corresponding site descriptors, water quality stats, river flow stats, and air temperature stats
  - Matched location references for water quality, river flow, and RHS-derived descriptors
- Land cover, EDF, and habitat indices are integrated into site descriptor files CP_REGION_MInv_siteVariables.csv.
- Completeness heatmaps (Appendix 4) provide insight into data coverage by year and region and can guide data filtering for GIS analyses.
- Data caveats:
  - Not all sites have complete data across all covariates; licensing and extraction limitations create gaps.
  - 0 EDF values may not reflect real absence of wastewater influence in headwaters.
  - Value handling for measurements below LoQ and above measurement range follows defined rules; ensure proper parsing of NA values and units when loading into GIS workflows.

## Practical considerations for GIS specialists
- Use BIO_SITE_ID to join macroinvertebrate observations with hydrology, water quality, temperature, RHS, and land cover descriptors.
- Leverage region-specific outputs to manage regional variations in data density and metadata.
- When mapping EDM-related variables (EDF, land cover, HMS/HQA indices), be mindful of temporal alignment (6-month windows) and static descriptors.
- Validate spatial relationships by reproducing the nearest-neighbor river-network matching steps and consider potential headwater exclusions in EDF and water-quality matches.
- Consult Appendix heatmaps and site location maps for data completeness and spatial distribution as part of GIS data QA.

## References and provenance (high-level)
- Data assembled from EA Biosys, EA Water Quality Archive, NRFA, CHESS-met, LF2000-WQX, RHS, Land Cover Map 2015, IHDTM, and UKCEH river network datasets; methodology combines ecological and GIS analyses for spatial-temporal harmonisation.