# Campanula rotundifolia cytotype and common garden study data

## Overview
- A dataset describing cytotype characterization and a common garden study of Campanula rotundifolia.
- Includes anatomical, cytogenetic, phenological, and growth/fecundity data from a large number of samples collected across Britain and Ireland, with additional context from elsewhere.
- Data are organized into several CSV files with detailed metadata and provenance.

## Data scope and provenance
- Plant material:
  - 1300+ samples (seeds, leaves, or stem cuttings) from nearly 900 geo-referenced locations.
  - Habitat range broadened beyond Britain and Ireland for broader context.
  - Samples collected by volunteers and sent by post; some from commercial seed suppliers or Botanic Gardens.
  - Preference for multiple samples per locality to reduce clonal redundancy; otherwise single plants collected.
  - Anonymized location data at 0.01° resolution; material stored at CEH Edinburgh for future use with sample codes.
- Cytotype data:
  - Chromosome counts from prior work and flow cytometry verification; consistency checks performed.
  - Flow cytometry followed standard protocols with internal standard (Pisum sativum L. 'Ctirad') and propidium iodide staining.
  - Quality control includes exclusion of groups with problematic DNA-content estimates or high CV (>5%).
  - Stored samples may bias DNA-content estimates and were treated accordingly in analyses.

## Cytotype determination methods
- Flow cytometry preparation:
  - One-step protocol using internal standard and PI dye; tissue chopped, nuclei released, stained, and analyzed.
  - Instrumentation: FACSCalibur or Accuri C6; calibration performed daily.
  - Data analysis: gating to isolate nuclei, histograms of relative fluorescence, DNA contents calculated by comparison to reference standards.
  - Re-analysis triggered by conflicting results or high variability; non-fresh/dried samples treated as separate from fresh for certain calculations.

## Common garden study design
- Clones produced from field-collected cuttings/seed over two preceding years; planted October 2008 in CEH Edinburgh.
- Experimental layout: five randomized blocks featuring tetraploid, pentaploid, and hexaploid clones.
  - 55 tetraploid, 1 pentaploid, and 37 hexaploid clones distributed across blocks.
- Plant maintenance: regular weeding; pollination not restricted.
- Phenology and growth monitoring:
  - Phenology: daily inspection in 2009–2010; first flowering date (FFD) recorded for each plant.
  - Growth and fecundity: counted flowering stems (Aug 2009), measured stem height, seedhead numbers, flower counts on selected stems (Aug 2009); some stems harvested for dry weight (Sept 2009).

## Data files and metadata
- Campanula_cytotype.csv
  - Columns: Country, Location, Sample code, Latitude, Longitude, Cytotype.
- campanula_FFD.csv
  - Columns: Block number, Clone code, Date of first flowering 2009, day-number conversion, plant condition notes for 2009 and 2010.
- Dest_harvest_Aug_2009_blocks_1_and_3.csv
  - Columns: Block number, Clone code, total flowering stems, stem height, seedhead numbers, flowers, buds, notes per stem 1–3, plant condition notes.
- Dest_harvest_Sept_2009_blocks_2_and_5.csv
  - Columns: Block number, Clone code, total stem dry weight, number of flowering stems.
- Data notes:
  - “*” indicates dead or missing data.
  - Data arranged in columns with clone and block references linking to cytotype data.

## Data quality, provenance, and limitations
- Anonymization: precise locations replaced with 0.01° resolution to preserve site anonymity.
- Sample storage: dried or posted samples may yield higher DNA-content estimates; excluded from mean calculations for cytotype determinations.
- Group analyses: samples analyzed in groups excluded from certain calculations to avoid bias.
- Potential biases: occurrence of hexaploids in restricted geographic areas prompted intensified sampling in those regions to better understand extent.

## Governance, sharing, and usage notes
- Data are prepared with clear provenance and metadata to support reuse by data creators and data stewards.
- Metadata includes cloning origin, cytotype, sampling locations, and timing of phenology and growth measurements.
- Data are suitable for cross-referencing cytotype with phenology, growth, and fecundity, as well as for geospatial and provenance analyses.
- Annotations and sample codes enable traceability back to original material and analyses; spatial data are anonymized for privacy.

## References
- Doležel J, Greilhuber J, Suda J (2007). Estimation of nuclear DNA content in plants using flow cytometry. Nature Protocols.
- Greilhuber J, Temsch EM, Loureiro JCM (2007). Nuclear DNA content measurement. In Flow Cytometry with Plant Cells.
- McAllister HA (1972). The experimental taxonomy of Campanula rotundifolia L. Ph.D. thesis.
- Stevens CJ, Wilson J, McAllister HA (2012). Biological Flora of the British Isles: Campanula rotundifolia. Journal of Ecology.