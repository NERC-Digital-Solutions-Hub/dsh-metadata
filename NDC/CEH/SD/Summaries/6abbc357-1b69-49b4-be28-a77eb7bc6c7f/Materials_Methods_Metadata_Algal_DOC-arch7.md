# Materials and methods, and metadata for Measured and modelled DOC concentrations, and chlorophyll concentration, for UK freshwaters and freshwater mesocosms, 2014-2015. Data taken from 'The contribution of algae to freshwater dissolved organic matter: implications for UV spectroscopic analysis', Adams et al, 2018 Inland Waters

## Overview
- Provides materials, methods, and metadata for measured and modeled dissolved organic carbon (DOC) concentrations and chlorophyll-a (Chl-a) concentrations across UK freshwaters and freshwater mesocosms during 2014–2015.
- Data include both field measurements and modeled DOC (via UV-Vis absorbance) with accompanying absorbance metrics and basic water quality parameters.
- Sets up a framework for GIS-based visualization and analysis of spatial and temporal patterns in DOC and Chl-a, suitable for map-based data products.

## Study sites and sampling design
- Shropshire-Cheshire meres (NW Midland outwash plains): a mix of agricultural, urban, and parkland catchments; DOC and Chl-a variability documented (average Chla across region 2–68 μg L⁻¹ in prior work).
- Additional field sites: Lake District (LD), reservoirs (PR), farm ponds (FP), Yorkshire rivers (YR).
- Site identifiers and metadata: site codes (e.g., SCM for Shropshire/Cheshire Meres) with corresponding site names, coordinates, and sampling details.
- Data tables include detailed geolocation (latitude/longitude) and sampling dates.

## Mesocosm experiments (CEH CAMF)
- Four mesocosms selected from a 32-tank facility to span a range of Chl-a concentrations: tanks 4, 7, 15, 20.
- Experimental treatments: heating (+4 °C above ambient) and nutrient additions (with/without nitrogen or phosphorus); both heated and unheated setups represented.
- Sampling schedule: seven occasions between February and August 2015.
- Assumption: dissolved organic matter (DOM) produced in mesocosms arises from algae-mediated fixation of atmospheric CO2.

## Data structure and content (tables and columns)
- Table S1a: Shropshire-Cheshire meres site list with columns for site code, site name, sample ID, date, latitude, longitude, [DOC] measured (TOC, mg/L), [DOC] modeled (via Carter model, mg/L), absorbance at 270 nm and 350 nm (absorptivity units), [Chl-a] (µg/L), pH, and conductivity (µS/cm). pH values draw on Fisher et al. (2009) for published sites.
- Table S1b: Other field sites (LD, PR, FP, YR) with equivalent columns; includes measured pH for new samples.
- Table S1c: Mesocosm tank time-series data with measured and modeled [DOC], absorbance at 270/350 nm, [Chl-a], pH, and conductivity, across sampling dates.
- Table S2: [DOC] and [Chla] for mesocosms with additional time-series details; includes log-transformed [DOC] and [Chla] values.
- Column heading explanations (provided for S1a, S1b, S1c, S2) cover:
  - Site codes, site names, sample IDs, dates, lat/long, DOC (measured by TOC), DOC (modeled by UV-Vis), absorbance (270 nm, 350 nm), chlorophyll-a, pH, conductivity.
  - Units: DOC (mg/L), absorbance (AU), Chl-a (µg/L), conductivity (µS cm⁻¹), pH (dimensionless).
  - Special notes: generation of modeled DOC via Carter model; some pH values based on prior publications; “Log” columns in Table S2 for log-transformed DOC and Chl-a.

## GIS-ready attributes and considerations
- Geospatial compatibility: each sample has latitude and longitude, enabling point-based mapping of DOC and Chl-a distributions.
- Hierarchical data structure: field sites, mesocosm tanks, and time-series samples can be linked via sample IDs and site codes for multi-layer visualizations (points, time-series charts, and modeled vs. measured comparisons).
- Time dimension: multiple sampling dates (field and mesocosm) support temporal trend analysis and animated maps.
- Data provenance and standards: metadata include explicit table-specific column explanations and units; standardized measurement types (DOC via TOC, UV-Vis modeled DOC, absorbance metrics, Chl-a, pH, conductivity) facilitate harmonization across sites.
- Modeling integration: inclusion of Carter-model DOC alongside measured DOC allows GIS users to compare observed vs. modeled carbon indicators spatially and temporally.

## Practical guidance for GIS use
- Map DOC and Chl-a distributions across UK freshwaters and mesocosm tanks, comparing field sites with mesocosm experiments.
- Explore relationships between Chl-a concentration and DOC, using both measured and modeled DOC values.
- Utilize time-series capabilities to visualize changes over sampling periods and treatments (heating, nutrient additions) in mesocosms.
- Integrate absorbance metrics (270/350 nm) and basic water quality parameters (pH, conductivity) as contextual layers or analytic covariates.
- Merge by consistent identifiers (site code, sample ID) to build comprehensive geospatial datasets with rich metadata.

## Limitations and considerations for interpretation
- Some pH values for older sites are drawn from published sources; newer samples provide fresh measurements.
- Spatial resolution varies by site type (meres, lakes, reservoirs, ponds, rivers), which may influence comparative analyses.
- Temporal coverage is 2014–2015; seasonal and annual variability beyond this window is not captured in the dataset.

## References and data provenance
- Adams et al. (2018) Inland Waters (data source for the measured and modeled DOC and chlorophyll data).
- Fisher et al. (2009); Reynolds (1979); Moss et al. (2005) provide contextual background on site types and ecosystem characteristics referenced in the study.