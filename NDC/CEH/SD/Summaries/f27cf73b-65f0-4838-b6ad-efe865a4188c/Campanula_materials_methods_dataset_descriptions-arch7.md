# Campanula rotundifolia: Cytotype determination and common garden study

## Overview
- A study combining large-scale, geo-referenced sampling with cytotype analysis and a controlled common garden experiment to understand cytotype distribution and phenology in Campanula rotundifolia.
- Data are organized in multiple CSV files describing cytotype results, phenology, and growth metrics, suitable for GIS-based visualization and spatial analysis.

## Spatial data and sampling
- >1300 samples collected from ~900 geo-referenced locations, focused on Britain and Ireland with additional samples for broader context.
- Materials included seeds, leaves, and stem cuttings; many samples contributed by volunteers.
- Sampling strategy aimed to minimize sampling of the same clone by maintaining at least 5 m between plants when possible; some sites yielded a single plant.
- Intensive sampling in known hexaploid hotspots (Wanlockhead, SW Scotland; Teesdale, central England; Cheddar, southern England) to map extent of hexaploids.
- Location data provided in campanula_cytotype.csv at 0.01° resolution to protect anonymity; GPS or Ordnance Survey-derived coordinates used where available.
- Some material stored in cold storage or dried, affecting downstream DNA content calculations (stored/dried samples excluded from mean DNA content calculations).

## Cytotype determination and data quality
- Cytotypes initially determined by root-tip cytology and later verified by flow cytometry; conflicting results re-tested.
- Flow cytometry protocol uses an internal standard (Pisum sativum 'Ctirad', 2C = 9.09 pg) and propidium iodide staining.
- Data collected with BD FACSCalibur or BD Accuri C6; QC checks ensure CV of peaks ≤ 5%.
- DNA content-based cytotype classification calibrated against known chromosome counts; some samples excluded from mean DNA content calculations (e.g., dried or group-analyzed samples).
- Results stored in campanula_cytotype.csv; includes country, location, sample code, and coordinates, along with cytotype information.

## Common garden study design and spatial layout
- Clonal material derived from field-collected seed/ cuttings and grown in a glasshouse before planting in a raised bed at CEH Edinburgh.
- Five randomized blocks containing tetraploid, pentaploid, and hexaploid clones to cover the species’ British Isles range.
- Final layout shown in Figure 1 with 55 tetraploid, 1 pentaploid, and 37 hexaploid clones across blocks.
- Plant growth, survival, and flowering phenology monitored; pollination allowed to proceed naturally.

## Phenology and growth data (data files)
- Campanula_FFD.csv: First flowering date (FFD) recorded in 2009 and 2010 for each clone; includes day-number conversion and plant condition comments.
- Dest_harvest_Aug_2009_blocks_1_and_3.csv: August 2009 measurements for blocks 1 and 3, including:
  - Number of flowering stems, stem height, seedhead counts, open flowers, and buds per stem (three stems per plant sampled).
  - Block and clone identifiers; occasional plant-condition notes.
- Dest_harvest_Sept_2009_blocks_2_and_5.csv: September 2009 harvest data for blocks 2 and 5, including:
  - Total dry weight of stems and number of flowering stems.
- Data file format notes: An asterisk (*) marks dead plants or missing data; data are organized in columns with clear headings.

## Data files (structure and usage)
- Campanula_cytotype.csv
  - Columns: Country, Location, Sample code, Latitude, Longitude
- campanula_FFD.csv
  - Columns: Block, Clone code, FFD 2009, 2009 day-number, plant-condition notes 2009, FFD 2010, 2010 day-number, plant-condition notes 2010
- Dest_harvest_Aug_2009_blocks_1_and_3.csv
  - Columns: Block number, Clone code, total flowering stems, stem height, seedhead counts, open flowers, buds, etc., plant-condition notes
- Dest_harvest_Sept_2009_blocks_2_and_5.csv
  - Columns: Block number, Clone code, total stem dry weight, number of flowering stems
- Notes: Dead/missing data indicated by *, and sample codes link across files to trace clone history and cytotype origin.
- Figure 1: Layout of clones in the common garden study and explanation of clone/sample codes (sd = clone propagated from a seedling).

## Practical GIS implications and considerations
- Enables mapping of cytotype distribution across Britain and Ireland at ~0.01° resolution, with links to phenology and growth data.
- Data integration opportunities:
  - Spatially align cytotype results with environmental layers (soil, climate, altitude) to analyze drivers of cytotype distribution.
  - Correlate first flowering dates and growth metrics with cytotype to explore reproductive and phenological patterns.
- Data quality and privacy:
  - Anonymized location data to protect site confidentiality; high-resolution coordinates may be replaced with coarse geographies.
  - Acknowledge potential sampling bias (single-plant sites, intensive sampling only in select hexaploid hotspots).
- Data management:
  - Cross-reference across multiple CSV files using clone/sample codes for comprehensive GIS analyses.
  - QC steps described (CV threshold, re-testing conflicting cytotypes) support reliable spatial extrapolation.

## References
- Doležel J, Greilhuber J, Suda J (2007). Estimation of nuclear DNA content in plants using flow cytometry. Nature Protocols 2(9): 2233-2244.
- Greilhuber J, Temsch EM, Loureiro JCM (2007). Nuclear DNA content measurement. In: Flow Cytometry with Plant Cells. WileyVCH: Weinheim, pp 67 - 101.
- McAllister HA (1972) The experimental taxonomy of Campanula rotundifolia L. Ph.D. thesis, University of Glasgow.
- Stevens CJ, Wilson J, McAllister HA (2012). Biological Flora of the British Isles: Campanula rotundifolia. J Ecol 100(3): 821-839.