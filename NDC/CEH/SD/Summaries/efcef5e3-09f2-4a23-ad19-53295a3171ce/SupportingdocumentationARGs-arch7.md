# Supporting documentation

## Overview
- Dataset comprises two CSV files: ARGtype.csv and ARGSubtype.csv
- Content: antibiotic resistance gene (ARG) data
  - ARGtype: copies of ARGs per copy of the 16S rRNA gene
  - ARGSubtype: copies of ARGs per cell
  - Empty cells indicate non-detection
- Structure: 10 columns total; column 1 is Type.level.results; columns 2–10 correspond to nine samples (LZ1–LZ9)
- Samples are pooled fecal samples from 30 cattle, collected from three farmlets (Red, Blue, Green)
  - Red: LZ1–LZ3
  - Blue: LZ4–LZ6
  - Green: LZ7–LZ9

## Data content and structure
- ARGtype.csv
  - Rows 2–25 contain data for Copy of ARGs per copy of 16S rRNA gene
  - Rows 26–49 contain data for Copy of ARGs per cell
- ARGSubtype.csv
  - Rows 2–1209 contain data for Copy of ARGs per copy of 16S rRNA gene
  - Rows 1210–2417 contain data for Copy of ARGs per cell
- Both files use the same 10-column format with sample columns corresponding to LZ1–LZ9

## Sampling and study design
- Location: North Wyke Farm Platform, Rothamsted Research, North Wyke, Devon, UK
- Date: November 2016
- Population: 30 cattle selected from 90; 10 cattle per farmlet (Red, Blue, Green)
- Sampling: Faecal samples collected as cattle entered housing for winter (weaning)
- Pooling: For each farmlet, 3 samples were pooled to create 9 fecal samples total
- DNA extraction: MO BIO PowerSoil DNA Isolation kit with a pre-heating step (65 °C for 10 minutes)
- DNA quality: Assessed with NanoDrop
- Sequencing: Conducted by University of Exeter
- Analysis: Metagenomic data analyzed at University of Hong Kong
  - Reference: ARG-OAP v2.0 with the Expanded SARG Database and Hidden Markov Models

## Metadata and provenance
- Licensing and approvals: Licence XA11784A2; project licence P592D2677
- Related data: Linked to a previously deposited dataset (EIDC_SA_ec83a4ea-923a-4f02-8a9f-aeecc43d7123)

## GIS relevance and potential uses
- Map-based visualization of ARG distribution across farmlets and sampling points
- Integrate ARG abundances with farmlet locations, cattle movement, or housing data
- Comparative analyses across sample types (per copy of 16S rRNA gene vs per cell) and across time/space context if extended
- Inform spatial risk assessments of antibiotic resistance gene presence in livestock environments

## Data quality and considerations for GIS
- Missing values (empty cells) indicate non-detection and must be treated appropriately in analyses
- Data are derived from pooled samples and may reflect group-level rather than individual-level variation
- Two data resolutions (per copy of 16S rRNA gene and per cell) require harmonization for certain GIS analyses
- Spatial interpretation is limited to farmlet-level locations, as precise coordinates are not provided

## Limitations and cautions
- Geographic scope is limited to a single UK site and a single time point (Nov 2016)
- No explicit latitude/longitude coordinates; spatial analysis is constrained to farmlet-level mapping
- Data format is CSV with gene-level abundance; careful preprocessing needed for integration with other GIS layers

## Access and contact
- Data provenance notes and references to original publication and datasets
- Additional licensing details available in the project licenses and linked datasets