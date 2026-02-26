# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Purpose and scope
  - Describes a suite of molecular analyses conducted on epilithon (water) and soil samples from the Tamar catchment during winter 2013/2014.
  - Provides data files, methodologies, and cross-linkages between environmental measurements and biodiversity datasets for GIS-based analysis and map-based data products.

- Spatial coverage and sampling design
  - Field sampling aimed for good spatial coverage from the Wold River through to the Tamar River.
  - Exact locations determined in the field using a Garmin GPS12; approximate site locations planned from maps first.
  - Epilithon: 20 locations with three stones sampled per location (A, B, C) along a transect; samples kept cold and processed in the lab.
  - Soil: Targeted a range of soils across the Tamar region representing multiple land uses; 1 km grid references used to protect site anonymity.
  - Spatial identifiers included for each dataset:
    - Epilithon: NGR, Eastings, Northings; River and Catchment names; sampling date; Stone_ID.
    - Soil: Grid reference (1 km resolution), Sampling date, depth of core.

- Datasets and data structure
  - Environmental data files
    - water_env_data.csv: Epilithon water environment data; key fields include Water_lab_ID (unique lab identifier), Water_sample_ID (cross-referenced to WP4 water chemistry), Stone_ID (A/B/C), sampling date, river, catchment, NGR/Eastings/Northings.
    - soil_env_data.csv: Soil environmental data; key fields include Soil_ID (unique lab identifier), Sampling date, Grid reference (1 km resolved for anonymity), depth of core; chemistry-related columns (e.g., Dry, C-total, Loss on Ignition, N-total, pH, major/minor elements such as Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
  - Biodiversity (sequence) datasets
    - Epilithon bacteria: water_bacteria_seq.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv
    - Soil bacteria: soil_bacteria_seq.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Data structure notes
    - DNA extracted from all samples; sequencing performed with 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
    - After processing, sequences clustered into operational taxonomic units (OTUs); data tables show the percentage of each OTU within each sample.
    - Cross-referencing scheme:
      - For epilithon: OTU rows correspond to OTU IDs; columns correspond to sample IDs. Example mappings:
        - Epilithon bacteria: water_bacteria_seq.csv with column headers referencing Water_lab_ID in water_env_data.csv.
        - Epilithon eukaryotes: water_eukaryotes_seq.csv similarly cross-referenced to Water_lab_ID in water_env_data.csv.
      - For soils: OTU rows correspond to OTU IDs; columns reference Soil_ID in soil_env_data.csv.
  - Ancillary documentation
    - Protocol CEH Tellus SW.docx (field and lab procedures reference)

- Data collection, processing, and QA
  - Field collection methods
    - Epilithon: sampling sites chosen for spatial coverage; three stones per site; samples processed in lab after field collection.
    - Soil: sampling across multiple land uses; field-selected sites with accessibility and logistics considered; samples processed in lab.
  - Laboratory and sequencing workflow
    - DNA extraction using MOBIO Powersoil 96-well kit.
    - Purity and yield checked prior to 454 pyrosequencing.
    - Bioinformatic processing yields OTU tables; percentage composition per sample provided in OTU tables.
  - Data quality considerations
    - Cross-referencing between environmental and biodiversity data via lab identifiers (Water_lab_ID, Soil_ID).
    - Anonymity of sampling sites maintained by restricting to 1 km grid references in soil data.
  - Documentation and provenance
    - Version 1.0 (dated 24/03/14) with listed contributors for sample collection, data processing, mapping, analysis, and planning/management.

- Practical GIS implications and usage
  - GIS-ready structure enabling spatial visualization of:
    - Environmental chemistry gradients (soil chemistry and water chemistry proxies).
    - Biodiversity composition across sample sites (OTU abundance per sample, grouped by bacteria/eukaryotes for epilithon and soil).
  - Cross-dataset joins facilitated by:
    - Water_lab_ID and Soil_ID linking environmental measurements to biodiversity OTU profiles.
    - Spatial coordinates (NGR/Eastings/Northings for epilithon; Grid reference for soils) enabling spatial analyses and mapping within the Tamar catchment.
  - Potential analyses
    - Spatial patterns of microbial and eukaryotic communities in relation to soil and water chemistry.
    - Comparison of biodiversity across land-use types and hydrological segments within the Tamar catchment.
    - Integration with WP4 water chemistry data for more detailed water-quality contextualization.

- Limitations and considerations
  - Data exist across multiple files with cross-references required to assemble complete records.
  - Soil data are restricted to 1 km grid references to protect site anonymity.
  - Datasets reflect winter 2013/2014 sampling; temporal scope is limited to that period.

- Access and provenance
  - Version-controlled dataset (Version 1.0; date: 24/03/14; author: R. Griffiths) with clearly attributed contributors for field collection, data processing, mapping, and management.
  - Primary data files listed for integration into GIS workflows, plus a protocol/document for reference.