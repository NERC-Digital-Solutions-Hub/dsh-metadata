# Organic waste flows and nutrients stocks and flows in Leicestershire and Leicester: a Material Flow Analysis

## Overview and scope
- Maps nutrient (nitrogen and phosphorus) flows embedded in regional organic waste streams (N and P in tonnes) for Leicestershire County and Leicester City.
- Types of waste mapped: green waste, food waste, on-farm slurry/manure, and wastewater (excluding run-offs due to data limitations).
- Time basis: 2019 data used as the baseline; study conducted July 2022–July 2023.
- Primary aim: quantify how nutrients are distributed along the waste journey to identify intervention points for improved resource management and environmental performance.
- Output: Sankey diagrams and accompanying spreadsheet data to show raw waste streams, processing/disposal outputs, and nutrient contents.

## Data sources and provenance
- Primary data sources:
  - Waste Data Interrogator (Environment Agency, 2019): waste received and removed; origin by Waste Planning Authority; European Waste Catalogue codes; limitations noted in precision of some destinations.
  - Severn Trent: wastewater volumes (data for 2022, with adjustments to reflect annual average 125 million tonnes due to seasonal variability).
  - Defra and UK datasets: on-farm slurry/manure volumes by livestock and land use.
  - ONS and WRAP/other sources for household/non-household waste assumptions.
- Data types:
  - Raw waste stream quantities (tonnes/year).
  - Processing/disposal options (e.g., composting, anaerobic digestion, landfilling, incineration, wastewater treatment).
  - Output stream quantities post-processing and nutrient contents (kg N, kg P per material).
- Data handling notes:
  - Some EA codes were imprecise, necessitating assumptions to determine destinations.
  - Transfers, storage, or non-treatment destinations could lead to double-counting if not carefully scrutinised.
  - Household food waste and non-household food waste flows required estimation and assumptions due to data gaps in EA dataset.

## Data collection, processing, and modelling
- Methodology:
  - Material Flow Analysis (MFA) to map stocks and flows of nutrients within regional waste streams.
  - Processing Unit (PU) modelling to perform mass balances for outputs (e.g., AD, composting, incineration, wastewater treatment).
  - Quantitative modelling supported by literature data from UK/Western Europe for representative PU performance.
- Data processing details:
  - Green waste: destinations determined by county vs city coding schemes (Tables 1.1–1.2).
  - Food production/processing waste: destinations determined by Tables 1.3–1.4 with assumptions for AD vs composting and land application.
  - Food consumption waste: household waste estimated using per-household generation rates and distribution derived from residual waste patterns (landfill vs incineration; some region-specific notes on AD).
  - Slurry/manure: on-farm application quantities and destinations drawn from Defra datasets.
  - Wastewater: main stream treated by Severn Trent; septic tank sludge included; nutrients tracked through treatment processes including AD and sludge handling.
- Outputs:
  - Sankey diagrams illustrating regional and intra-regional nutrient flows (Figures 1.5–1.9) and distribution of N and P across sources/sinks (Figure 1.10).

## Data quality, limitations, and uncertainty
- Key limitations:
  - Data availability constraints limited coverage of losses, chemical changes during transport/storage.
  - Imprecise EA destination coding required assumptions; potential for misclassification and double-counting.
  - PU modelling relies on literature-derived, point parameter values rather than ranges; real-world variability not fully captured.
  - Scope limited to waste streams; run-offs, imports/exports of nutrients, and fertilizer inputs are not included, reducing completeness of regional nutrient circularity assessment.
- Uncertainty handling:
  - Acknowledged reliance on representative point values; results should be treated with caution and as indicative.
  - Suggestions for future work to incorporate broader nutrient flows and data ranges.

## Outputs and stakeholder engagement
- Stakeholder workshops:
  - First workshop (July 2022) developed system understanding, identified key sources, links, and bottlenecks; produced a nutrient flow map (Figure 1.1).
  - Second workshop (Feb 2021) explored technical, economic, environmental, and regulatory issues, data gaps, and potential options viable for Leicestershire.
- Deliverables:
  - System maps (Figure 1.2 and associated figures) and a set of Sankey diagrams illustrating green waste, food waste, slurry/manure, and wastewater flows (Figures 1.5–1.9).
  - Distribution of N and P across identified sources and sinks (Figure 1.10).

## Data governance implications for Data Stewards
- Provenance and traceability:
  - Clear documentation of data origins (EA Waste Data Interrogator 2019, Severn Trent 2022, Defra datasets, ONS, WRAP) and the specific sheets/tables used.
  - Explicit notes on decisions made where coding was imprecise (assumptions for destinations, especially in routing waste streams).
- Metadata and documentation:
  - Need for detailed metadata describing data quality, limitations, and transformation steps (PU definitions, mass-balance assumptions, nutrient content basis).
  - Documentation of the rationale behind household waste estimates and the transfer of data between streams (e.g., from residual waste to AD vs landfill).
- Data quality control and reproducibility:
  - Use of literature-based PU data introduces variability; establish versioning of PU parameters and measurement sources.
  - Reproducibility requires access to the Excel model and any scripts used to generate Sankey diagrams (SankeyMATIC usage demonstrated).
- Data sharing and interoperability:
  - Ensure alignment with standard waste and nutrient taxonomies (EWC codes, R&D codes) to facilitate cross-regional comparisons.
  - Consider publishing datasets and model configurations in a data portal with clear licensing and update cadence.
- Data governance actions and recommendations:
  - Maintain comprehensive data dictionaries for all inputs, transformations, and outputs.
  - Capture uncertainties and provide sensitivity analyses or ranges for key PU parameters.
  - Plan for regular updates as newer waste data become available (e.g., post-2019 baselines, newer wastewater data).

## Practical implications and usage
- For policy and planning: provides a quantitative basis to identify key nutrient sinks and sources, informing regional nutrient circularity opportunities and targeted interventions.
- For data management: demonstrates the need for robust, interoperable data flows and metadata to support ongoing nutrient flow mapping and governance across regions.
- For future work: expand data coverage to include run-offs, fertilizer inputs, and cross-regional nutrient movements; incorporate data ranges and probabilistic modelling to better capture uncertainty.

## Conclusions and future work
- The study demonstrates a systematic MFA-based approach to map regional nutrient flows within waste streams, supported by stakeholder input and multiple data sources.
- It highlights valuable insights into where nutrients concentrate and where intervention could improve resource efficiency and environmental outcomes.
- Limitations identified point to the need for broader data coverage, improved data precision, and inclusion of additional nutrient pathways in future work.