# Soil Biodiversity Thematic Programme: Sourhope Site Summary

- A four-year field programme at the Sourhope site (Macaulay Land Use Research Institute, Scottish Borders) monitoring above-ground biomass (productivity), plant composition and diversity under five management treatments across 5 replicate blocks.
- Treatments include Control 1, Control 2 (unmanipulated), Nitrogen, Lime, Nitrogen & Lime, and Insecticide; site grasses are cut monthly to 6 cm and, in insecticide plots, treated with Dursban 4 insecticide.
- Major findings highlight how mowing, fertilisation, insecticide application, and trampling influence productivity, species composition, diversity, and functional plant groups (CSR framework).

## Spatial Design and Data Collected

- Experimental layout: 5 blocks on a downslope gradient; each block contains 6 main plots subdivided into 10 sub-plots; 0.5 m x 0.5 m cells used for data collection and group allocations.
- Data types and collection:
  - Weather: Continuous on-site Automatic Weather Station (rainfall, temperature, radiation, soil moisture).
  - Above-ground biomass: Annual biomass estimates from random 0.5 m2 cells within sub-plots S, T, U, V; samples dried and weighed after every mowing (May–Sept).
  - Baseline and repeated botanical surveys: 0.5 m2 point quadrats (25-point baseline in 1998; 100-point grid in 2000–2002) to record species occurrences; bryophyte identification enhanced in 2002.
  - Soils: Soil pH measured at ~5 cm depth; soil moisture measured in July/August 2002 with theta probe.
  - Field activity: Data collected from multiple projects (Phase I and II) with additional 13CO2 pulse studies and trace-gas measurements in 2002.
- Data scope notes: Appendix maps detail plot-level treatments; 2000–2002 point analyses provide treatment- and block-level patterns; some surveys (e.g., Control 2) were not conducted in specific years.

## Key Findings by Theme

- Mowing effects
  - Agrostis capillaris and Agrostis vinealis declined by over 40% since 2000 across most treatments.
  - Festuca rubra expanded, especially in more fertile (N/L) plots; bryophytes expanded, aided by a ~6 cm sward height from mowing and lack of grazing.
  - Stress-tolerant species increased generally, with reduction in ruderal/S-R types linked to disturbance changes.
- Fertilisation effects
  - Nitrogen and/or lime increased above-ground productivity; plots with both N and lime showed the strongest productivity but may be reaching a peak in response.
  - Lime raised soil pH toward ~7.0; higher pH coupled with lower soil moisture may stress plants in some high-pH plots.
  - Higher pH appears more influential for competitive (CSR) species than simply nitrogen addition; C-S-R group expanded in N+L plots relative to others.
- Insecticide effects
  - Shannon diversity indices were highest in insecticide-treated plots, suggesting reduced herbivory may enable a broader set of plant species to persist.
  - The observed patterns align with literature suggesting insect herbivory can influence diversity, though direct causation remains cautious.
- Trampling effects
  - In C2 plots, productivity declined more sharply in 2002, likely due to trampling during intense sampling and labelled 13CO2 pulses.
- Functional groups and community shifts
  - Three predominant functional groups—stress-tolerators (S), competitive-stress-ruderal (CSR), and SR/CSR—account for 69–95% of vascular plant hits per plot.
  - By 2002, nitrogen and lime plots showed dominance of CSR-type species; unimproved plots favored stress-tolerant species; SR/C-S-R groups reduced in lime- and insecticide-treated plots.
  - Bryophyte presence increased across the site, particularly in unimproved plots, contributing to changes in biomass composition.
- Biodiversity and community structure
  - Point analyses reveal shifts in species hits by treatment; Festuca rubra and Poa pratensis were abundant in fertilised plots, while Festuca ovina and Anthoxanthum odoratum dominated unimproved plots.
  - PCA of point-analysis data clearly separates improved vs unimproved plots; lime-treated plots form a distinct cluster; some N-treated samples resemble limed plots.
  - Shannon diversity declined in nitrogen-and-lime plots from 1998 baseline, while increases were observed in other treatments (notably insecticide plots).

## Data by Year and Plot: Trends Informing Maps

- Biomass productivity
  - General long-term increase from 1999 to 2002 across treatments, with peak productivity in N+L plots; 2002 saw overall biomass reductions relative to 2001, with slope-related variability and block-specific patterns (Block 1 lowest, Block 5 highest decrease).
- Soil chemistry and moisture
  - Lime raised soil pH significantly; high pH correlated with lower soil moisture and a positive relationship to biomass in some plots but not all (pH-biomass relationship is context-dependent by treatment).
- Species and bryophytes
  - Bryophyte hits rose from 2000 to 2002, especially in unimproved plots; vascular plant composition shifted toward Festuca rubra in fertile plots and away from Agrostis spp.
- Disturbance and trampling
  - Lower productivity in recently trampled plots (C2) ties to carrying out 13CO2 pulse experiments; effect is plot- and event-specific.

## Data Quality, Gaps, and Limitations

- 2002 weather data gaps due to a station malfunction; Konza weather data used as a substitute for missing periods.
- Some plots lacked surveys in certain years (notably Control 2 in 2000–2001); analyses use available data with noted limitations.
- The 2002 point analysis included improved bryophyte identification, enabling finer species-level assessment but complicating year-to-year comparability.

## GIS-ready Data Products and Visualizations

- Spatial layers and attributes to create:
  - Plot polygons with attributes: block, plot ID, treatment (Control 1, Control 2, Nitrogen, Lime, Nitrogen+Lime, Insecticide), year, mowing schedule, and trampling events.
  - Biomass time series per plot (1999–2002): total annual biomass and biomass normalized to Control 1.
  - Soil properties per plot: pH at 5 cm (yearly), moisture (2002 measurement locations).
  - Species distribution maps per year: 0.5 m2 cell-level point analysis hits by major taxa (Festuca spp., Agrostis spp., bryophytes, etc.) and by functional groups (S, CSR, SR/CSR).
  - Bryophyte expansion maps showing relative hit proportions across treatments and years.
  - PCA and cluster summaries: spatially encoded results showing separation of improved vs unimproved plots and grouping by lime-treated plots.
  - Disturbance layer: trampling-related productivity impacts by plot and year.
- Potential analyses:
  - Correlation maps between soil pH, moisture, and biomass across plots.
  - Trend maps showing shifts in dominant species and functional groups over time.
  - Suitability maps for future land-use scenarios under N/L amendments and mowing regimes.
- Appendices as data sources:
  - Appendix 1: Site map with treatments
  - Appendix 5: Weather station data
  - Appendix 6–8: Biomass, rank abundance, and species lists by year and treatment

- Data deliverables to GIS teams:
  - Georeferenced plot shapefiles with yearly attribute tables for biomass, pH, moisture, species hits, and Shannon index.
  - Point-analysis CSVs per year with species hits and functional-group classifications ready for spatial visualization and PCA replication.