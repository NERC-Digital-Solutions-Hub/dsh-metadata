# Benthic organic matter of Welsh upland rivers in response to organic matter addition

- Study aim and design
  - A BACI (before-after-control-impact) experiment to test how added leaf litter affects benthic organic matter (BOM) in upland Welsh rivers.
  - Each stream divided into an upstream reference (control) zone and a downstream experimental zone, with 20–50 m separation to ensure independence.
  - Time periods: before (T1; 61–65 days, early Nov 2012 to early Jan 2013) and after (T2; 57–62 days, Jan to Mar 2013) manipulation.
  - In T2, the experimental zone received leaf litter additions to simulate natural senescence/abscission; downstream portion of leaf litter bags maintained a minimum wet weight; additional leaf litter (630 kg wet weight) added after storm events on 12 Feb and 5 Mar 2013.

- Experimental setup and manipulation details
  - Leaf litter supplied via one tonne bags containing oak, birch, and alder, proportioned to experimental zone area.
  - Vegetable net bags used to maintain minimum litter presence (wet weight ~1.7 kg m^-2) within the experimental stretch.
  - Leaf packs deployed along the wetted channel using poles; leaf litter degraded gradually across T2.
  - Storm-driven supplementation occurred twice during T2.

- Collection methods and laboratory processing
  - BOM sampled with Surber nets (area 0.1 m^2, mesh 330 µm, depth 10 cm) from all reaches on five occasions: January, February, March, April, May 2013; six random samples per reach each time.
  - On-site preservation in 70% IMS; in-lab separation of macroinvertebrates from debris; remaining material dried and weighed to 0.01 g.
  - Inorganic content corrected by ash-free conversion (subset combusted at 550°C for 5 h).
  - Measurements reported as grams of organic matter (coarse and fine particulate organic matter).

- Data structure and units
  - Data stored as flatbed CSV files.
  - BOM data comprises 10 columns:
    - site_code, landuse, region, time (Before/After manipulation), month, reach (Experimental or Control), replicate, surber_area, cpom (grams), fpom (grams).
  - Supporting site description data provided in a separate CSV with 10 fields (e.g., site_code, site name, coordinates in British National Grid and WGS84, elevation, catchment, survey campaign).

- Metadata, provenance, and supporting documents
  - Site description CSV includes coordinates, grid references, elevation, catchment, and survey campaign details (e.g., WAWS Welsh Acid Water Survey, Wye catchments, Plynlimon, Llyn Brianne).
  - Data structure explicitly documents the temporal (Before/After) and spatial (Experimental/Control) factors, enabling downstream analyses of treatment effects.

- Quality control and data provenance
  - Calibration steps and dedicated quality-control procedures are not reported.
  - No formal quality-control steps noted; data handling includes ash-free correction for BOM but lacks additional QC metadata.

- Implications for data management and reuse
  - Clear BACI design with explicit upstream reference and downstream treatment zones supports causal inference about organic matter additions.
  - Comprehensive metadata at both the BOM level and site level enhances discoverability and potential cross-site synthesis.
  - Some gaps in QC documentation; future reuse should account for potential variability due to lack of formal QA steps and reliance on ash-free conversion without broader QC metadata.