# cocoabugs_field_data_20230204_readme.docx

- A dataset describing 123 Malaise trap samples collected in Nov–Dec 2021 in the Gola Rainforest National Park (GRNP) area of eastern Sierra Leone, where cocoa is a major cash crop. The study area is a 908 km² forested “leakage belt” buffer zone. Data collection was funded by the Natural Environment Research Council (Grant NE/S014063/1).

## How the data were collected and processed

- Methods:
  - A single Malaise trap per sampling point, deployed for 5 days with >99% ethanol in the collection bottle.
  - Trap contents were transferred to clean ethanol-filled tubes and shipped to the UK for metabarcoding of arthropods using Leray2 primers via NatureMetrics’ service.
- Quality control:
  - Key error sources include misrecording labelling/ENV covariates and DNA handling/sequence/bioinformatic errors.
  - Measures taken: transcription of field sheets to a spreadsheet on collection day; clear, multiple labeling; mitigation of DNA degradation by ethanol storage and desiccation; use of a commercial eDNA lab and validated bioinformatic pipeline to reduce metabarcoding errors.
- Outputs:
  - Environmental covariates and taxonomic/sequence data linked to the samples through multiple files (see data structure).

## Data structure and file linkage

- CocoaBugs_field_data_20230128.csv
  - Records environmental covariates for each sample.
  - Key linking columns:
    - NatureMetrics_sample_name: connects to a sample column in Malaise_traps_ZG0001592.client.otuids.csv.
    - SRA_sample_name: connects to entries in BioSampleObjects_20230128.txt (SRA/BioProject identifiers).
- Malaise_traps_ZG0001592.client.otuids.csv
  - OTU table (species x sample perspective): rows are OTUs (NMSeqID); columns include per-sample data.
  - Key fields and concepts:
    - NMSeqID: unique OTU identifier (representative DNA barcode sequence for the OTU).
    - Taxonomic columns: Kingdom, Phylum, Class, Order, Family, Genus, Species (as assigned by NatureMetrics).
    - Incidence: number of samples in which the OTU is detected.
    - Similarity: sequence similarity to the reference GenBank sequence used for taxonomy.
    - Status: Target ( Arthropoda) or Unassigned; IUCN.Red.List, ID_Status, ID_Date, RunID, Sequence, and other metadata.
    - NatureMetrics_sample_name: sample-name key linking to CocoaBugs_field_data_20230128.csv.
- BioSampleObjects_20230128.txt
  - Provides the NCBI SRA/BioProject accession numbers for each sample.
- Data relationships and naming conventions (as described in the 20230204_readme):
  - Structure links NatureMetrics_sample_name (in the OTU table and covariate table) to connect sample data with OTU counts.
  - SRA_sample_name connects covariates to SRA/BioSample entries in BioSampleObjects_20230128.txt.
  - NatureMetrics_sample_name values look like ZG0001592_16360_MiSeq175; the middle number (e.g., 16360) is NatureMetrics’ unique sample identifier; repeated sequencing runs are indicated with a trailing letter (A, B, etc.).
  - The dataset includes 123 samples in total, including possible replicates (e.g., 16425A) representing multiple sequencing replicates.

## Variables and units (environmental covariates and metadata)

- CocoaBugs_field_data_20230128.csv (environmental covariates)
  - Essential linking columns:
    - NatureMetrics_sample_name: sample column name in the OTU table.
    - SRA_sample_name: SRA/BioSample accession for the sample.
  - Example and explanation structure:
    - Sample naming conventions tie environmental covariates to the corresponding OTU data.
- CocoaBugs_field_data_20230204_readme.docx (field descriptors)
  - SITE_ID, date/time of deployment and collection, latitude/longitude, and site-level environmental descriptors.
  - Canopy height, bare ground and ground cover (grass, cocoa, lianas), forest and agriculturally managed areas, recent burning, stumps >10 cm and >30 cm, oil palm presence, notes (e.g., cocoa farm with palm), and equipment identifiers (Audiomoth, BAR Recorder) and presence/absence of sample tubes.
  - These fields support spatial, habitat, and disturbance-context analyses for each trap.

## Taxonomic/sequence data and sample metadata

- Malaise_traps_ZG0001592.client.otuids.csv (OTU table)
  - NMSeqID: OTU identifier (representative DNA barcode).
  - Taxonomy: Kingdom, Phylum, Class, Order, Family, Genus, Species (as assigned by NatureMetrics).
  - Incidence: number of samples in which the OTU was detected.
  - Sequence: DNA barcode sequence used to represent the OTU.
  - Similarity and Comments: taxonomic assignment confidence and notes.
  - Status: Target ( Arthropoda) or Unassigned.
  - IUCN.Red.List: Red List status (where assigned with high confidence).
  - RunID: sequencing run identifier (e.g., MiSeq run).
  - NatureMetrics_sample_name: links to CocoaBugs_field_data_20230128.csv.
- BioSampleObjects_20230128.txt
  - SRA/BioProject identifiers for each sample, enabling retrieval of raw sequencing data.

## How to use the data (practical guidance)

- Integrate data across files by:
  - Joining CocoaBugs_field_data_20230128.csv with Malaise_traps_ZG0001592.client.otuids.csv on NatureMetrics_sample_name.
  - Linking to BioSampleObjects_20230128.txt via SRA_sample_name to access SRA/BioProject metadata and raw data.
- Potential analyses:
  - Explore arthropod community composition (OTU presence/absence, incidence) across cocoa-dominated vs. forested sections using the Taxonomic fields.
  - Correlate OTU patterns with environmental covariates (canopy height, cocoa cover, forest_pct, recent burning, oil palm presence, stumps, etc.).
  - Assess spatial and temporal structure using Section, SITE_ID, latitude/longitude, and deployment/collection dates.
  - Examine replicates (A/B) to gauge technical variation in sequencing runs.
  - Use IUCN status and taxonomic deeper levels to prioritize taxa of conservation relevance.
- Considerations:
  - Some fields may be missing (NA/dots); replicate naming indicates multiple sequencing runs.
  - Data quality steps were applied to minimize mislabelling and degradation; still, users should validate linkages when performing cross-table joins.

## Practical considerations and limitations

- The dataset comprises 123 Malaise trap samples from a specific cocoa-agroforestry context, over a defined 5-day sampling window, with ethanol preservation and metabarcoding.
- Data quality controls focused on accurate field transcription, labeling, and robust metabarcoding pipelines via NatureMetrics.
- Data completeness and consistency depend on correct linkage across the covariate CSV, the OTU CSV, and the BioSample objects file; users should confirm NatureMetrics_sample_name and SRA_sample_name connections before analyses.
- Taxonomic assignments may carry varying confidence (as indicated by Comments and Similarity fields); some OTUs may be Unassigned outside Arthropoda, or have provisional identifications.

## Access and references

- Data provenance includes NatureMetrics metabarcoding outputs, NCBI SRA/BioProject metadata, and field covariate records.
- Core files (referenced in the readme) include:
  - CocoaBugs_field_data_20230128.csv
  - Malaise_traps_ZG0001592.client.otuids.csv
  - BioSampleObjects_20230128.txt
  - CocoaBugs_field_data_20230204_readme.docx (describing the fields and their meanings)
- Funding: Natural Environment Research Council (Grant NE/S014063/1).