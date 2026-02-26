# Suspended organic matter stocks of Welsh upland rivers in response to organic matter addition

## Study overview
- A BACI (before-after-control-impact) experiment comparing upstream reference zones with downstream experimental zones across multiple streams.
- Before period (T1): 61–65 days from early November 2012 to early January 2013; both reference and experimental zones untreated.
- After period (T2): 57–62 days from early January 2013 to March 2013; experimental zone received leaf litter additions to simulate natural inputs.
- Leaf litter sources: one-tonne bags containing oak, birch, and alder leaves; deployment kept a minimum wet weight of 1.7 kg m-2; ambient litter packs reflected naturally occurring leaf inputs.
- Additional leaf litter (630 kg wet weight) added on 12 February and 5 March 2013 after storm events.

## Experimental design details
- Each stream segment comprised a downstream experimental zone and an upstream reference zone of similar length, habitat structure, slope, flow, substratum, and land use.
- A 20–50 m gap between zones ensured independence.
- Data collection spanned both pre- and post-manipulation periods to assess the response to organic matter additions.

## Data collected and variables
- Suspended Organic Matter (SOM) measurements: particles >10 µm and <1 mm.
- Sample collection: 100 L of stream water filtered through sequential 10 µm and 1 mm meshes; three replicates per sampling event.
- Processing and analysis:
  - Freeze-drying of SOM, followed by grinding and subsampling (3 mg ± 0.3 mg) for elemental (C, N) and stable isotope (δ13C, δ15N) analysis.
  - Correction for inorganic content via combustion (550°C, 5 h) on a subset to apply ash-free conversion factors.
- Data products include:
  - Coarse Particulate Organic Matter (CPOM) metrics per sample.
  - Fine Particulate Organic Matter (FPOM) metrics per sample.
  - Concentrations (mg L-1), mass per sample (g), and ash-free dry matter (AFDM) metrics.
  - Isotopic and elemental composition (δ13C, δ15N; C and N contents) for CPOM and FPOM.
- Recording of sampling and environmental context:
  - Site metadata (site_code, landuse, region, etc.)
  - Time indicators (Before/After), sampling month, date, and time
  - Discharge (L s-1)
  - Reach designation (Experimental or Control)
  - Replicate codes (A–F)

## Methods and processing
- Field collection with fixed, random deployment of leaf litter packs within experimental zones.
- Sample handling: refrigeration at ~4°C, transport, and freezing prior to analysis.
- Laboratory analysis:
  - Mass-based quantification of SOM components (g per sample; AFDM basis).
  - Isotopic and elemental analyses performed on subsamples using standard mass spectrometry workflows.
- Data curation: values recorded to the nearest 0.01 g for SOM stocks; detailed column-level metadata for traceability.

## Data structure and files
- Data format: flatbed comma-separated value (CSV) files.
- Main SOM dataset structure includes 33 columns with fields such as:
  - site_code, landuse, region, time (Before/After), date, time, discharge, reach, replicate
  - cpom.g.per.sample, cpom.afdm.mg.l, cpom.subsample.wt.ug, cpom.ug.C.per.subsample, cpom.ug.N.per.subsample, cpom.d13C, cpom.d15N, cpom.d15N Comment
  - fpom.g.per.sample, fpom.afdm.mg.l, fpom.subsample.wt.ug, fpom.ug.C.per.subsample, fpom.ug.N.per.subsample, fpom.d13C, fpom.d15N, fpom.d15N Comment
- Supporting documentation:
  - DURESS_CU_site_description.csv providing site-level metadata (Site_code, Name, Eastings/Northings, Grid, Latitude/Longitude, Elevation, Survey, Catchment)
- Additional context: "Miscellaneous supporting documents" folder includes the site description file and other context for site-level metadata.

## Quality control and data provenance
- Inorganic correction applied to a subset of samples to determine ash-free conversion factors.
- Measurements conducted with standardized units and reporting precision (g, mg, µg, µL, etc.) to enable comparability and replication.
- Documentation of measurement procedures and sample processing steps to support reproducibility.

## Data accessibility and documentation
- Data are structured for upload to relevant data portals and catalogues.
- Comprehensive metadata included within the dataset structure and a dedicated site description file to orient users.
- Clear indication of sampling periods (Before/After), stream reach designation (Experimental vs Control), and replicate coding to support traceability and re-use.

## Relevance for data stewardship
- Demonstrates careful experimental design (BACI), with explicit definitions of reference and experimental zones, and a clearly defined before-after timeline.
- Rich, well-documented data schema enabling reuse for meta-analyses, comparisons across streams, and integration with other hydrological or biogeochemical datasets.
- Metadata richness supports discoverability, interoperability, and proper interpretation of SOM metrics, isotopic and elemental analyses, and environmental context.
- Data stewardship considerations:
  - Ensure consistent unit standards and clear column definitions (especially for CPOM/FPOM and isotopic measures).
  - Maintain provenance records linking SOM measurements to sample events, sites, and processing steps.
  - Plan for metadata versioning and portal publication to facilitate timely discovery and reuse.