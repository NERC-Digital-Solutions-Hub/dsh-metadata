# Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UKSSPs) and climate projections (UK-RCPs)

## Data access and licensing
- Data are available from the provided DOI: https://doi.org/10.5285/f9ab3051-4f85-415f-b691-371ff8e951f2
- Licensed under the Open Government Licence; users must cite Brown et al. (2023) when reusing the dataset.
- Hosted data reference: NERC Environmental Information Data Centre (EIDC); dataset cited as Brown et al. (2023) with associated links.

## What the dataset represents
- Description: Future land use projections for Great Britain produced by the CRAFTY-GB agent-based model, at 1 km2 resolution, aligned with linked UK-RCP climate projections and UK-SSP socioeconomic pathways (SSPs), for decadal timesteps from 2020 to 2080.
- Scope: Six SSP-RCP scenario combinations (e.g., RCP2.6-SSP1, RCP4.5-SSP2, etc.) used to explore climate and socio-economic influences on land use, integrated within a global modelling context to account for UK trade and global change.
- Output format: For each SSP-RCP scenario, 1 km grids provided as stacked raster files with seven bands representing land use at each decadal timestep (2020–2080).

## Data structure and content
- Land Uses (agents): Represented as indices -1 to 15, mapping to specific land use agents (Unmanaged, Agroforestry, Bioenergy, Intensive/Extensive arable, Intensive/Extensive pasture, Sustainable Arable, Very Extensive Pasture, Urban, various productive native/non-native forest types, Bioenergy, Agroforestry, etc.).
- Agent typology: Includes arable, pastoral, forest, and combined classes (e.g., bioenergy, agroforestry) to capture a continuous spectrum of management intensities.
- Capitals and drivers: Model inputs are diverse capitals (human, social, manufactured, financial, natural) used by land-use agents to provide ecosystem services. Natural capital is split into yields/suitabilities for arable, pastoral, and forest uses.
- Spatial extent: GB only; data for Northern Ireland not included due to data constraints.
- Urban areas: Projected via a separate urban allocation model using SSP-specific parameters and land exclusions (protected areas, flood risk) with decadal updates to 2100.

## Data creation and methods
- Modelling framework: CRAFTY-GB, an application of the CRAFTY agent-based framework, calibrated for the British context with inputs drawn from observational data and stakeholder-informed scenario assumptions.
- Data inputs and structure: Capitals provide location-specific drivers; protected areas constrain land-use change; urban areas are modeled separately; demand for ecosystem services and their valuations drive competition among land-use agents.
- Services and demand: Ecosystem services include provisioning, regulating, cultural services, biodiversity, landscape diversity, carbon sequestration, recreation, and employment; service demand levels are guided by UK-RCP-SSP scenarios.
- Scenario integration: Each of the six cross-SSP-RCP scenarios informs parameters, active model processes, and policy objectives, enabling a range of plausible futures.
- Key data sources: UK-SSP, UK-RCP scenario descriptions; ESC yield classifications; LCM2015; NFI; CEH Land Cover Plus data; UKCP18 climate data; urban projections; and related supporting information (S1–S8) referenced in Brown et al. 2022.

## Data files and technical notes
- Six SSP-RCP scenarios: Each scenario provides a 1 km stacked raster with seven bands per decadal timestep (2020–2080).
- Land Use Agent Indices: A detailed mapping table (Unmanaged to Urban, plus various forest and agricultural classes) is provided to translate indices to agent names.
- Initial allocation: Allocation of land-use types (e.g., intensive arable for food, extensive pastoral, various forest types, urban) is based on LCM2015 and NFI, with random or specified spatial placement within constraints.
- Intensity mapping: A continuous land-use intensity mapping approach was developed to aid interpretation, combining inputs, technology, and production levels to produce per-scenario color saturation in visuals. Intensity scalars by SSP (Table 4) are provided for 2020–2080, applicable to IA/EA and IP/EP classes, and are SSP-specific.
- Data gaps and processing: Coastal/island data gaps addressed with regression or nearest-neighbor approaches; 2020 inputs normalized to baseline where inconsistent; boundary smoothing applied.

## Data quality, provenance, and validation
- Model evaluation: TRACE-based evaluation documented in Supporting Information S2 (Brown et al. 2022); combines unit tests, sensitivity analyses, comparisons to empirical data and other models, and public access to model code and outputs via landchange.earth/CRAFTY.
- Validation approach: Cross-checks of agent typology against independent datasets (LCM2015, EUNIS habitat classifications, CEH Land Cover Plus: Fertilisers and Pesticides) to assess representativeness of land-use types and initial distributions.
- Limitations: Historical reproduction validation not performed due to lack of temporally consistent UK land-cover data; full spatio-temporal validation of every agent type is not targeted but the typology is deemed broadly appropriate for the study aims.

## Governance, reuse, and metadata considerations
- Licensing and citation: Open Government Licence; proper citation required as specified by the dataset authors for any reuse.
- Documentation and supporting materials: Comprehensive documentation available (Brown et al. 2022; Supporting Information S1/S2; related methodological papers) to support understanding of model structure, data derivation, and scenario parameters.
- Reproducibility: Model is openly accessible (https://landchange.earth/CRAFTY) with interactive exploration, facilitating replication or adaptation under similar UK contexts.
- Data scope and maintenance: Dataset covers Great Britain only; updates or extensions to include Northern Ireland would require additional data and calibration.

## Key considerations for data stewards
- Data provenance and lineage: Clear traceability of inputs (SSP/RCP descriptions, urban projections, land-cover datasets) through to final stacked rasters and agent-intensity representations.
- Metadata completeness: Ensure documentation includes scenario definitions, band ordering, decadal mapping, agent-to-name mappings (Table of Land Use Agents), and intensity scalars (Table 4) for proper interpretation.
- Interoperability and formats: Raster stacks with seven bands per decadal step; ensure compatibility with GIS workflows and visualization tools; preserve unit conventions and index mappings.
- Access, licensing, and attribution: Maintain Open Government Licence compliance and explicit citation requirements; provide stable DOI and dataset versioning if updates occur.
- Reuse constraints: GB-only scope; note data gaps handling and normalisation steps that may affect cross-border comparisons or integration with NI data.
- Quality assurance: Leverage TRACE-based evaluation summaries and contextual validation against independent datasets; document any caveats or uncertainties arising from scenario assumptions or data gaps.

## References and further reading
- Brown, C.; Seo, B.; Alexander, P.; et al. (2023). Decadal maps of multiple alternative future land use based on UK Shared Socioeconomic Pathways (UK-SSPs) and climate projections (UK-RCPs). NERC Environmental Information Data Centre. Dataset.
- Brown, C.; Seo, B.; Rounsevell, M.D.A. (2022). Agent-Based Modeling of Alternative Futures in the British Land Use System. Earth's Future.
- Supporting Information S1–S2; related methodological and evaluation literature cited within the document.