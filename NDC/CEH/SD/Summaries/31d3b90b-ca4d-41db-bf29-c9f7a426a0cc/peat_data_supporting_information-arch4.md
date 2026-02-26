# West Halladale wildfire peat cores

- Purpose: Document the collection, handling, and analysis of peat cores from the West Halladale wildfire footprint in the Flow Country peatlands, Scotland, to assess post-fire peat properties and carbon-related metrics.

## Site and sampling design
- Wildfire occurred in spring 2019, burning about 60 km2 of wet heath and blanket bog in Caithness and Sutherland.
- Sampling focused on a severity- and drainage-stratified footprint (low, medium, high severity × drained/undrained), plus near-natural southern areas.
- A severity map from NatureScot guided plot selection; sampling plots were quarter-grid cells within each severity/drainage combination.
- Code names for plots used a severity letter (H, M, L) and drainage status (N for near-natural), plus a running number (1–15).

## Field sampling methods
- Between 10–15 plots per severity × drainage category were targeted; due to terrain and access, 34 plots yielded cores.
- Coring conducted with Russian corer; cores stored in PVC half-pipes, labeled with codename and plot orientation (top/bottom).
- Field visits totaled five sessions (late Feb–mid Mar 2020); some plots unsuitable due to slope, peat depth, or access constraints.

## Field data collection and storage
- In-field data captured: date, observer, burn severity, plot codename, core depth, coordinates, elevation, exposure, vegetation.
- Complete field data recorded in a spreadsheet and stored on the ERI server; photographs taken for each plot and core.
- All cores stored in cold storage post-collection to prevent deterioration.

## Timestamp and logistics
- Most cores analyzed within days of collection; ten cores stored due to Covid restrictions and analyzed in late July 2020.
- Field equipment included GPS, maps, measuring tape, camera, and safeguarding materials; laboratory analysis used standard lab equipment and protective procedures.

## Instruments and calibration
- Field: GPS device, printed maps for site localization; core sampling apparatus (Russian corer, PVC half-pipes, saran wrap).
- Lab: measuring tape, knives, foil, camera, recording sheets; crucibles; precision balances (three- and five-decimal); 100 mL cylinders; oven (105°C) and muffle furnace (550°C); desiccator; Milli-Q water system.
- Instrument calibration followed manufacturer instructions; balances calibrated with standard weights.

## Datasets and metadata
- Field metadata dataset (Peat_core_coordinate.csv) includes:
  - COREID: unique identifier (based on severity and number)
  - Depth (cm): 40–50 cm range
  - Lat_OSGB, Long_OSGB: geographic coordinates
  - Grid_Reference: British Grid reference
  - Alt_masl: altitude above sea level
  - Exposure: slope/aspect details
  - Vegetation: field description of surrounding vegetation
- Laboratory-derived data per 5 cm core sub-section (Peat_core_data.csv) includes:
  - SEVERITY: LOW, MEDIUM, HIGH
  - TYPE: DRAINED or UNDRAINED
  - COREID, DEPTH (cm)
  - VOL (volume, cm3)
  - WET_PEAT, DRY_PEAT (g)
  - BD (bulk density), MOIST%, vonPOST (humification), WET_PEAT10, DRY_PEAT10
  - ASHg, OM%, ASH%, OC% (organic carbon), and von Post scale values
- Data quality: sub-samples with weighing errors were removed (three sub-samples excluded to avoid erroneous calculations).

## Analytical methods and calculations
- Lab analyses performed on each 5 cm sub-section:
  - Bulk density (BD) calculated from oven-dried mass divided by measured volume (water displacement method).
  - Moisture content (MC) derived from wet and dry weights.
  - Organic matter (OM) via loss on ignition (LOI) at 550°C; OM% derived from LOI and dry weight at 105°C.
  - Ash content (Ash%) calculated from weights after ashing at 550°C; alternatively 100% – OM%.
  - Organic Carbon (OC) estimated as OM%/2 (Beilman et al., 2009).
  - Von Post Scale used to rapidly assess peat humification/decomposition.
- Standardized procedures referenced (Chambers et al. 2011; Heiri et al. 2001; Beilman et al. 2009; Ratcliffe et al. 2018).
- Calculations explicitly documented for BD, MC, OM, OC, and related metrics.

## Data governance, storage, and reuse
- Raw and processed data stored on ERI server; field notes and lab data transcribed to Excel and quality-checked.
- Data handling includes explicit description of units, valid ranges, and data validation rules.
- Data were prepared for dissemination to broader teams and potentially for future cross-site meta-analyses on peat carbon dynamics post-fire.

## Key implications for data leadership
- Demonstrates end-to-end data lifecycle management: design, collection, labeling, metadata curation, storage, lab analysis, and QC.
- Emphasizes the importance of consistent metadata (COREID naming, OSGB coordinates, grid references, depth, severity, drainage) for discoverability and re-use.
- Highlights challenges common to data systems in environmental research: scattered or heterogeneous data sources, need for standardized datasets, and requirement for rigorous quality control.
- Underlines opportunities for data ecosystems: enabling co-ownership of data products, integrating field and lab datasets, and sharing methodologies to support comparable, multi-site analyses.

## References
- Beilman et al. (2009); Chambers et al. (2011); Ekono (1981); Heiri et al. (2001); Melling et al. (2006); Ratcliffe et al. (2018a, 2018b).