# Purpose To describe the sampling strategy and procedures for sample collection of human faecal, poultry caecal and environmental samples (water supply, wastewater, surface water, soil, animal manure, poultry pen litter) in the study Spatial and Temporal Dynamics of Antimicrobial Resistance (AMR) Transmission from the Outdoor Environment to Humans in Urban and Rural Bangladesh.

## Overview
- Describes the sampling strategy and procedures for three main categories of samples: human faecal, poultry caecal, and environmental samples (water supply, wastewater, surface water, soil, animal manure, poultry pen litter).
- Part of the Spatial and Temporal Dynamics of Antimicrobial Resistance (AMR) Transmission study in urban and rural Bangladesh.
- Two sampling rounds conducted in different seasons to capture temporal variation.

## Study design and sampling frames
- Sampling sites:
  - Urban live poultry markets
  - Commercial poultry farms
  - Rural households with domestic poultry
- Rounds:
  - Round 1 (winter)
  - Round 2 (summer)
- Scope per site:
  - Urban markets: samples from human participants, municipal water, market waste streams, poultry cloacal samples, and poultry pen surfaces.
  - Commercial farms: samples from farm workers, nearby low-exposure village residents, drinking water on the farm, poultry caecal and pen feces, downstream water bodies.
  - Rural villages: households in Mirzapur with high exposure (poultry owning) and low exposure (non-owning); environmental samples from tubewell water, soil, animal manure, poultry caecal samples when applicable, and downstream water bodies and waste streams.

## Sample types and collection details (high-level)
- Human samples: faecal samples from adults (urban markets, farms, rural households); stool collected within 2 hours of collection; stored on ice.
- Poultry-related samples: cloacal swabs, poultry pen litter, poultry drinking water; pooling and sterile handling as specified; samples stored on ice and transported to laboratory.
- Environmental samples:
  - Water: supply/tubewell water, tap water, wastewater, pond/river water, downstream river water; volumes typically around 500 ml for bottle collection; multiple collection points and pooling where indicated; immediate cold-chain transport.
  - Soil and manure: soil from household compound (approximately 20 g), fresh animal manure (~20 g), poultry litter (pooled ~20 g); sterile collection tools; samples placed on ice.
  - Solid waste: collected from market dustbins near wet markets; pooled (~20 g) in sterile bags; handled with new gloves.
- Downstream and shared facilities: some markets share water supply, wastewater, and solid waste facilities; in these cases, only one sample per market collected.
- Processing timelines: all samples transported on ice and processed in the laboratory within 12 to 24 hours of collection.

## Rounds and sampling cadence
- Round 1: 20 urban markets, 20 farms, 20 rural households (totaling 40 per site category across market/farm/household).
- Round 2: 20 additional urban markets, 20 additional farms, 20 additional rural households (total 40 per site category across market/farm/household).
- Total per round: 40 markets, 40 farms, 40 rural households.

## Data capture and ancillary measurements
- Geolocation: GPS coordinates recorded for downstream river sample locations.
- In-field measurements: pH, temperature, conductivity recorded where applicable.
- Documentation: detailed sample summaries include sample type, site, exposure status, and whether a sample is from a high- or low-exposure group.

## Data quality, governance, and documentation
- Standardization: use of sterile techniques, autoclaved tools, LifeGuard solution for certain samples, and consistent labeling.
- Chain of custody and tracking: explicit handling instructions (gloves, sterile containers, avoidance of sharp objects, pooling procedures).
- Ethics and privacy considerations: human samples collected from participants; implied need for ethical approvals and de-identification in data sharing (not explicitly stated but relevant for data stewardship).
- Documentation: procedures are formalized and linked to a specific NERC study reference (NE/N019555/1); field procedures and collection protocols are stated to support reproducibility and future data cataloging.

## Data stewardship implications and recommendations
- Metadata schema to support this study:
  - Sample-level fields: sample_id, sample_type (human stool, poultry cloacal, pond water, etc.), site_type (urban market, farm, rural household), site_id, round, exposure_group (high/low), date/time, collector_id, processing_time_since_collection.
  - Environmental context: GPS coordinates for relevant samples, water source type, downstream location, presence of shared facilities.
  - Laboratory readiness: storage_condition (ice, -20°C, etc.), transport_duration, processing_protocol references.
- Data quality considerations:
  - Ensure consistent units, volumes, and pooling conventions across sites.
  - Capture transport and storage timelines to assess sample integrity.
  - Maintain detailed SOPs, field forms, and data dictionaries to enable reproducibility and auditing.
- Privacy and ethics:
  - De-identify human participant data; document consent and ethical approvals; restrict access to identifiable information as appropriate.
- Data sharing and cataloging:
  - Plan for uploading datasets to appropriate portals; include data dictionaries, SOPs, and field forms to accompany data.
  - Document limitations, such as shared facilities affecting sampling independence and any missing or incomplete sample counts per site.

## Endnotes and references
- Sampling plan and procedures reference: NERC study NE/N019555/1.
- Scope includes multiple sample types and a multi-site, multi-round design to support analysis of AMR transmission dynamics.