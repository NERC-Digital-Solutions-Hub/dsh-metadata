# Documentation of shortlist of soil-based greenhouse gas removal practices selected following consideration of biophysical, economic and social impacts

## Overview
- Documents a shortlisted set of soil-based greenhouse gas removal practices (GGR) aimed at enhancing soil carbon sequestration (SCS) in agricultural land.
- Built on a multidisciplinary analysis of biophysical, economic, and social impacts; informed by literature and expert panel input.
- Emphasizes identification of practices with farm-level SCS potential and uptake feasibility, and situates findings within broader policy and review contexts.

## Data structure and fields
- Describes a dataset capturing measures across crops, regions, climates, rotations, and case studies, with harvested area (ha) as a key metric.
- Core table structure includes:
  - ID and description
  - Region-specific fields: IMAGE_region, Representative_of?, Rotated_with?, Case_study_country
  - Area_harvested_ha
  - A comprehensive set of measures (e.g., Erosion_control, Fire_management, Stocking_density, Pasture_renovation, Sward_management, Extend_perennial_phase, Reduce_bare_fallow, Cover_crops, Deep_rooted_plants, Nutrient_management, Organic_amendment_inc_grass_to_crops, Residue_management, Add_biochar, pH_management, Reduced_no_till, Water_management, Wetland_management, Agroforestry, Hedges)
  - For each measure: a corresponding comment_1 … comment_19 field capturing data source, provenance, and any caveats
- The data structure intentionally records measurement context, data sources, and caveats to support transparency and traceability.
- Metadata and provenance considerations highlighted as essential for data quality, verifiability, and future updates.

## Shortlist rationale and method
- GGRTs and SCS focus: soil carbon sequestration as a greenhouse gas removal technology within agriculture.
- Shortlist derived from:
  - Identification of practices with potential positive SCS impact at farm level and a plausible uptake rate globally.
  - Focus on mechanisms such as optimizing crop productivity (nutrient management, pH, irrigation), reducing soil disturbance (rotations, minimum till), minimizing carbon removal and erosion, adding external carbon inputs (organic amendments, biochar), and increasing internal carbon inputs (agroforestry, cover crops).
  - Consideration of economic and non-cost barriers, externalities, and governance/incentives affecting implementation.
  - Evaluation of whether existing scientific methods can quantify technical potential and externalities; recognition of barriers and incentives to adoption in global systems.
- Final shortlist results from a broader literature review complemented by expert panel input.
- Key sources:
  - Sykes AJ, Macleod M, Eory V, et al. Characterising the biophysical, economic and social impacts of soil carbon sequestration as a greenhouse gas removal technology. Glob Change Biol. 2020.
  - Macleod, M., Eory, V., Gruère, G., & Lankoski, J. (2015). Cost-effectiveness of greenhouse gas mitigation measures for agriculture: A literature review. OECD Publishing.

## Assessment criteria and key measures
- Primary aim: identify specific practices with potential to positively impact SCS at farm level and with uptake compatible with broader, global impact.
- Focus areas include:
  - Optimising crop productivity (e.g., nutrient optimisation, pH management, irrigation)
  - Reducing soil disturbance and improving soil physical properties (e.g., improved rotations, minimum till)
  - Minimising deliberate carbon removal and erosion-related loss
  - Adding carbon produced outside the system (e.g., organic amendments, biochar)
  - Providing additional carbon inputs within cropping systems (e.g., agroforestry, cover cropping)
- Broader considerations:
  - Economic and non-cost barriers, incentives, and externalities
  - Capabilities of current scientific approaches to quantify potential and externalities
  - Barriers and incentives to implementation in global agricultural systems
- The approach relies on a synthesis of existing literature and expert judgments, with detailed methodological description available in cited works.

## Implications for monitoring frameworks
- The data structure demonstrates how to organize, document, and track a diverse set of soil-based GGR measures, supporting transparent monitoring and evaluation.
- Highlights governance and data management needs critical to monitoring:
  - Data access and timeliness to overcome data gaps and silos
  - Public sharing of underlying datasets vs. barriers to openness
  - Metadata completeness and clarity to enable verification and reuse
  - Data transformation and standardization requirements to ensure comparability
  - Data quality assurance, cleaning, transformation, and analysis processes
  - Clear communication of complex findings to stakeholders
  - Implementation of data governance to keep datasets up to date and properly stored
- Practical guidance for monitoring frameworks:
  - Adopt structured data schemas with explicit fields for region, crop, rotation, case study, area harvested, and a comprehensive set of measures with source-annotated comments
  - Incorporate mechanisms for updating data provenance, metadata, and data sources
  - Ensure outputs (reports, charts, dashboards) transparently reflect underlying data and governance processes
  - Engage stakeholders throughout data collection, verification, and dissemination

## References
- Sykes AJ, Macleod M, Eory V, et al. Characterising the biophysical, economic and social impacts of soil carbon sequestration as a greenhouse gas removal technology. Glob Change Biol. 2020. https://doi.org/10.1111/gcb.14844
- Macleod, M., Eory, V., Gruère, G., & Lankoski, J. (2015). Cost-effectiveness of greenhouse gas mitigation measures for agriculture: A literature review. OECD Publishing. http://doi.org/10.1787/5jrvvkq900vj-en