# JAE_Keogan_Europeanshag_phenologymismatch

## Overview
- A set of data files describing European shag phenology and diet to investigate phenology mismatch with prey availability (sandeels) and reproductive success.
- Contains three datasets: shag dataset (phenology and outcomes), diet dataset (sample collection and prey composition), and a bivariate dataset (combined phenology and reproductive metrics by species).
- Data are structured to support analysis of annual patterns, year-centred trends, and cross-variable relationships (e.g., lay date, SST, fledging success, prey proportion).

## Data Assets at a Glance
- JAE_Keogan_Europeanshag_phenologymismatch_shagdataset
  - Variables include: year, lay date (laydate), first-clutch fledging (chicks.fledged.first), first-clutch failed eggs (failedeggsfirst), mean lay date (Mean.Lay), lay date relative to annual mean (relative.lay), past/present SST for February/March (SST.past, SST.present), breeding population size (pop.size), year-centred variable (yearcentre), total fledging and total failed eggs across all clutches (chicks.fledged.all, failedeggsall).
- JAE_Keogan_Europeanshag_phenologymismatch_dietdataset
  - Variables include: Year, Date (sample collection day), Age ( chick or adult ), SST, yearcentre, meandate, datediff, SE1:SE0_proportion (proportion of 1+ sandeels), logitSE1:SE0 (logit-transformed proportion).
- JAE_Keogan_Europeanshag_phenologymismatch_bivariatedataset
  - Variables include: Year, Species (shag or sandeel), chicks.fledged, failedeggs, sandeelproportion, dayofyear (laying for shags or sample collection for sandeels), Mean.Lay, Relative (centred day-of-year around average lay date).

## Core Variables and What They Measure
- Phenology and reproduction
  - laydate, Mean.Lay, relative.lay: timing of egg laying within and across years.
  - chicks.fledged.first/all, failedeggsfirst/all: reproductive outcomes by clutch and overall.
- Climate context
  - SST.past, SST.present: February/March sea surface temperatures for current and previous year.
- Population context
  - pop.size: breeding pair population size.
- Data centering and alignment
  - yearcentre: year centred around study average to enable year-to-year comparisons.
- Diet and prey dynamics
  - SE1:SE0_proportion, logitSE1:SE0: proportions of 1+ sandeels relative to total prey, with logit transformation for analysis.
- Data collection and alignment
  - Date, meandate, datediff: timing of sample collection and its relation to annual timing.
- Integrated indicators (bivariate)
  - chicks.fledged, failedeggs: combined reproductive outcomes alongside prey metrics (sandeelproportion) and timing (dayofyear, Mean.Lay, Relative).

## Data Quality, Standards, and Governance
- Metadata and discoverability evident via explicit variable definitions and centering around annual norms.
- Clear notes on units and measurement contexts (e.g., day of year, SST timing, age categories).
- Potential gaps in standardization across datasets (e.g., naming conventions and units harmonization) that could affect cross-dataset analyses.
- Access considerations not specified but implied by presence of nested datasets and potential data-sharing needs.

## Access, Collaboration, and Data Stewardship
- Data appear organized for collaboration across researchers studying phenology mismatch, with explicit fields to enable cross-dataset linkage (e.g., yearcentre, relative lay date).
- To maximize reuse, consistent metadata, documentation, and versioning are important; consider establishing data standards and a data dictionary across all three datasets.
- Potential for cross-partner collaboration to expand beyond shag/diet to broader predator-prey or phenology studies.

## How This Informs Data Strategy for Data Leaders
- System-level view: Integrates phenology, reproduction, prey availability, and climate context to assess mismatch dynamics.
- User-centred data products: Variables like relative lay date and year-centred measures support stakeholder visibility into timing mismatches and trends.
- Data discovery and provisioning: Highlights need for clear metadata, data provenance, and discoverability to support analysts and policy colleagues.
- Data quality and governance: Emphasizes standardized measures, consistent units, and clear documentation to enable reliable cross-year comparisons.
- Collaboration and community: Opportunities to harmonize datasets and share best practices with a broader data community focused on ecological phenology.

## Challenges and Gaps (Relevance to Data Leaders)
- Ensuring data standards across datasets (naming, units, centering methods) for seamless integration.
- Variability in data granularity and potential inconsistencies in timing references (lay date vs. sample date).
- Access barriers and data protection considerations that may hinder sharing and reuse.
- Verification of data content and format across datasets, especially where multiple clutches or complex prey metrics are involved.
- Need for stronger coordination and communities of practice to avoid duplicated effort and improve interoperability.

## Opportunities and Next Steps
- Develop and publish a unified data dictionary and standard metadata schema for all three datasets.
- Harmonize variable naming, units, and centering methods to enable straightforward cross-dataset analyses.
- Create data products that align with user needs (e.g., dashboards of phenology mismatch metrics, trend analyses by year/region).
- Establish data-access protocols and governance to balance openness with privacy/protection requirements.
- Promote cross-institution collaboration to expand the dataset scope (e.g., additional species, regions, or prey types) and strengthen communities of practice.