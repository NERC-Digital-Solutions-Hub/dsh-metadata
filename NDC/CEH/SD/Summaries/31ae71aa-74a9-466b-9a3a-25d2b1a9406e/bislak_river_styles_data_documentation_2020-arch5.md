# Section 1: Overview

- Purpose and scope
  - Data submitted for the Bislak River Styles Report and the paper “River Styles and stream power analysis reveal the diversity of fluvial morphology in a Philippine tropical catchment.”
  - Authors and timeline: analyses from March–October 2020; initial analyses by Tolentino, Perez, Guardian; River Styles classification reviewed by all authors; methods discussed in Section 2.

- Data types and structures
  - Segment-stream power shapefiles with computed stream power attributes.
  - River Style identification shapefiles (polygon for landscape units; polylines for isohyet and river styles).
  - Spreadsheets (.csv) containing stream power divided by River Style.
  - Supporting documentation CSVs detailing classifications across river styles (e.g., confined/ unconfined, braided, deltaic, bedrock/plains/low sinuous variants).
  - Extensive metadata fields and column naming conventions (e.g., FID, X, Y, Z, Strahler, Shreve, area_km2, dist_km, slope, chi values at various concavities, ksN, flow accumulation, distoutlet, stream power, segment identifiers, and river style name).

- Methods and data processing
  - TopoToolbox v2 used to extract the stream network and delineate catchment areas with a 1 km² upstream threshold to focus on alluvial channels.
  - Data cleaning: non-parametric quantile regression to remove artefacts; quantile carving along the central tendency; downstream elevations verified to decrease; mean slope averaged over 0.2 km segments.
  - Validation: stream network position checked against Google Earth imagery; ground-truthing and field verification for River Styles; longitudinal profiles interpreted with catchment/regional analyses.
  - Key equation: steady-state relation for constant total stream power (Ω = 0.44 χ A S) used to compute Ω for 0.2 km river segments.
  - River Style framework: Stage One procedural tree to classify river types based on confinement, planform, geomorphic units, and bed material; expert judgement and field checks underpin classifications.
  - Documentation and provenance: analyses by a named team with cross-author review; methods cited from established River Styles literature.

- Data governance, quality, and provenance
  - Ground-truthed, imagery-assisted, and field-verified data; explicit acknowledgement of expert judgment in River Style assignments.
  - Clear documentation of data outputs, variable definitions, and file naming conventions to support reproducibility and future reuse.
  - References provided for methodologies and framework (Brierley & Fryirs; Khan & Fryirs; Rhoads; Schwanghart & Scherler; Tadaki et al.).

- Usage, access, and attribution considerations
  - Data underpin a published report and provide a framework for replicating river-type classifications and associated hydromorphological analyses in similar catchments.
  - Metadata-rich dataset structure supports reuse and comparison across River Styles, with explicit attribute columns for downstream distance, area, slope, channel steepness indices, and stream power metrics.
  - Authors emphasize the role of expert judgement in River Style classification, which bears on reproducibility and potential need for methodological harmonization in future applications.

- References (method and framework context)
  - Brierley GJ, Fryirs KA (2005); Fryirs K, Brierley G (2018); Khan S, Fryirs KA (2020); Rhoads B (2020); Schwanghart W, Scherler D (2014, 2017); Tadaki M, Brierley G, Cullum C (2014).