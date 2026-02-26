# Live-trapping surveys of small mammals on arable field margins on the Hillesden estate in Buckinghamshire (England) during 2005-2011

## Overview (GIS-focused context)
- A long-term, spatially explicit study to assess small-mammal populations under three habitat-management types on the Hillesden estate (Buckinghamshire, central England).
- Treatments:
  - Cross Compliance (CC): narrow, unmanaged field margins; hedgerows cut annually.
  - Entry Level Scheme (ELS): 6-m margins with grass mix; one 0.25 ha patch for food resources; hedgerows cut biennially.
  - Entry Level Scheme Extra (ELSX): larger habitat mosaic (6-m margins with grasses and wildflowers), multiple patches with wild bird seed or wildflowers; hedgerows cut biennially.
- Study design: randomised block with five replicates; margins and habitat features distributed across blocks; villa-hedgerows and ditch boundaries provide contextual spatial features.
- GIS cues used in analysis: comparing hedgerow length within a 50 m buffer around sampling sites; finding no significant hedgerow-length differences across treatments.

## Survey design and spatial layout
- Temporal coverage: autumn sampling (November–December) in 2005, 2006, 2008, 2010 and spring sampling (May) following those autumns.
- Spatial sampling: two 100 m trap lines per replicate, positioned 1–2 m from field boundaries; lines run parallel to boundaries with traps spaced 10 m apart (11 traps per line; 22 traps per replicate per season).
- Margin types and locations: trapping conducted on 6 m wide ELS/ELSX grass margins and on 1–2 m CC margins within replicate blocks.
- Data collection scale: captures linked to precise field locations, enabling spatial aggregation by block, margin type, and habitat.

## Data structure and GIS-ready attributes
- Dataset size and scope:
  - 3172 trapping records, representing at least 1881 individual animals.
  - Most records are captures or recaptures; some records note trap activations without captures.
- Spatial and spatial-temporal fields:
  - x_coordinate, y_coordinate: start coordinates for each 100 m trap line.
  - Sampling_Block: block-level identifier (1–5).
  - Location: field names on the Hillesden Estate.
  - Trap_Line and Trap_Number: delineate the exact trap position within lines.
  - Date, Year, Season, Trap_Check_Time (Morning/Afternoon).
- Treatment and habitat fields:
  - Farming_Regime: Cross Compliance or ELS/ELSX.
  - Habitat: margin type (6 m ELS/ELSX margin vs 1–2 m CC margin).
- Individual animal data and tagging:
  - Species_English, Species_Scientific, Sex, Body_Condition, Weight_g.
  - Fur_Clip_or_PIT (tagging type); PIT_Tag_Code (unique ID for PIT-tagged animals).
  - Capture_Type (new or recapture; or a trap activated without capture).
- Data quality:
  - Records cleaned; missing values labeled as No_data.
  - Appendix-quality notes indicate occasional non-biological records (e.g., trap activations without animals).

## Data quality, processing, and caveats
- Data integrity:
  - Cleaning steps performed to remove errors; explicit handling of missing values.
- Spatial interpretation caveat:
  - Hedge/ditch management differences exist, but hedgerow length within a 50 m buffer showed no treatment-based differences, suggesting hedgerows were not a major driver of observed mammal numbers in this study.
- Interference considerations (Appendix: Corvids exploiting traps):
  - Corvids (Carrion Crows, Magpies) disturbed a subset of traps; 33% of transects affected, about 20% of monitoring visits, and 6% of traps.
  - Disturbances occurred mainly in daytime; potential bias for spatial capture data.
  - Interference persisted despite attempts to pin/bury traps; indicates a need to consider predator interference as a covariate or data QC factor in GIS analyses and when interpreting spatial patterns.

## Key GIS-relevant findings and implications
- The GIS-enabled comparison of habitat features (e.g., hedgerow length within buffers) across treatments showed no significant hedgerow-length disparity, indicating that observed differences in small-mammal data are less likely due to hedgerow quantity alone.
- The rich, coordinate-based dataset supports spatial analyses of small-mammal responses to habitat management, including:
  - Spatial distribution of captures by block and margin type.
  - Habitat-scale aggregations (6 m margins vs. narrow CC margins).
  - Temporal changes across autumn-spring cycles.
- Data structure supports creating map-based visualisations of: annual/seasonal capture density, species distributions, movement recursion (recaptures), and treatment effects at fine spatial scales (trap lines, field margins).

## Appendix: Corvid interference
- Observations indicate corvids actively disturbed Longworth traps, especially in certain transects and times of day.
- Practical limits to mitigation were found; this can inform GIS-based bias assessment, e.g., including trap interference as a covariate or flagging affected transects for targeted QC.

## References (context for GIS users)
- Related methodological and ecological references linked to Hillesden experiment, live-trapping practices, and hedgerow/biodiversity considerations.