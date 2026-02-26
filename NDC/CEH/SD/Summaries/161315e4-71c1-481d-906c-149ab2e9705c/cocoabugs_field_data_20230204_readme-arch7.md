# cocoabugs_field_data_20230204_readme.docx

## Overview
- Describes locations, environmental conditions, and data structures for 123 Malaise trap samples collected in Nov–Dec 2021 within the Gola Rainforest National Park (GRNP) buffer zone in eastern Sierra Leone.
- Context: cocoa farming dominates the landscape and is linked to deforestation; study area spans 908 km².
- Data generated include environmental covariates per sample and metabarcoding results (arthropods) linked to sequencing data, enabling map-based analyses of biodiversity in relation to land-use and habitat features.
- Supported by Natural Environment Research Council (Grant NE/S014063/1).

## Study area and sampling design
- Bounding box for the study area defined in UTM coordinates (zone 29N): five corners provided to outline the sampling extent.
- Sampling division: landscape partitioned into 5 sections (Section 1–GRNP, etc.) to aid logistics and auditing; GRNP serves as a contrast to the agroecosystem.
- Sampling protocol: each sampling point used a single Malaise trap deployed for ~5 days with 99% ethanol; samples stored in fresh ethanol until transport to the UK.
- Temporal scope: November–December 2021.

## Collection and processing methods
- Arthropod collection using Malaise traps; samples preserved in 99% ethanol to minimize DNA degradation.
- Metabarcoding performed by NatureMetrics using Leray2 primers on bulk invertebrate samples.
- Data flow links field collection to sequencing outputs via NatureMetrics’ lab and bioinformatic pipeline.

## Quality control and data reliability
- Primary QC concerns: misrecording environmental covariates and sample labeling; DNA degradation, cross-contamination, sequencing, and bioinformatic errors.
- Mitigations:
  - Handwritten field sheets transcribed to a spreadsheet on collection day.
  - Samples clearly labeled before sequencing.
  - Bulk samples minimize detectable trace contamination; ethanol storage helps reduce degradation.
  - Use of NatureMetrics’ commercial service and established pipeline to reduce sequencing/bioinformatic errors.

## Data structure and file descriptions
- CocoaBugs_field_data_20230128.csv
  - Environmental covariates per sample.
  - Key linkage: NatureMetrics_sample_name connects to columns in Malaise_traps_ZG0001592.client.otuids.csv; SRA_sample_name connects to entries in BioSampleObjects_20230128.txt.
- Malaise_traps_ZG0001592.client.otuids.csv
  - OTU table (species X sample) with NMSeqID as OTU identifier.
  - Sample columns correspond to NatureMetrics_sample_name values.
  - Taxonomic assignments and metadata fields (Kingdom, Phylum, Class, Order, Family, Genus, Species), incidence, similarity, status, and auxiliary fields (e.g., IUCN, RunID).
  - Sequence field contains representative DNA barcode sequence (not all fields shown in dataset excerpt).
- BioSampleObjects_20230128.txt
  - Provides SRA accession numbers and overall BioProject for the samples.

## Nature of recorded values and variable definitions
- CocoaBugs_field_data_20230128.csv describes how covariates are captured for each sample (e.g., NatureMetrics_sample_name, SRA_sample_name, Section, Surveyor).
- Covariate examples (fields commonly used for GIS mapping):
  - Spatial: Latitude, Longitude
  - Habitat/landscape: canopyHt_m, bare_ground_pct, grass_pct, cocoa_pct, liana_pct, forest_pct, agric_pct
  - Management/ disturbance: recent_burning_y_n, stumps_gt_10cm_y_n, stumps_gt_30cm_y_n, oil_palm_y_n
  - Site logistics: date_deploy, time_deploy, datetime_deploy, date_collect, time_collect, datetime_collect
  - Site-specific notes and equipment status (notes, Audiomoth, BAR_Recorder, sample_tube)
- The dataset uses a hierarchical linking scheme:
  - NatureMetrics_sample_name ties covariate data to a specific OTU-table sample column.
  - SRA_sample_name ties covariates and OTU data to sequencing data in SRA/BioSampleObjects.
  - Sample names can include replicates (e.g., A, B) indicating multiple sequencing runs for a single sample.

## Linking data for GIS use
- To map samples and analyze biodiversity against environmental context:
  - Use CocoaBugs_field_data_20230128.csv for per-sample covariates (link via NatureMetrics_sample_name to OTU data and via SRA_sample_name to sequencing metadata).
  - Use Malaise_traps_ZG0001592.client.otuids.csv to relate OTU incidences and taxonomy to samples.
  - Use BioSampleObjects_20230128.txt for SRA accessions and BioProject context.
- Spatial analysis can leverage:
  - Latitude/Longitude coordinates per sample (from covariate file).
  - Canopy height, ground cover (bare/grasses/cocoa), and vegetation structure metrics for habitat suitability and biodiversity modelling.
  - Administrative/section data to aggregate results by landscape segment or GRNP contrast.

## Provisions, provenance, and accessibility
- Data provenance is documented through explicit linking fields between field covariates, OTU tables, and sequencing accession records.
- The dataset emphasizes reproducibility via:
  - Detailed field collection records and standardized labeling.
  - Use of a commercial metabarcoding service with tested pipelines.
- Data accessibility notes:
  - SRA and BioSample accession references are provided in the covariate and OTU tables to access sequencing data and project metadata.

## Acknowledgments
- Funding acknowledged: Natural Environment Research Council (Grant NE/S014063/1).