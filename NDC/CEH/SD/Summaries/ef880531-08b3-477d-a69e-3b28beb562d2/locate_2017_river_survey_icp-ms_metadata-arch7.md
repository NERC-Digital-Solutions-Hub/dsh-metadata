# Summary

- Objective and scope
  - LOCATE Part 2 provides ICP-MS analyses of cations in river waters as part of a broader project to understand carbon flow from land into the ocean.
  - Sampling covered 41 rivers across England, Scotland, and Wales, monthly in 2017 (with some November 2016 samples; Dorset Stour not sampled until April 2017).
  - Part 2 complements Part 1 (river water parameters) and other LOCATE estuarine datasets; river details are in locate_river_info.txt.

- Data collection design
  - Fixed-site monthly sampling at each river; most sites sampled within a 2–3 day window each month.
  - Sampling aimed for broad geographic and seasonal resolution to study spatial/temporal variation in cations.
  - Coordination managed by BGS personnel; sampling protocol documented for reproducibility.

- River sampling procedure and field practices
  - Field filtration and bottle preparation generally done in the field; POC samples filtered in the lab on return.
  - Samples kept dark and cool (cool box or freezer) during transport.
  - In-field measurements of salinity, electrical conductivity (SEC), and temperature where possible.
  - Mid-channel sampling depths (~0–30 cm) when accessible; representative of main river body.
  - Contamination control measures include rinsing vessels, gloves, and photographing sites upstream and downstream.

- ICP-MS analyses and QA/QC
  - Instrument: Agilent 8900 ICP-QQQ; method Ag_2.3.21 for major and trace elements.
  - Sample type: 0.45 μm filtered river water acidified to 1% HNO3; post-reception samples may receive 0.5% v/v HCl in the lab.
  - Units: elements reported in mg/L or μg/L; extensive list of elements including Ca, Mg, Na, K, P, S, Si, Ba, Sr, Mn, Fe, Li, Be, B, Al, Ti, transition metals, lanthanides, etc.
  - Detection limits and reporting: two detection limits per element (Batch DL and Method DL); below DL typically reported as < DL.
  - QA/QC: UKAS-accredited laboratory (ISO/IEC 17025:2017); QC runs every ~20 samples with calibration blocks; blanks prepared from MQ water acidified to 1% HNO3.
  - Data delivery: results stored in a 61-column CSV with fields for River, Month, sample IDs, and concentrations for each element.

- Data format and contents
  - Primary data file: CSV with 61 columns, including sample identifiers (Lims code), River, Month, and concentrations for a wide suite of elements (Calcium through Uranium, plus several heavy elements and rare earths); units specified per element.
  - Notes on data handling: two DLs per element; if a value is below DL, it should be treated as analytical noise and often reported as < DL.
  - Associated resources: locate_river_info.txt provides river-specific details; Part 1 and estuarine datasets available via DOIs; data may be cross-referenced with BODC records.

- Data access and provenance
  - LOCATE collaboration includes multiple institutions (NERC, NOC, BGS, CEH, Plymouth Marine Laboratory) with academic partners.
  - Part 1 DOI: 10.5285/08223cdd-5e0143ad-840d-15ff81e58acf; estuarine companion dataset DOI: 10.5285/d111d44e-0794-28dc-e053-6c86abc0fc99.
  - Data suitable for GIS-enabled analyses when joined with river metadata (from locate_river_info.txt) and potentially land-use or watershed data.

- GIS relevance and potential uses
  - Enables mapping of spatial and seasonal variation in major and trace cations across GB rivers.
  - Supports spatial interpolation and regional comparisons when combined with river location data and catchment attributes.
  - Useful for studies on river chemistry, nutrient transport, and links to carbon flow from land to ocean.
  - Important considerations: limited to 41 rivers and monthly sampling windows; data resolution may constrain fine-grained mapping in some areas; handle detection limits appropriately in analyses.

- Considerations and caveats
  - Some months have incomplete sampling (e.g., November 2016 as a trial; Dorset Stour late start in 2017).
  - Data are subject to field and lab QA/QC practices; DLs indicate detection thresholds that affect low-concentration values.
  - Integration with Part 1 data or other LOCATE datasets requires careful alignment of site identifiers and temporal frames.