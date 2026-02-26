# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

- Objective and scope
  - Suite of molecular analyses on epilithon (water) and soil samples collected from the Tamar catchment during winter 2013/2014.
  - Aimed at assessing biodiversity (bacteria and eukaryotes) and linking them to environmental data.

- Spatial coverage and data geography
  - Field sampling sites chosen to provide comprehensive spatial coverage from the Wold River through to the Tamar River.
  - Exact sampling locations determined in the field; approximate planning done from maps.
  - Spatial references include:
    - Water samples: Eastings, Northings, and an NGR (British National Grid) reference; GPS-based site locations.
    - Soil samples: 1 km resolution Grid Reference to anonymize sites.
  - Watershed context includes epilithon sampling along a Wolf/Tamar transect.

- Data products and structure
  - Environmental data files:
    - soil_env_data.csv: soil_id, sampling date, grid reference, depth, and soil chemistry (elements and properties such as Dry mass, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K).
    - water_env_data.csv: water_lab_id, water_sample_id, stone_id (A/B/C), sampling date, river, catchment, NGR/easting/northing.
  - Biodiversity data files (OTU tables with percentage composition per sample):
    - Epilithon bacteria: water_bacteria_seq.csv
    - Epilithon eukaryotes: water_eukaryotes_seq.csv
    - Soil bacteria: soil_bacteria_seq.csv
    - Soil eukaryotes: soil_eukaryotes_seq.csv
  - Cross-referencing metadata
    - Rows in each OTU table are OTU IDs.
    - Columns reference samples via:
      - water_bacteria_seq.csv and water_eukaryotes_seq.csv column 1 = Water_lab_ID in water_env_data.csv
      - soil_bacteria_seq.csv and soil_eukaryotes_seq.csv column 1 = Soil_ID in soil_env_data.csv
  - Data processing workflow
    - DNA extraction (MOBIO PowerSoil kit) from all soil and epilithon samples.
    - Purity/yield checked; samples submitted for 454 pyrosequencing to assess bacterial and eukaryotic biodiversity.
    - Post-processing: sequences clustered into OTUs; secondary data tables present OTU percentages per sample.

- Metadata and documentation
  - Protocol document: Protocol CEH Tellus SW.docx (sampling and processing details).
  - Water chemistry context noted: detailed water chemistry and metadata are referenced to WP4 documentation for proximity-related data.

- Field methods and sampling design
  - Epilithon (water) method: field-determined exact sites for spatial coverage; three stones sampled per location; samples kept cold and processed in lab.
  - Soil method: sampling across diverse soil types and land uses; exact sites chosen in field for accessibility; samples kept cold and processed in lab.
  - Sample identifiers:
    - Water: Water_lab_ID, Water_sample_ID, Stone_ID (A, B, C).
    - Soils: Soil_ID.

- Data quality, standards, and cautions
  - Soil data uses 1 km grid references to anonymize sites; coordinates are provided but anonymized at a coarse resolution.
  - Units for soil chemistry are unspecified in the summary; full methodological details awaited.
  - Data are cross-referenced between environmental and biodiversity datasets to enable GIS-like joins, but users must align sample IDs carefully (Water_lab_ID with water_env_data.csv; Soil_ID with soil_env_data.csv).

- Intended GIS and data-visualization uses
  - Map biodiversity across spatial locations by sample, linking OTU compositions to environmental contexts (soil chemistry, water chemistry proximity).
  - Visualize distribution of bacterial and eukaryotic OTUs in relation to environmental gradients (pH, metals, organic content, etc.).
  - Integrate with WP4 water chemistry metadata for comprehensive environmental mapping around epilithon samples.

- Contributors and provenance
  - Sample collection, data processing, laboratory analysis, planning and management contributions listed.
  - Timeframe: winter 2013/2014; version 1.0, dated 24/03/2014.