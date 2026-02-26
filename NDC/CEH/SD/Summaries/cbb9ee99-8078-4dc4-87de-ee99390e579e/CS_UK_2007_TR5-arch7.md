# HEADWATERS

- Purpose and scope
  - UK Countryside Survey 2007 headwater component.
  - Re-survey headwater streams in 425 CS2000 squares; elements include macroinvertebrate community (RIVPACS), hydromorphology (River Habitat Survey, RHS), physical characteristics, and water chemistry.
  - In CS2007, 25 squares contain new headwater sampling sites on smaller watercourses to improve focus on headwaters; sampling length is defined and nested within survey design.

- Spatial design and sampling framework
  - Headwater sampling site length: 500 m of watercourse; the 500 m defines RHS sampling reach.
  - Hydromorphological and macroinvertebrate sampling centered on RHS spot-checks; RHS section is 500 m long and centered on the macroinvertebrate sampling site when possible.
  - In each of the 425 squares from CS2000, core elements (macroinvertebrate score, RHS hydromorphology, water chemistry) are re-surveyed; an indicative 50 m aquatic plant stretch is included within the 500 m RHS reach.
  - Random pond sampling in CS2007 squares containing ponds: aquatic plant community, physical characteristics, and water chemistry.

- Data collection and field workflows
  - Macroinvertebrate sampling (RIVPACS-based)
    - Target: widest possible taxa range within a single continuous sampling area (5–15 m, depending on stream width).
    - Method: 3-minute kick-sampling with a 25 cm2 pond-net (900 μm mesh) plus 1 minute of manual searching; multiple habitats sampled proportionally to their cover.
    - Sample handling: keep material damp; fix and preserve in formalin; label and bag samples; avoid cross-contamination of nets; standard field data forms (RIVPACS Sample Area Form) used for environmental data.
  - Water chemistry sampling
    - Indicative chemical sample collected downstream of macroinvertebrate area before biological sampling.
    - Measurements: conductivity and pH on-site; SRP, TON, alkalinity from filtered water (0.45 μm syringe filters); standardized bottle labeling and handling.
  - Hydromorphology and habitat data (RHS)
    - RHS 2003 protocol used; data captured in the field via RAPID (tablet-based) to enable validation on-site.
    - Data types include spot-checks, channel attributes, bank condition, vegetation, substrates (including four substrate size classes), habitat types (POOL, RUN, RIFFLE, SLACK), shading, and water clarity.
  - Aquatic macrophyte survey (MTR)
    - 100 m reach centered on macroinvertebrate sampling point; wading or grapnel retrieval depending on depth; species presence and percent cover (9-point scale) recorded; specimens collected for lab confirmation when needed.
  - Data capture systems
    - RHS data: RAPID (MS Access on Tablet PC); on-site validation, square selection, and data export to CEH systems.
    - Aquatic plants: IRIS (MS Access on Tablet PC) for macrophyte data; on-site validation and plant specimen handling; lab confirmation where required.
    - Macroinvertebrate data: primarily paper forms (RIVPACS) with field guidance; later integration into RIVPACS-based databases.
  - Photographs and relocation
    - Required photos of macroinvertebrate sampling area and RHS reach; marker boards clearly labeled for relocation in future surveys.
  - Data quality and governance
    - On-site validation via RAPID/IRIS; data audits (~7% of headwater sites) by CEH staff; cross-team data quality checks; standardized workflow to minimize drift over time.

- Metadata, identifiers, and spatial data outputs
  - Spatial identifiers: CS square numbers; precise GPS/NGR for macroinvertebrate sampling points (8-digit National Grid Reference).
  - Data models and outputs: RHS data (RAPID) and aquatic plant data (IRIS) feed into centralized databases; macroinvertebrate data linked via RIVPACS forms.
  - Data management: field data validated on-site; samples fixed, labeled, and stored for transport to CEH Dorset; transit documented with Transport Emergency Card (TREM) for fixatives.
  - Data consolidation and sharing: fieldsheets and samples dispatched monthly; data integrated into CEH Dorset processing workflow; outputs suitable for GIS-based mapping and policy/product development.

- Logistics, safety, and governance
  - Two-person field teams; health and safety considerations for sampling in streams; on-site risk assessment and decision rules for unsafe conditions.
  - Use of standardized field equipment and digital data entry; on-site validation to ensure completeness before leaving site.

- Key takeaways for GIS use
  - Spatial resolution and scope: 500 m RHS reaches across 425 squares; headwater sampling designed for consistent, georeferenced site relocation and comparability across years.
  - Data fusion potential: integrate RHS hydromorphology, macroinvertebrate scores, water chemistry, and macrophyte data into multi-layer GIS datasets; per-square and per-reach summaries enable habitat-quality and bioassessment maps.
  - Open data pathways: on-site tablet-based data capture (RAPID/IRIS) facilitates timely GIS-ready datasets; standardized naming (CS square, pond/sampling IDs) enables robust joins and data lineage.
  - Relocation and reproducibility: explicit relocation features (photos, fixed marker boards, sketch maps) support reproducible mapping and change detection over time.

- Related pond condition component (CS2007)
  - Pond mapping and condition surveys: identification of ponds within each CS square; boundary delineation based on maximum winter water level; survey pond selected per square for macrophyte, environmental characteristics, and water chemistry assessment.
  - Macrophyte and habitat assessment: 100 m macrophyte survey length; species presence, abundance, and coverage of submerged, floating-leaved, and emergent types; shading and surrounding land use documented.
  - Data capture and workflow: pond condition sheets and MTR-style macrophyte surveys; specimens sent for lab confirmation where needed; field data validated and compiled for downstream GIS use.
  - Outputs: pond boundary geometries, area estimates, turbidity, depth, sediment composition, pollution indicators, inflows/outflows, and surrounding land-use metrics suitable for pond-focused GIS products.