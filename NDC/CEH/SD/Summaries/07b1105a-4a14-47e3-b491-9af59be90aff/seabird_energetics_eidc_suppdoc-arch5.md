# Time-activity budgets and energetics of common guillemot, razorbill, Atlantic puffin, and black-legged kittiwake

## Purpose and scope
- Detailed dataset of key behavioural and physiological traits for four seabird species during chick-rearing, an energetically demanding period impacting population demography.
- UK & British Isles focus; primary links to Isle of May long-term study (IMLOTS) and the Future of the Atlantic Marine Environment (FAME) project data (2010–2014).
- Aims to capture core metabolic costs and energy requirements, including links to prey intake rates for different prey classes.

## Data structure and content
- File: Seabird_energetics_parameters.csv
- Structure: single CSV with a first column named parameter and four subsequent columns for each species (Guillemot, Razorbill, Kittiwake, Puffin).
- Data rows represent 24 named parameters describing time-activity budgets and energetic costs; values include means (μ) and standard deviations (sd) where applicable.
- Parameter groups:
  - Time budgets (TB_foraging, TB_foraging_sd, TB_flying, TB_flying_sd, TB_resting_sea, TB_resting_sea_sd, TB_nest, TB_nest_sd)
  - Energetic costs for core behaviours (ER_foraging, ER_flying, ER_resting_sea, ER_nest, ER_warming_food, chick_ER, chick_ER_sd)
  - Chick-rearing and body metrics (CR_duration, init_mass, init_mass_sd, mass_change, tissue_en_dens, energy_prey_conv, assim_effic, assim_effic_sd, BMR)
- Units described per parameter (e.g., %time for time budgets; kJ day-1 for energetic costs; days for duration; g for body mass).

## Parameters, sources, and calculations
- Time budgets (1–8): derived from activity logger data and published studies; methods vary by species.
- Core-behaviour energy costs (9–12): calculated for a representative 24-hour cycle, using species-specific approaches and literature-based scaling (e.g., BMR-based conversions, diving-to-rest ratios, and nest-time costs).
- Warming of food, provisioning, and chick costs (13–15, 19–24): grounded in published metabolic and provisioning data; various scaling and dietary energy-density calculations apply.
- Diet and energy densities (20–21): prey energy densities estimated from diet composition (sandeel and clupeids) with year- and species-specific weighting (2010–2014) and conversion formulas.
- Biological metrics (16–18): chick-rearing duration and adult body masses sourced from long-term studies; mass-change estimates where available.
- Transparency on updates: some costs (e.g., rest-at-sea) recalculated when newer BMR values were available; detailed calculation notes provided in accompanying documentation.

## Provenance and documentation
- Primary data sources: Isle of May long-term study (IMLOTS), FAME project data (2010–2014), and numerous peer-reviewed sources for parameter calculations.
- Comprehensive references accompany the dataset, covering metabolic rates, foraging energetics, diet composition, and energy-density conversions.
- Documentation includes explicit sections on parameter calculations and sources, enabling traceability from raw observations to final parameter values.

## Quality control, storage, and access
- Quality control: described as part of the dataset documentation; data are consolidated in a single .csv file.
- Storage/access: stored securely with no shared access; currently restricted rather than openly accessible.
- Acknowledgement of contributors and funding sources provided; data lineage and sourcing are clearly cataloged.

## Data governance and sharing considerations for data stewards
- Metadata requirements:
  - Dataset title, authors, year, geographic scope, species, data collection period (2010–2014), and linkage to IMLOTS/FAME.
  - Clear definitions for each parameter, units, and whether values are means, sds, or both.
  - Provenance details, including primary data sources and methods used for calculations.
  - Licensing, access restrictions, and any embargo or embargo-like conditions (currently “no shared access”).
- Interoperability and cataloging:
  - Maintain a machine-readable data dictionary mapping each parameter to its meaning, units, and calculation notes.
  - Harmonize species naming, units, and date ranges to align with related seabird energetics datasets for cross-dataset discovery.
- Publication and discovery:
  - Consider assigning a persistent identifier (e.g., DOI) and publishing a dataset-level metadata record to improve discoverability.
  - Document and publish data lineage, processing steps, and version history to support reproducibility.
- Usage policies:
  - Clearly state access conditions given current secure storage; outline procedures for requesting access or for future data sharing, if policy changes.
  - Note temporal relevance (2010–2014 study period) and geographic scope (UK & British Isles) to guide applicability.

## Practical implications for reuse
- Suitable for studies on seabird energetics, chick-rearing energetics, and linking metabolic costs to population demography.
- Users should respect the restricted access status; any reuse requires appropriate permissions and adherence to provenance and licensing terms.
- When integrating with other datasets, ensure consistent units, species conventions, and time-frame compatibility.

## Limitations and caveats
- Access is restricted; ongoing sharing or redistribution is not described and may require authorization.
- Parameter values are tied to the 2010–2014 window and specific geographic context; applicability to other populations or periods may require recalibration.
- Several derived costs depend on literature-based scaling and assumptions; users should consider uncertainty in these calculations when conducting meta-analyses.

## References and related materials
- Extensive reference list accompanying the dataset, including key methodological sources for activity budgets, metabolic rates, energy densities, diet composition, and prey energy calculations.
- Core sources span Thaxter et al., Daunt et al., Harris & Wanless, Enstipp et al., Nagy, and the IMLOTS and FAME projects, among others.