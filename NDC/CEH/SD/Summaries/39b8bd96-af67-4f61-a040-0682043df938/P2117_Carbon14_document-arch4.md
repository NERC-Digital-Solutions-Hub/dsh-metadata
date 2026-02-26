# Measurements of carbon-14 transfer from plants to soil within mesh cores [NERC Soil Biodiversity Programme] Johnson, D., Leake, J. R., & Read, D. J. University of Sheffield

## Overview
- Describes a dataset from the NERC Soil Biodiversity Thematic Programme (established 1999) focusing on carbon-14 transfer from plants to soil within mesh-core experiments.
- Site: Sourhope field site, Kelso, Scotland (upland grassland turf) as part of a larger project on soil biodiversity, carbon and nitrogen cycles, and the roles of soil biota.
- Primary aims: understand soil biota diversity and functional roles in ecological processes; assess mycorrhizal networks and carbon/nutrient cycling.
- Dataset produced from a controlled experiment using mesh-bound cores to manipulate mycorrhizal access and trace carbon movement.

## Study and data collection highlights
- Experimental setup:
  - Mesh-bound cores inserted into turf to control mycorrhizal colonization (35 μm pore size nylon mesh; 22 mm diameter, 120 mm deep).
  - 16 cores across 8 turfs; cores were either static or rotated to alter hyphal connections.
  - Turfs maintained in controlled environment prior to labeling.
  - 14CO2 labeling: 1 MBq of 14CO2 administered for 3 hours in a gas-tight box; lactic acid used to generate labeled CO2.
  - Post-labeling sampling at multiple timepoints: 6, 20, 28, 42, 51, 70 hours.
  - Traps using NaOH absorbed respired 14CO2 for measurement.
- Measurements collected:
  - Concentrations of 14C in plant shoots, soil, and roots.
  - Amount of 14C transferred to soil via AM (arbuscular mycorrhizal) mycelium, and allocation to AM structures inferred by comparing static vs rotated cores.
  - Total above-ground biomass and soil/root sub-samples at the end of the experiment.
- Key findings (as summarized in the dataset description):
  - Initial shoot 14C content ranged from 103 to 245 nmol 14C per pot (mean ~183).
  - After 70 hours, shoot 14C content decreased by ~83% (from 62 to 10 nmol g dry weight).
  - Analyses used to estimate allocation of 14C to AM mycelium and to quantify transfer dynamics over time.

## Dataset structure and contents
- Dataset: 1079 14C transfer 1.0 (CSV) with the following schema:
  - SAMPLEID: Unique sample identifier.
  - SAMPLE_TYPE: Pot (whole pot), Rotated core, Static core.
  - SAMPLE_DATE: Date of sampling.
  - HOURS_POST_LABELING: Time since labeling (hours).
  - SHOOT_14C: 14C in plant shoots (nmol 14C g shoot dry weight-1).
  - RESP_14C: 14CO2 respired from cores (pmol 14CO2 h-1 cm-2).
  - SOIL_14C: 14C in soil within cores (nmol 14C g soil dry weight-1).
  - ROOT_14C: 14C in plant root-associated soil (nmol 14C g root dry weight-1).
- Data collection context:
  - Samples drawn from 8 turfs with 16 mesh cores, under both static and rotated conditions.
  - 14C content in plant material determined after drying and combustion, followed by liquid scintillation counting.
  - Headspace CO2 measurement captured in NaOH traps and quantified via scintillation counting.
- Data origin and timing:
  - Analyses conducted in August 2000.
  - Related outputs include total above-ground biomass, bulk soil, and fine-root sub-samples.

## Methods, materials, and data provenance
- Site and vegetation:
  - Grassland community: Festuca-Agrostis-Galium with notable AM associations; no fertilizer for at least 40 years.
- Core design and labeling protocol:
  - Nylon mesh cores (35 μm) used to permit hyphal in-growth while limiting root access.
  - Cores rotated in some pots to disrupt hyphal connections with host plants to distinguish AM-driven transfer.
  - 14CO2 introduced via a labeled box, with 14C tracing in plant tissue, soil, and emitted CO2.
- Post-labeling sampling and analysis:
  - Samples oven-dried, weighed, and analyzed for 14C content.
  - 14C allocation estimated by comparing static vs rotated cores.
- Quality control and data integrity:
  - Numeric range checks, formatting checks, and logical integrity checks implemented.
  - QA procedures applied, but data are provided without warranty of accuracy; NERC disclaims liability for use of the data.

## Metadata, standards, and governance considerations for Data Leaders
- Dataset identifiers and version:
  - Dataset: 1079 14C TRANSFER 1.0 (CSV)
  - Dataset notes indicate structured fields and units, facilitating discoverability and reuse.
- Data quality and caveats:
  - Explicit disclaimers about accuracy and liability; users should assess fitness for purpose.
  - QA steps present, but lack of formal warranty implies reliance on user validation for critical decisions.
- Relevance for data strategy:
  - Demonstrates end-to-end data capture from field experiment to structured metadata and analysis-ready schema.
  - Highlights the importance of documenting sampling methodology, core design, labeling protocol, timepoints, and tissue-specific measurements for reproducibility.
  - Illustrates the need for clear metadata around core conditions (static vs rotated) to support reuse and cross-study comparisons.
- References and supporting material:
  - Johnson, D.; Leake, J.R.; Read, D.J. (2001). Novel in-growth core system enabling functional studies of grassland mycorrhizal networks.
  - Johnson, D.; Leake, J.R.; Read, D.J. (2002). Transfer of recent photosynthate into mycorrhizal mycelium: short-term losses and accumulation.
  - Sourhope Field Data Handbook (2003) and related UK soil biodiversity literature (2006).

## Practical takeaways for data leadership and data management
- Ensure datasets include clear sample descriptors (static vs rotated cores) and timepoints to enable re-analysis of mycorrhizal transfer dynamics.
- Maintain a well-documented data schema with explicit units and measurement definitions to support cross-study integration.
- Include data provenance, methodological details, and QA notes to support trust and reuse, while communicating any limitations or liability considerations.
- Consider creating a versioned dataset, with accompanying data dictionary and references to related publications to facilitate discoverability and collaborative use across networks.