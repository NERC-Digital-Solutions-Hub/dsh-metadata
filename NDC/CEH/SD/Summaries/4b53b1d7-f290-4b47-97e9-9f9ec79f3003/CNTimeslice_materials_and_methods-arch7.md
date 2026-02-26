# Nitrogen and Carbon isotope data from 210 Pb dated lake sediment cores in the United Kingdom

## Summary
- A UK-based dataset of nitrogen and carbon isotopes from lake sediments, dated using 210 Pb and 137 Cs methods, intended for GIS-enabled analysis and map-based data products.
- Focuses on lakes with well-resolved chronologies and sediment available from 1850 to the present; spatial distribution reflects UK lake geography and historical ECRC research emphasis, with broader coverage achieved through lowland lake cores.
- Data are generated from cores measured and dated at specialized radiometric facilities; isotopic measurements are conducted at UC Davis, with results linked to core IDs and sample IDs.

## Chronology and dating framework
- Age/depth intervals selected from 210 Pb and 137 Cs dating of cores measured by gamma assay at:
  - Environmental Radiometric Facility, University College London
  - Liverpool University Environmental Radioactivity Research Centre
- 210 Pb dating uses 46.5 keV gamma emissions; 226 Ra inferred via 214 Pb gamma lines after a ~3-week equilibration.
- 137 Cs measured at 662 keV; calibrations based on detector efficiencies with known activity standards; self-absorption corrections applied.
- Target time slices for measurement: 1850, 1900, 1980, and present.
- Age errors:
  - 1980: ±2/3 years
  - 1900: ±15–20 years
  - 1850: ±15–25 years
- Modern date derived from the depth immediately below the surface sample to capture contemporary deposition signals; typical modern date median around 1995.
- Mismatches between cores and lakes exist; most lakes have four depth/age measurements, but some are incomplete due to sediment scarcity or preservation issues.
- Notable multi-core cases: some large lakes or basins (e.g., Loch Lomond, Loch Shiel) have multiple cores to reflect distinct basins or temporal experiments.

## Data coverage and structure
- Spatial distribution reflects NW England, Wales, Scotland emphasis, with broader UK coverage from lowland lake research.
- Incomplete lake sequences are documented:
  - Llyn Dulyn, Wales — missing most recent sediment
  - Loch Ness, Scotland — missing 1980 and recent
  - Lochan Uaine, Scotland — missing 1980 and recent
  - Loch Lomond — two cores (LOMO3, LOMO4) due to basin complexity
  - Loch Shiel — two cores (SHIE2, SHIE5) collected decade apart for diagenesis study

## Isotope measurement and data processing
- Sample preparation: freeze-dried sediment homogenized by ball milling; ~10–12 mg per tin capsule; no pre-treatment to remove inorganic carbonate.
- Measurement: total carbon and nitrogen, plus 15N/14N and 13C/12C, via isotope ratio mass spectrometry at UC Davis facilities (Hydra 20-20 or Anca-GSL IRMS).
- Standardization and quality control:
  - Interspersed with multiple replication standards; analysis IDs and sample IDs recorded as unique identifiers.
  - Isotopic results expressed as delta values:
    - δ15N (‰) and δ13C (‰) per standard definitions.
    - Nitrogen standard: atmospheric N2 (AIR); Carbon standard: Vienna Pee Dee Belemnite (VPDB).
- Quantities reported:
  - Total sediment Carbon and Nitrogen expressed as grams per gram dry weight (g-1 DW).

## Data quality, provenance, and metadata
- Provenance:
  - Core collection and geochronology information archived in the Environmental Change Research Centre (ECRC) internal reports.
  - Isotopic analysis data linked to UC Davis processing IDs; sample and analysis identifiers maintained for traceability.
- Temporal resolution varies by core due to dating uncertainties and sediment availability.
- Data limitations:
  - Gaps in older or recent sediment for several lakes; diagenetic effects considered in multi-core comparisons.
  - Some cores represent multiple basins or decadal experiments, which should be reflected in GIS analyses to avoid spatial-temporal conflation.

## GIS-relevant implications and potential data products
- Suitable map layers:
  - Lake polygons with core locations (point data) and associated cores per lake.
  - Age-depth models and time-sliced isotopic values per core for visualization of isotopic shifts over time.
  - Metadata-rich links to laboratory IDs, measurement dates, and analytical methods.
- Use cases:
  - Visualizing spatial patterns of isotopic compositions (δ15N, δ13C) across UK lakes through 1850–present.
  - Integrating with other lake sediment proxies or land-use data for policy or conservation planning.
  - Comparing dating uncertainties and diagenetic considerations across basins to inform map-based uncertainty analyses.

## Access, lineage, and repository notes
- Data lineage includes:
  - Core selection criteria based on chronology and sediment availability (1850–present focus).
  - 210 Pb and 137 Cs dating procedures and age-depth calculations documented in internal ECRC reports.
  - Isotope measurements conducted at UC Davis with documented standards and QA processes.
- Primary archives:
  - ECRC internal reports for chronology and core metadata.
  - UC Davis Stable Isotope Facility for isotope analysis data and processing IDs.

## Key considerations for GIS specialists
- Ensure linkage between lake-level GIS features and multiple cores per water body, accounting for basins or repeated sampling dates.
- Represent dating uncertainties and age-depth relationships in spatial analyses; consider providing per-core age-depth models as ancillary GIS layers.
- Maintain clear provenance and IDs (sample IDs, analysis IDs) to support reproducibility and cross-referencing with laboratory data.
- Be mindful of data gaps due to incomplete sediment sequences when interpreting spatial-temporal isotope patterns.