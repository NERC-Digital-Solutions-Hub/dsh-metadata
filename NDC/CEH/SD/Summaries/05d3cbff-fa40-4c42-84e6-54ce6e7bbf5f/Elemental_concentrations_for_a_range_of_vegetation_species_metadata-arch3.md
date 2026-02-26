# Elemental meta-data

## Overview
- Describes the metadata and measurement framework for elemental analysis in plant and soil samples.
- Captures sample provenance (lab and sample identifiers, collection site, sampling date), biological context (plant species and taxonomy), and analytical results (element concentrations by ICPMS/ICPOES).
- Distinguishes plant samples from soil samples; when soil samples are taken, plant-specific taxonomic fields may be not applicable.
- Includes a comprehensive set of element concentration fields, with both quantitative and semi-quantitative measurements and detection-limit indicators.

## Core metadata fields
- Laboratory_ID: CEH centralised chemistry laboratory unique sample identifier.
- Sample_ID: CEH Radiochemistry laboratory unique sample identifier.
- Collection_Site: Sampling site.
- Sampling_date: Date of sampling (dd/mm/yyyy).
- Species: Latin name of the plant species (n/a if soil sample).
- Common_name: Common name of the plant species (n/a if not provided or soil sample).
- Order, Family, Genus: Taxonomic classification (n/a if soil sample).
- Notes on sample type: Clear distinction between plant tissue vs soil sample (soil samples may have plant fields as n/a).

## Measurements and data types
- Element concentration columns (e.g., Li_mg_kg_quantitative_mg_kg_dry, Be_mg_kg_quantitative_mg_kg_dry, etc.) measured primarily by ICPMS or ICPOES.
- Units vary by column; common units include mg per kg (dry weight) or mg per kg (fresh weight) as specified.
- Some columns indicate tests as semi-quantitative rather than fully quantitative.
- Many elements have multiple related columns (e.g., different measurement methods or weight bases) and are labeled with descriptors like _dry, _kg_quantitative_mg_kg_dry, _mg_kg_semi_quantitative_m etc.

## Data quality indicators and missing data
- Detection limits indicated with a "<" prefix (e.g., Be_<, S_<, Cr_<, Ce_<).
- Some columns marked as “n/a - data not available” indicating missing data.
- Some records explicitly state “sample was below the limit of detection (LOD)” for certain elements.
- A mix of complete, semi-quantitative, and non-available data across elements and samples.

## Methods and data structure
- Methods referenced: ICPMS (inductively coupled plasma mass spectrometry) and ICPOES (inductively coupled plasma optical emission spectroscopy).
- Data structured to support traceability from collection through laboratory analysis to reported results, enabling quality assurance and audit trails.

## Sample types and taxonomic information
- Plant samples include species with full taxonomic details (Latin name, Common_name, Order, Family, Genus).
- Soil samples represented either by absence of plant taxonomic fields or explicit n/a entries in plant-related columns.
- Sampling_date, collection_site, and laboratory identifiers provide spatial and temporal context for monitoring.

## Data governance and sharing implications
- The framework emphasizes data provenance and transparency (clear identifiers for labs and samples, collection site, date).
- Public sharing of underlying data is acknowledged as a potential barrier in practical implementations; the metadata structure supports data sharing while highlighting the need for robust metadata and data management standards.
- Quality assurance, data cleaning, transformation, and clear presentation (reports, charts, dashboards) are integral to turning raw measurements into actionable monitoring outputs.

## Relevance for monitoring frameworks
- Enables environmental health monitoring by linking sample provenance, species context, and multi-element chemical data.
- Supports policy evaluation and decision-making through standardized metrics across sites, species, and time.
- Helps identify data gaps, standardize metadata, and plan targeted data collection or new data acquisition to fill critical gaps.
- Provides a structured basis for data governance and open-data practices to improve transparency and reuse.