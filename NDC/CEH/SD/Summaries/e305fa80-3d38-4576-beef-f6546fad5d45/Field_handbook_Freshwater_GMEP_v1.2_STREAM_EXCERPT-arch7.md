# HEADWATER STREAM SECTION ONLY

- This document outlines the AXIS II headwater stream and pond survey methods, designed to produce map-based data products for GIS users and stakeholders. It follows the Countryside Surveys methodology with minor updates and aligns with related manuals (CS2007, RHS 2003, DARES, MTR).

## Scope and study design (GIS-relevant context)

- Survey targets per square:
  - Headwater streams: 500 m watercourse surveyed; 100 m aquatic plant survey centered within the 500 m stream reach.
  - Ponds within squares: randomly selected ponds surveyed for water chemistry, macroinvertebrates, aquatic plants, and physical attributes.
- Data types collected for mapping and spatial analysis:
  - Water chemistry, diatom community, macroinvertebrate community, aquatic plant community, physical/hydromorphological characteristics (RHS), and pond environmental attributes.
- Data and locations are intended to feed GIS-based visualization and analysis, with standardized spatial referencing and attributes.

## Field methods and data capture (GIS-focused data layers)

- Water chemistry (Headwater Streams)
  - Ind indicative chemical sample collected downstream of the macroinvertebrate sampling area.
  - Measurements: conductivity and pH (field), alkalinity, SRP, TON (laboratory; filtered sample).
  - On-site protocol includes sample rinsing, filtration with 0.45 µm filters, and careful labeling for lab analysis.
- Diatom sampling (Headwater Streams)
  - Centered on RHS spot-check 6; samples from cobbles, emergent/ submerged macrophytes as substrata.
  - Substratum-based methods (A–D) depending on available substrates; preservatives (Lugol’s iodine) and proper labeling.
  - Environmental data collected alongside diatom samples; samples fixed, stored, and transported to CEH/Bowburn as appropriate.
- Macroinvertebrate sampling (Headwater Streams)
  - 4-minute main kick/sweep in a 10–15 m reach; habitats sampled in proportion to cover.
  - Sampling areas include surface searches and sub-surface searches; avoid collection of fish/amphibians; crayfish handled per guidance.
  - Sample preservation with 40% formalin; containers labeled; transport to CEH Bangor/APEM as appropriate.
  - Environmental data collected along the sample area (width, depth, surface velocity, substratum, bed features, shading, water clarity, presence of street lighting, etc.).
- Aquatic plant survey (Mean Trophic Rank, MTR) and macrophyte sampling
  - 100 m reach (50 m upstream and downstream of macroinvertebrate center) walked to record presence and percent cover of macrophyte/bryophyte species on a 9-point cover scale.
  - Biomass measurements: three samples of the dominant submerged species weighed after field processing.
  - Species identification to species level where possible; representative samples sent for lab confirmation; grapnel used to sample submerged plants where feasible.
  - Channel characteristics and environmental data collected, including fencing, slope, silt drape, wet weight, and biomass data, with modified DAFLOR scale for channel vegetation.
- River Habitat Survey (RHS) data collection
  - 500 m reach centered on the macroinvertebrate sampling site; field data entered electronically via RAPID.
  - Spot-check data (10 checks) include GPS coordinates, vegetation, substrate, channel geometry, banks, and features; A new set of AXIS II questions was added (weir/dam location, weir height, side bars, etc.).
  - Data validation and relocation features in RAPID to ensure consistency and accuracy; if RHS cannot be completed, reasons are logged.

## Data capture systems and GIS integration

- On-site digital data entry platforms:
  - RAPID for River Habitat Survey (RHS) data (500 m reach; spot-checks; Section D–K–L attributes).
  - RIVPACS electronic form for macroinvertebrate sampling environmental data and sample area measurements.
  - IRIS for aquatic plant (MTR) data collection (100 m reach) including species, cover, biomass, and physical attributes.
  - GIS-ready coordinates: GPS/NGR data collected to high precision; detailed relocation boards and photographs for future relocation.
- Data validation and submission processes:
  - On-site “Check Data” routines in RAPID and IRIS to validate completeness and consistency; fix errors as they’re found.
  - Centralized post-survey transport and processing with designated labs and partners (CEH Bangor, Bowburn, Wallingford, APEM).
- Data organization and storage:
  - Field specimens and samples labeled, stored, and transported per project safety and biosecurity requirements.
  - Transport Emergency Card (TREM) maintained for hazardous materials (formaldehyde) during road transport.
  - Final data and specimen handling follow established paths to CEH, Bowburn, and partner facilities; samples in different media routed to appropriate labs.

## Practical GIS considerations and outputs

- Spatial data structure:
  - 500 m RHS reach with 100 m MTR plant survey; exact sampling points and transects are geolocated and documented for GIS layering.
  - Diatom, macroinvertebrate, and macrophyte data linked to square/site IDs and NGR coordinates; sample dates and surveyor IDs accompany data.
- Attribute sets and scales:
  - Water chemistry: pH, conductivity, alkalinity, SRP, TON; sample-level metadata for lab tracking.
  - Diatoms: substrate type and collection method; preservation and environmental variables.
  - Macroinvertebrates: RIVPACS field data including width, depth, velocity, substratum, channel features, and DAFLOR vegetation coding.
  - Macrophytes: species presence and cover (9-point scale), biomass, and 100 m MTR data; species-level identifications where possible.
  - RHS: channel dimensions, bank features, slope, fencing, shading, bed stability, substrate types, and channel vegetation types using DAFLOR-like scaling.
- Visualization and analysis-ready outputs:
  - GIS layers for each component (water chemistry, diatoms, macroinvertebrates, macrophytes, RHS attributes) aligned to square-based spatial grids.
  - Relocation aids: site boards, photographs, and sketch maps enable accurate site re-location for future surveys.
  - Data products support policy and client-facing maps, habitat assessments, and biodiversity indicators.

## Quality assurance, challenges, and governance

- QA processes:
  - On-site validation (RAPID/IRIS) ensures completeness; images and sketch maps accompany data for robust relocation.
  - Standardized field protocols and instrument calibration (e.g., Hanna pH/Conductivity meter) to ensure comparability across sites.
- Common challenges to address in GIS workflows:
  - Data fragmentation across multiple datasets and labs; need for standardized metadata and harmonized coordinate systems.
  - Variability in dataset resolutions and formats; rigorous data cleaning and integration steps needed before GIS analysis.
  - Safety, storage, and sample transport considerations that influence data availability and timeliness.
- Documentation and references:
  - Methodological references include CS2007, RHS 2003, DARES, MTR, and associated CEH/NERC guidance.
  - Field checklists and field notes are essential for ensuring complete, relocatable GIS-ready datasets.

## Appendix: Safety, storage, and references (highlights for GIS workflows)

- Safety and handling:
  - Use of protective equipment; Lugol’s iodine preservative for diatoms; formalin for macroinvertebrates; TREM cards for hazardous shipments.
- Sample handling and storage:
  - Clear labeling, storage containers, and transport protocols to CEH and partner labs; long-term storage considerations for diatom, macroinvertebrate, and plant samples.
- References and standards:
  - Environment Agency RHS protocol, DARES diatom method, MTR plant survey, and related CS technical guidance.
  - Emphasis on standardization to enable reliable GIS-based comparisons across sites and years.