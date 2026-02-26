# cocoabugs_field_data_20230204_readme.docx

- Scope and purpose: This README describes 123 Malaise-trap samples collected in November–December 2021 within the 908 km2 forested leakage belt around Gola Rainforest National Park (GRNP), eastern Sierra Leone, where cocoa farming is a key deforestation driver. The project aims to document environmental conditions and associated arthropod biodiversity to inform environmental health monitoring and policy decisions. The work was supported by the Natural Environment Research Council (Grant NE/S014063/1).

- Study context and location: Samples collected in a cocoa-dominated landscape adjacent to GRNP, with a defined bounding box for the area of study.

- Sampling design and collection methods:
  - Each sampling point used a single Malaise trap deployed for 5 days with >99% ethanol in the collection bottle.
  - After collection, contents were transferred to fresh 99% ethanol and stored at ambient temperature, then shipped from Sierra Leone to the UK.
  - Samples were metabarcoded for arthropods using Leray2 primers via NatureMetrics (bulk invertebrate service).

- Quality control and data provenance:
  - Primary error sources include misrecording environmental covariates, sample mislabelling, DNA degradation, cross-contamination during amplicon generation, sequencing, and bioinformatic clustering/taxonomic assignment.
  - Mitigations:
    - Handwritten field sheets transcribed to a spreadsheet on collection day; sites were documented while fresh.
    - Samples were clearly and multiply labelled before sequencing.
    - DNA degradation minimized by ethanol preservation and storage in fresh ethanol.
    - Use of a commercial service with a dedicated eDNA lab and vetted bioinformatic pipeline to reduce sequencing/analysis errors.

- Data structure and key files:
  - CocoaBugs_field_data_20230128.csv: environmental covariates per sample.
    - NatureMetrics_sample_name: links to columns in the OTU table.
    - SRA_sample_name: links to NCBI SRA entries (BioSampleObjects.txt) and to fastq files.
  - Malaise_traps_ZG0001592.client.otuids.csv: species x sample table (transposed OTU table).
    - NMSeqID: unique OTU identifier representing a species hypothesis.
    - Taxonomic fields and metadata (kingdom, phylum, class, order, family, genus, species) as provided by NatureMetrics.
    - incidence: number of samples where the OTU is detected.
    - Similarity, Comments, Status, and IUCN fields provide taxonomic confidence and target status.
  - BioSampleObjects_20230128.txt: NCBI SRA accession numbers and overall BioProject, linking samples to sequence data.

- Naming conventions and data linkage:
  - The NatureMetrics_sample_name in the covariate file connects to columns in the OTU table.
  - The SRA_sample_name connects to SRA/BioSample entries, tying each sample to its pair of fastq files and to the NatureMetrics sample metadata.
  - Replicate handling: presence of trailing letters (e.g., A, B) indicates technical PCR/sequencing replicates.

- Data content and scope:
  - 123 Malaise trap samples collected across multiple sites/sections within GRNP-adjacent agroecosystem.
  - Data include environmental covariates (e.g., site section, deployment and collection dates/times, geolocation, canopy and ground cover attributes, land-use indicators, recent burning, stump presence, oil palm presence, anthropogenic features, and equipment used).

- Data use and relevance for monitoring:
  - Enables evaluation of arthropod biodiversity in cocoa-influenced landscapes and its relationship to environmental covariates.
  - Supports monitoring frameworks by linking field measurements to metabarcoding outputs, informing data governance, quality assurance, and transparent reporting.
  - Provides traceable data provenance from field collection through sequencing to taxonomic assignment.

- Metadata completeness and data quality considerations:
  - Metadata gaps can hinder reuse; the README emphasizes the need for high-quality, well-documented covariates and sample labelling.
  - Transformation and standardization steps are necessary to ensure covariate values are readily auditable and comparable across studies.

- Data accessibility and sharing:
  - Data are linked to public sequencing resources (SRA/BioSample) via the provided identifiers, enabling reanalysis.
  - The documentation acknowledges barriers to sharing datasets publicly and highlights the importance of data governance and open data practices at the data source.

- Grants and collaboration:
  - Funded by NERC (Grant NE/S014063/1); collaboration between CocoaBugs project and NatureMetrics for metabarcoding services.