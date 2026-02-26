West Halladale wildfire peat cores from Flow Country peatlands

## Overview
- After a 2019 wildfire, 34 short peat cores (50 cm) were collected across the West Halladale burn footprint in Caithness and Sutherland, Scotland.
- Sampling targeted a burn severity map (low, medium, high) and drainage status (drained vs near-natural/undrained), with plots coded by severity and drainage (H/M/L plus N for near-natural).
- Fieldwork occurred in late February to mid-March 2020, with some cores stored due to Covid-19 and analyzed later in July 2020.
- Data are organized into two primary datasets: Peat_core_coordinate.csv (field metadata) and Peat_core_data.csv (laboratory measurements).

## Study design and sampling plan
- Plot selection: Areas representing each severity x drainage combination were identified, and 10–15 plots per combination were planned, then refined in the field.
- Core count: 34 plots ultimately yielded cores; 5 field visits were conducted to collect them.
- Core labeling: Each core/plot received a codename (H, M, L with N for near-natural; numbered 1–15).
- Geography: Field coordinates, elevations, and grid references captured to document sampling locations.

## Field sampling and sample handling
- Equipment used: GPS, printed maps, Russian corer, PVC half-pipes, saran wrap, measuring tape, camera, and recording sheets.
- In-field process: Each plot was surveyed for suitability (depth >40 cm, slope, accessibility). Cores were wrapped and labeled with codenames; bottom and top identified.
- Data capture: Field notes included date, observer, burn severity, codename, core depth, coordinates, elevation, nearby vegetation; photos were taken.
- Sample handling: Raw data (field notes, locations, depths) transcribed to an Excel file and stored on the ERI server; cores transported to cold storage for lab work.

## Laboratory analysis and data generation
- Core processing: Each core was sectioned into 5 cm intervals from the top (0–50 cm). Photos of each section were taken before analysis.
- Measurements and analyses per 5 cm sub-section:
  - Bulk density (BD) via oven-dried weight and water-displacement volume.
  - Moisture content (MC) from wet and dry weights.
  - Organic matter (OM) via Loss on Ignition (LOI) at 550°C for 4 h.
  - Ash content (ASH) from ashed weight at 550°C.
  - Organic carbon (OC) estimated as OM%/2 (Beilman et al. method).
  - Von Post decomposition scale for peat humification assessment.
- Calculation details:
  - BD = dry weight / volume; MC and OM calculated from weights; LOI% and Ash% derived from weights; OC% derived from OM%.
- Documentation and quality: Each sub-section documented with core ID, depth, and imaging; data entry and calculations followed published protocols (Chambers 2011; Beilman 2009; Ekono 1981; etc.).
- Data curation: Three sub-samples with weighing errors were removed to avoid invalid results; overall, multiple cores were analyzed promptly, with some shifted to July 2020 due to Covid delays.

## Datasets and metadata structure
- Dataset: Peat_core_coordinate.csv
  - COREID: Unique ID (letter-based severity/drainage code and number)
  - Depth of core (cm): 40–50 cm (field note indicates 0–50 cm coverage in processing)
  - Lat_OSGB, Long_OSGB: Geographic coordinates (OSGB)
  - Grid_Reference: British Grid Reference
  - Alt_masl: Altitude above sea level (m)
  - Exposure: Slope aspect/angle
  - Vegetation: Description of surrounding vegetation
- Dataset: Peat_core_data.csv
  - COREID, DEPTH (cm): 0–50 cm increments
  - SEVERITY: LOW, MEDIUM, HIGH (burn severity)
  - TYPE: DRAINED or UNDRAINED
  - VOL: Volume (cm3) from water displacement
  - WET_PEAT, DRY_PEAT: Wet and dry weights (g)
  - BD: Bulk density (g cm-3)
  - MOIST%: Moisture content (%)
  - vonPOST: Peat humification stage (1–10)
  - WET_PEAT10, DRY_PEAT10: 10 g peat weights for LOI
  - ASHg: Ash mass (g)
  - OM%: Organic matter content (%)
  - ASH%, OC%: Ash percentage and organic carbon percentage
  - OC% = OM%/2 (Beilman et al. 2009)
- Units and ranges are specified for all measurements (e.g., BD 0.01–1 g cm-3; OM% 30–100%; OC% 15–50%).

## Analytical methods and calibration
- Bulk density: Determined by dividing oven-dried peat weight by water-displacement volume; volume measured with a graduated cylinder.
- Moisture: Calculated from wet and dry weights.
- Organic matter and ash: LOI at 550°C for 4 h; OM% = LOI/dry weight × 100; Ash% = dry ashed weight / dry weight × 100; alternative OC% = OM%/2.
- Organic carbon: Estimated by assuming 50% carbon content in organic matter.
- Von Post: Humification assessed via qualitative squeezing method and scored (H1–H9, plus H10 for near-complete/complete decomposition).
- Instrument calibration: Balances calibrated with standard weights per manufacturer instructions.
- Data provenance and quality: Field and lab workflows documented; sub-sample data with weighing errors removed to ensure data integrity.

## Data governance, quality, and accessibility
- Data provenance: Field data, lab results, and calculations are linked by COREID and depth; metadata define sampling context (severity, drainage, location) and lab methods.
- Quality control: Data were checked and cleaned; some sub-samples excluded due to measurement inconsistencies.
- Storage and access: Raw data and processed datasets stored on institutional servers (ERI/related data infrastructure); standard file formats (CSV) for interoperability.
- Documentation: Methodological details, analytical steps, and references provided to support reproducibility and reuse.

## Challenges and considerations for data stewardship
- Incomplete field picture potential: Not all plots were collectible due to accessibility or management constraints; results reflect feasible sampling within the footprint.
- Data interoperability: Multiple systems used in field (GPS, maps) and lab (ovens, balances) necessitate consistent unit handling and clear linking keys (COREID, DEPTH).
- Timeliness and access: Covid-related delays affected timing of analysis; data are catalogued with clear timestamps and versioning in the data store.
- Reuse and provenance: Detailed methodological notes and reference standards support reuse for peatland carbon studies and comparative analyses.