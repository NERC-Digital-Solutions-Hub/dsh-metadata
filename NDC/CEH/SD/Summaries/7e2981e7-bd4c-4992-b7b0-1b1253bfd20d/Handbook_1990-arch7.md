# COUNTRYSIDE SURVEY 1990

- Purpose and scope
  - National land-use/land-cover monitoring project using the ITE Land Classification System.
  - Aims to provide current, ground-truth data to link top-down remote sensing with field observations; supports trend and process analysis in rural environments.
  - Two-tier approach: satellite/remote-sensing groundwork plus extensive bottom-up field survey for ground-truth data and pattern detection.
  - 1990 resurvey plan: 512 sample squares (six ITE stations), with 128 new squares and 128 previously surveyed squares; enhanced data capture with additional vegetation and habitat information; standardization across observers to improve statistical accuracy of change data.

- Data model and GIS readiness
  - Primary data product: Field Assessment Booklet (FAB) per square, combining mapping, quadrat data, and sampling; maps at 1:10,000 scale (enlarged 6" sheets) with coded annotations.
  - Data encoding system: map annotations use primary and secondary codes; alpha codes summarize multiple numeric codes to save space while preserving detail; two code types (primary and secondary) with dominant primary code prioritized.
  - Universal codes and structured fields cover: ownership, farmer information, physiography/inland water/coastal features, ground cover, vegetation types, boundary types, buildings/structures/communications, and land use categories.
  - Vegetation and habitat data are captured via standardized plot types and templates, with explicit guidance on unit size, minimum mapping units, and coding rules to ensure consistency across squares.
  - API (Aerial Photograph Interpretation) guidance provides non-ground truth cues (e.g., boundaries, isolated features) to aid ground surveys, with clear caveats to rely on field evidence when conflicts arise.

- Survey design and data collection workflow
  - Sampling design
    - 512 squares total, divided into six teams; each square expected to yield detailed land-cover and landscape data.
    - Large quadrats: five 200 m2 quadrats per square (set on a grid, with center-of-gravity placement chosen to represent habitat).
    - Small quadrats: five 2 m x 2 m quadrats to sample natural/semi-natural vegetation types.
    - Up to five linear plots in enclosed land (boundary plots near hedgerows, streamsides, and roadsides) to capture linear habitat variation.
    - Additional linear plots for hedgerows, streams/rivers, and road verges (including extra verge plots to cover road types).
    - Location/relocation rules to adapt to land-use changes since 1977/78, ensuring plots remain representative and non-overlapping.
  - Field procedures and documentation
    - On arrival: assess area, obtain access permissions, plan comprehensive coverage, and ensure no omissions in data collection.
    - Record keeping via FABs with careful, neat completion; every page labeled with square number; caution to avoid ambiguity in interpreting codes.
    - Field decisions are final; deviations require notes or comments on FABs.
    - Aerial photo interpretation and field evidence are reconciled on maps; in the field, boundaries and units are delineated with clear end-points and perpendiculars.
  - Permissions and landowner engagement
    - Pre-visit letters to landowners; plan site visits with sensitivity to landowner relations.
    - If access is refused, predefined procedures determine whether to abandon the square, continue partial survey, or relocate to a new square.
    - Ownership and farmer information recorded on FABs to facilitate future surveys and introductions, with governance scoring for cooperativeness (0–3 scale).

- Data capture schemas and attribute encoding
  - FAB structure
    - Front/middle pages include: square number, location, ownership, farmer information, physiography, inland/water/coastal features, land cover categories, boundaries, and built features.
    - Detailed instructions for coding: primary and secondary codes, correct order (dominant uses first), and use of alpha codes to summarize multiple codes.
    - Special attention to boundaries: actual vs. interpreted boundaries; mark “no longer present” with 999; ensure edge coding and minimum unit sizes are adhered to.
  - Vegetation and land-cover coding (6.2.2)
    - Standardized vegetation plot recording with a fixed form (header attributes, list of common species, nested quadrats, cover estimates in 5% bands, and sketch/maps).
    - Plot types: large 200 m2 quadrats with nested 4 m2/quadrat entries; five 2 m x 2 m small quadrats per square; linear plots for hedgerows, streamsides, and roadsides; boundary plots adjacent to boundaries; and extra plots for verges and aquatic habitats.
    - Species lists and combinations: a curated list of 200 common species; allowances for species combinations where identification is uncertain; restricted list of bryophytes and lichens for inclusion.
    - Data integrity rules: final cover estimates per quadrat; up to three cover codes for mosaics; age, height, and canopy notes where relevant.
  - Data integration and outputs
    - Data captured in FABs feed into GIS layers: vegetation/land-cover types, boundary networks, road verges, hedgerows, water bodies, physiography, and land-use classes.
    - Universal codes map to map features and support cross-square comparability over time.
    - Aerial interpretation and field data jointly inform boundary delineation and feature identification.

- Fieldwork logistics and equipment
  - Equipment provided by Merlewood: FABs, aerial photos, site maps, project handouts, weatherproof clipboards, colored pens, survey poles, markers, sampling gear, tape measures, navigation aids, and identity cards.
  - Local ITE stations provide site maps, pencils, reference books, cameras, hand lenses, film, First Aid, and personal gear.
  - Photography: print films used to photograph vegetation plots; plot numbers clearly marked for reference.

- Data quality, standards, and challenges
  - Emphasis on standardization to reduce observer variation; field handbook is a prerequisite for consistent data recording.
  - Challenges include data scattered across many locations, lack of data at useful resolutions, inconsistent data standards, and the effort required to clean and transform data for GIS use.
  - 1990 procedures include quality control measures to maintain recording consistency across observers and years.
  - Practical field constraints: complex mosaics, varying land-use changes, and need for rapid, on-site decision-making to avoid transcription errors.

- Post-survey procedures and governance
  - After each survey day, teams review FABs to ensure completeness; data are transposed to updated maps only if necessary due to damage or loss of original sheets.
  - FABs and samples are returned to ITE stations promptly for processing and archival.

- Special survey components
  - Freshwater biota sampling (IFE and NELUP)
    - Two standing-water biota sampling systems per square (freshwater biota from flowing waters and standing waters); sites chosen to reflect typical square habitats (lakes/lochs, ponds, dried streams, calcareous/acid flushes, Sphagnum bogs, etc.).
    - Samples collected with a sieve, preserved in formalin, labeled with square, date, and surveyor; transported to Merlewood for processing.
  - Photography and mapping integration
    - High emphasis on photographic documentation of vegetation plots for reference and validation.

- End-state and intended GIS outputs
  - A suite of map layers and attribute tables derived from the FABs covering:
    - Land use/land cover categories and mosaics
    - Physiography, inland water, and coastal features
    - Boundaries (fences, walls, hedges, banks, ditches)
    - Woodlands/forests and trees with age, canopy, and condition attributes
    - Buildings/curtilages, roads, verges, and designated/non-designated recreational areas
    - Sampling plots (large quadrats, small quadrats, boundary/linear plots) with precise locations and associated vegetation data
  - The standardized coding system facilitates cross-year comparability and supports change detection analyses within a GIS framework.

- Temporal context and evolution
  - Builds on earlier ITE surveys (1977/78 and 1984) with additional emphasis on standardization and a two-tier sampling approach.
  - Ongoing resurvey (1988 baseline data used for ECOLUC) informs the 1990 protocol and future monitoring cycles.
  - The Handbook and coding standards are designed to preserve continuity across successive survey waves and to enable robust time-series GIS analyses.