# UKCEH Countryside Survey 2021

- Purpose and scope
  - Large-scale vegetation monitoring to quantify changes in countryside by habitat type and location.
  - Data collected from vegetation plots using two sizes: 200 m2 vegetation plots and 4 m2 soil/vegetation plots (nested within the 200 m2 area).
  - Digital data collection via ESRI Survey123 (Vegplots) and Collector apps; paper plot maps retained for relocation.

- Data collection framework
  - Plot location and relocation
    - Plots are repeatedly surveyed across years; precise relocation relies on GPS, sketch maps, and photos.
    - Plots are marked with metal plates or wooden stakes; if not found, relocation is marked with attention to the degree of relocation error.
    - If a plot cannot be relocated satisfactorily, it is recorded as Not Found and may be replaced as a New Plot.
  - Plot header and metadata
    - Each plot has header information: square, plot type (X = 200 m2, XX = 4 m2 soil), plot number, and Plot ID (auto-generated).
    - Surveyors recorded names/initials, habitat context, slope, aspect, and precise location (geopoint via GPS with accuracy indicators).
    - Plot relocation status (Found, Not Found, New Plot, Access Denied, Too Dangerous, etc.) and notes describe disturbances or land-use changes.
  - Plot maps and photos
    - Plot sketch maps and photos are required to aid future relocation and to document changes; photos should reference distinctive nearby features for re-finding.
    - Sketch maps must include GPS reference point and north arrow; redraws/edits are documented in the software.
  - Data capture workflow
    - Collector app: navigate to a plot using a map, then open a form in Survey123 to enter data.
    - Survey123: used for entering header information, plot-specific headers, and species data; supports offline editing with auto-save.
    - Data submission: online submission via Send Now; offline work stored in Drafts/Outbox; resubmission via Copy to new survey if needed.

- Plot types and layout
  - X plots (200 m2 vegetation plots)
    - Five predetermined random positions per square (X1–X5).
    - Vegetation nest is 14.14 x 14.14 m (200 m2) with nested sub-squares to capture species presence and cover.
    - Laying out the 200 m2 plot uses diagonals and strings; orientation aligned to north/south and east/west axes.
  - 4 m2 plots (Soil/NEST)
    - Nest 0 is the innermost 2 x 2 m area; nests 1–5 expand outward to cover the full 4 m2 nest within the 200 m2 plot.
    - Nested sampling captures presence and cover for vascular plants, bryophytes, and other ground features; total cover aims for about 100% (allowing layered vegetation).
  - Nest-based recording
    - Nest 0: species in inner 2x2 m area; list of species and cover estimates.
    - Nest 1–Nest 5: additional species found as the nest area expands; total species list is built cumulatively.
    - Bryophytes and lichens: limited to listed taxa; major bryophytes recorded; full bryophyte lists are constrained to standard sets.
  - Data entry specifics
    - Species are entered via dropdowns with auto-type; “Other” option allows free-text entries for unidentified species (to be corrected later).
    - For each species, cover is recorded; total cover across nests should reflect the entire plot.
    - Special notes for species identifications, habitat context, and disturbances can be added in notes fields.

- Data quality, validation, and standards
  - Data validation
    - The software enforces required fields and prompts for missing information before submission.
    - Caution against blank or duplicate species entries; summary totals and species counts are provided to aid QA.
  - Standardization and aggregation
    - Aggregations/combination taxa used to maintain consistency with historical data where species identification is uncertain.
    - Emphasis on recording to species level where possible; where not feasible, accepted combinations are used (per BRC list).
  - Habitat and vegetation classification
    - Broad Habitat (BH) and Priority Habitat (PH) codes are assigned to plots and wider polygons as part of habitat mapping and reporting.
    - Habitat descriptions range from Broadleaved woodland, coniferous woodland, arable/horticulture, various grasslands, bog, fen/marsh, to urban and coastal habitats.
    - Special note on how to classify areas affected by logging/clear-felling (record current habitat rather than future land-use).

- Appendices and supporting resources
  - Appendix I: Generic references for Collector and Survey123 (installation and usage guidance).
  - Appendix II: Random numbers between 0 and 1 (used for sampling guidance).
  - Appendix III: Plot types historically recorded in each square (Areal, X, Y, U, etc.).
  - Appendix IV: Habitat descriptions and priority habitat guidance (for Habitat Key codings and PH allocation).

- Practical considerations and challenges (from an analyst’s perspective)
  - Data at the right scale and local detail is critical; relocation accuracy directly affects data usability for detecting vegetation change.
  - Access issues, land-use changes, and habitat heterogeneity influence plotting strategy and relocation success.
  - Integrating data from multiple plots, nested nests, and variable taxonomic resolution requires careful QA and consistent metadata.
  - Offline data collection and synchronization processes are essential to minimize data loss; robust metadata and audit trails support reproducibility.
  - Detailed habitat classification supports downstream reporting (e.g., biodiversity indicators and Priority Habitat assessments) but requires careful adherence to the Habitat Key guidance.

- Outcome and deliverables
  - A longitudinal, high-resolution dataset documenting vegetation presence, abundance, and habitat context across England, Scotland, and Wales, suitable for trend analysis, habitat-based reporting, and statistical modeling of vegetation change.