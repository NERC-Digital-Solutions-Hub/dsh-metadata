# Glastir Monitoring & Evaluation Programme Vegetation Data 2013-2016

## Overview
- Wales-wide monitoring under the Glastir scheme (AES) to assess biodiversity and track progress toward biodiversity objectives.
- GMEP uses an ecosystem-based, multi-scale approach with a single snap-shot visit planned to capture multiple metrics.
- A 4-year rolling survey (2013–2016) with two components: Wider Wales (baseline estimation and national trends) and Targeted (priority Glastir areas).
- Common spatial unit: 1 km squares; 300 squares sampled over the four-year cycle.
- Data designed for integration with the GB Countryside Survey, enabling potential future cross-survey analyses.
- Spatial confidentiality: maps show 1 km squares plotted at 10 km resolution.

## Survey Design and Sampling
- Rolling 4-year cycle to maximize site coverage while permitting year-on-year trend detection.
- Sampling framework built on Countryside Survey methodology for national and sub-national indicators.
- 300 1 km squares selected: half as Wider Wales (random within Land Classification strata) and half targeted at Glastir priority areas.
- Urban (>75% urban land) or sea (>90%) squares excluded.
- Sampling units aligned to a national 1 km grid with a 10 km confidentiality layer.

## Data Collection and Plot Types
- Vegetation surveys record presence and abundance of vascular plants plus selected bryophytes and macro-lichens; canopy and general habitat data are also collected.
- Plot types and sizes (examples):
  - X plots: random main plots (4 m² or 200 m²; up to 5 per square)
  - Y plots: Small Targeted/Enclosed habitats (4 m²; up to 5 per square)
  - U plots: Unenclosed broad habitats (4 m²; up to 10 per square)
  - B plots: Boundary plots (10 × 1 m; up to 5 per square)
  - A plots: Arable edge plots (100 × 1 m; up to 5 per square; paired with X plots if outside Glastir)
  - M plots: Margin plots (2 × 2 m; up to 15 per square)
  - H plots: Hedgerow plots (10 × 1 m; up to 2 per square)
  - D plots: Hedgerow diversity plots (30 × 1 m; up to 10 per square)
  - S/W and P plots: Stream/Watercourse plots and upslope perpendicular plots (varied lengths)
  - R/V plots: Roadside verge plots (10 × 1 m; up to 5 per square; 2016 only)
- Plots follow standard GB Countryside Survey protocols with some targeted additions to reflect Glastir options.
- Data collected include detailed plot metadata (location, slope, aspect, shade, vegetation heights) and species data across nests within plots.
- Perpendicular P plots are new type; nest lengths can total up to 10 m.
- Field methods and plotting guidelines documented in the GMEP Vegetation Field Handbook (Smart et al., 2016).

## Data Files and Schema
- Three primary CSV files (2013–2016) accompanying the vegetation data:
  - GMEP_VEGETATION_PLOTS_2013_16.csv
    - Core plot-level data per nest: SQ_ID, PLOT_TYPE, PLOT_NUM, COORDINATES (EASTING/NORTHING, 10 km scale), PLOTYEAR, COMPLETED_DATE, SLOPE, ASPECT, SHADE, HEIGHTS (GROUND/SHRUB/CANOPY), TREES_PRESENT/DEAD, and numerous habitat/invasive species fields.
    - Includes fields indicating plot type, location, and landscape context (LC – Land Classification).
  - GMEP_VEGETATION_PLOTS_SPECIES_2013_16.csv
    - Species-level data per plot: SQ_ID, PLOT_TYPE, PLOT_NUM, BRC_NUMBER (species code), BRC_NAMES, COMMON_NAME, NEST_LEVEL, ZERO_COVER, FIRST_COVER, TOTAL_COVER, PLOTYEAR, coordinates, LC.
  - GMEP_VEGETATION_PLOTS_PNESTS_2013_16.csv
    - P plot nest measurements: SQ_ID, PLOT_TYPE, PLOT_NUM, NEST_LEVEL, MAX_LENGTH, PLOTYEAR.
- Data are linked by 1 km square identifiers (SQ_ID) and include OSGB coordinates; 10 km references are included for confidentiality.
- Species nomenclature follows Stace (1997). Field data include presence/absence, cover percentages (to the nearest 5%), and aggregated records where species are difficult to separate in the field.

## Spatial and GIS Considerations
- Data are tied to a 1 km square sampling framework, enabling national and sub-national biodiversity indicators.
- Coordinates are provided in OSGB (E/N at 10 km and plot-level details); supports GIS mapping and spatial analysis.
- Aims to facilitate integration with GB CS datasets for broader landscape-scale analyses.
- Confidentiality is preserved by plotting squares at a coarser 10 km resolution on maps.

## Quality Control and Assurance
- Rigorous field training and standardized field handbooks to ensure consistency across surveyors.
- Quality Assurance (QA) exercise conducted to quantify reliability; target of surveying just over 10% of the sample.
- QA squares selected across Land Classification strata and components; resurveyed by botanical experts using photographic records and maps.
- Across survey years, 85.5% to 90.9% of assessor-recorded species were detected by QA.
- UKCEH operates a Quality Management System (ISO 9001:2015) with documented QA policies and procedures.

## Access, Confidentiality, and Usage
- Data designed for integration with GB CS frameworks; supports national biodiversity monitoring and policy reporting.
- Spatial outputs risk exposure of sensitive locations; confidentiality provisions apply (1 km squares shown at 10 km).
- Primary publications, methodologies, and data handling guidelines are available via the Glastir Monitoring & Evaluation Programme (GMEP) website and the Field Handbook (Smart et al., 2016).

## References and Further Information
- Key methodological references and field handbook:
  - Bunce et al. (2007) ITE Land Classification of Great Britain
  - Glastir Monitoring & Evaluation Programme (GMEP) annual reports and website
  - GMEP Vegetation and Soil Field Handbook (Smart et al., 2016)
- Data and project governance:
  - UKCEH ISO 9001:2015 Quality Management System
  - Appendix 1 lists project roles, data management, and field team personnel
- Related datasets and documentation accessible via gmep.wales and data centre repositories.