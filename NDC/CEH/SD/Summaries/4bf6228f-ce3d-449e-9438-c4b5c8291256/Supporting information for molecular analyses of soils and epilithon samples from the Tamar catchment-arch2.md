# Suite of molecular analyses in epilithon and soil samples collected from the Tamar catchment in winter 2013/2014

## Aim
- Demonstrate environmental condition and biodiversity across the Tamar catchment using standardized molecular and chemical data.
- Provide datasets suitable for scrutiny of environmental health and policy performance over time.
- Produce comparable outputs (e.g., biodiversity profiles and chemistry data) that can be presented as reports, maps, or charts.

## What is covered
- Epilithon (water) samples and soil samples collected in winter 2013/2014 from the Tamar catchment.
- DNA-based biodiversity assessments (bacteria and eukaryotes) via 454 pyrosequencing.
- Physico-chemical data for soils and water to accompany biodiversity data.

## Data files and structure
- Environment data
  - soil_env_data.csv: soil chemistry and related metadata.
    - Key fields: Soil_ID, Sampling date, Grid reference (1 km anonymized), depth of core, Dry, C-total, Loss on Ignition, N-total, pH, Al, Cd, Cr, Cu, Fe, Ni, Pb, Zn, Ca, Mn, P, S, Mg, K.
  - water_env_data.csv: water chemistry and site metadata.
    - Key fields: Water_lab_ID (unique lab identifier), Water_sample_ID (cross-references WP4 dataset), Stone_ID (A/B/C per site), SAMPLING DATE, RIVER, CATCHMENT, NGR, EASTINGS, NORTHINGS.
- Biodiversity data (OTU tables; cross-referenced to environment data)
  - Epilithon bacteria: water_bacteria_seq.csv
  - Epilithon eukaryotes: water_eukaryotes_seq.csv
  - Soil bacteria: soil_bacteria_seq.csv
  - Soil eukaryotes: soil_eukaryotes_seq.csv
- Cross-referenced structure
  - Rows = OTU IDs for each dataset.
  - Columns = sample identifiers that map to the corresponding environment data IDs:
    - Water datasets align with water_env_data.csv via Water_lab_ID.
    - Soil datasets align with soil_env_data.csv via Soil_ID.
  - Example mappings illustrate how OTU tables link to environmental context (e.g., Epilithon bacteria OTUs linked to water_lab_ID in water_env_data.csv).

- Protocol and documentation
  - Protocol CEH Tellus SW.docx referenced for methodological context.

## Field and laboratory methods
- Field sampling
  - Epilithon (water): 20 sampling locations along the Wolf/Tamar transect; site locations chosen for broad spatial coverage and logistics; GPS (Garmin GPS12) used to record exact locations; three stones collected per location with epilithon removed from a defined area; samples kept cold and processed in the lab.
  - Soil: diverse soils from the Tamar region representing various land uses; sites chosen to provide broad catchment coverage; precise sites determined in the field; GPS used; samples kept cold and processed in the lab.
- Laboratory analysis
  - DNA extraction: MOBIO Powersoil 96-well kit used for both soil and epilithon samples.
  - Quality control: DNA purity and yield checked prior to sequencing.
  - Sequencing: 454 pyrosequencing conducted to assess bacterial and eukaryotic biodiversity within each sample.
  - Data processing: sequences clustered into operational taxonomic units (OTUs); results presented as percentage of each OTU within each sample.

## Data linking and interpretation
- Cross-referencing between biodiversity data and environmental data enables integrated analyses of biotic patterns and environmental conditions.
- Example cross-referencing demonstrates alignment of OTU tables with corresponding Env data IDs (e.g., OTU abundances per Water_lab_ID or Soil_ID).

## Data management and documentation
- Version control: 1.0 (date 24/03/14); author R. Griffiths.
- Contributors by role:
  - Sample collection: Peter Scarlett, Gearóid Webb, Pete Nuttall
  - Data processing and mapping: Gearóid Webb
  - Laboratory analysis: Radim Sarlej, Bruce Thomson, Rob Griffiths
  - Planning and Management: François Edwards, Richard Pywell, Jodey Peyton, Robert Griffiths
- General description: Suite of molecular analyses in epilithon and soil samples from the Tamar catchment (winter 2013/2014).
- Acknowledged need for full methodological documentation (full procedures and units pending).

## Access, reuse, and ongoing documentation
- Data are organized for integration with standard environmental monitoring workflows and are intended to be stored and uploaded to appropriate data portals.
- The documentation emphasizes standardised data structures to enable secondary use, data sharing, and long-term monitoring comparisons.

## Key considerations for analysts monitoring the environment
- Emphasis on standardised data collection, data quality assurance, and clear cross-referencing between biological and environmental datasets.
- Ability to track environmental health over time through linked chemical and biodiversity indicators.
- Potential to enhance value by combining these datasets with additional data sources and by providing accessible data for reuse and policy evaluation.