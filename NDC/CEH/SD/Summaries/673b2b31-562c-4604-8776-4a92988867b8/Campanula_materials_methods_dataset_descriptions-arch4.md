# Campanula rotundifolia: Cytotype Determination and Common Garden Study

## Overview
- Describes the collection, cytotype determination, and a common garden experiment for Campanula rotundifolia.
- Integrates field samples (1700+), flow cytometry-based cytotyping, and a controlled garden study to examine growth, phenology, and fecundity across cytotypes.
- Data are organized into multiple CSV files with detailed metadata and provenance.

## Data collection and materials
- >1700 samples (seeds, leaves, or stem cuttings) collected from geo-referenced locations, mainly Britain and Ireland; some samples from elsewhere for context.
- Volunteers contributed many samples; some seeds obtained from commercial sources or Botanic Gardens.
- Specimens stored appropriately during transport (leaf tissue cool; seeds air-dried and stored at 4°C; leaf material stored at -20°C).
- Efforts to sample multiple plants per locality when possible; targeted intensive sampling in known hexaploid hotspots (Wanlockhead, Teesdale, Cheddar).
- Anonymization: original location resolutions preserved only at 0.01°; samples stored at CEH Edinburgh with sample codes.

## Cytotype determination
- Cytotypes calibrated using prior chromosome counts; flow cytometry used for all routine determinations.
- Preparation and analysis followed a standard one-step protocol (Doležel et al., 2007) with internal standard Pisum sativum L. 'Ctirad' and propidium iodide.
- Flow cytometers used: BD FACSCalibur™ or BD Accuri™ C6; data analyzed with Cyflogic or manufacturer software; CV checked (acceptance if ≤5%).
- Consistency checks: re-analysis performed if multiple peaks or conflicts; some samples grouped to save resources and reanalyzed if needed.
- Quality issues: desiccation and red/brown coloration of samples caused erratic results and were excluded from Cx analyses.
- Cytotype assignment by genome size (pg DNA): diploid, tetraploid, pentaploid, hexaploid ranges defined; samples outside these ranges labeled as aneuploids.
- Linkage: chromosome counts from prior work used to anchor flow cytometry results.

## Common garden study
- Clonal material produced in a glasshouse from cuttings or field-derived seedlings; planted Oct 2008 in a raised bed at CEH Edinburgh (glacially tetraploid-native site.
- Experimental design: five randomized blocks containing clonal tetraploids, pentaploids, and hexaploids; total 55 tetraploid, 1 pentaploid, 37 hexaploid clones across blocks.
- Layout described in Figure 1; plot weeded occasionally to reduce competition.
- Plant-level measurements:
  - Phenology: first flowering date (FFD) recorded in 2009 and 2010 (daily checks; bees can access flowers once open).
  - Growth and fecundity: August 2009 measurements included number of flowering stems, stem height, seedhead counts, open flowers, buds; September 2009 harvests included dry weight and flowering stems.

## Data files and metadata
- Campanula_cytotype.csv: country, location, sample code, latitude, longitude (0.01° resolution), cytotype.
- campanula_FFD.csv: block, clone code, date of first flowering (2009 and 2010), day-number conversions, and plant-condition notes.
- Dest_harvest_Aug_2009_blocks_1_and_3.csv: block, clone code, total flowering stems, stem metrics (height, seedheads, flowers, buds) for up to three stems per plant, plus plant-condition notes.
- Dest_harvest_Sept_2009_blocks_2_and_5.csv: block, clone code, total stem dry weight, number of flowering stems.
- Figure 1: layout of clonal plants in the common garden study (five blocks; random arrangement; clone codes linked to cytotype data via campanula_cytotype.csv).
- Data conventions: dead plants marked with an asterisk; missing data indicated by *.

## Data quality, constraints, and provenance
- Flow cytometry quality control: CV ≤ 5% threshold; reanalysis if peak variability exceeded threshold.
- Temporal/condition effects: time from collection to processing and sample condition (fresh vs. desiccated; green vs. red/brown) can affect results; such samples excluded from certain analyses.
- Anonymization: site coordinates masked to protect locations; sample codes retain traceability to original material for verification.
- Provenance: methods align with established protocols (Doležel et al., 2007) and cross-validation with previous cytotype determinations (e.g., Shepherd 2007; McAllister 1972; Stevens et al. 2012).

## Usage and potential applications
- Enables analysis of how cytotype (diploid to hexaploid and aneuploids) relates to phenology and growth in a controlled setting.
- Supports assessment of data quality, provenance, and replication across years (2009–2010) and environments.
- Demonstrates integration of field-collected materials, molecular/cytometric data, and controlled garden experiments for data-driven ecological and ploidy studies.
- Provides a structured data framework for collaborative reuse and cross-study data sharing within plant cytogenetics and phenology research.