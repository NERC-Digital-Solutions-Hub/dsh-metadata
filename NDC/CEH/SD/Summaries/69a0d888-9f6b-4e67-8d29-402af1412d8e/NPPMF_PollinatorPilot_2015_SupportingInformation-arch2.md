# NPPMF_PollinatorPilot_2015

## Overview
- A pollinator monitoring pilot conducted in 2015 across 14 UK sites with four sampling rounds (April–August 2015).
- Half the sites were agricultural habitats; half semi-natural habitats.
- Goals included comparing sampling methods, evaluating recorder capabilities, gathering participant feedback, and generating detailed implementation cost information.

## Aims and Approach for Analysts
- Standardise data to monitor environmental health and policy performance over time.
- Verify, clean, and transform data from established sources; produce outputs suitable for reports, maps, and charts.
- Ensure datasets are stored and accessible through appropriate portals.
- Explore opportunities to enhance dataset value by combining with other environmental data and increasing data access.

## Recorder Types and Roles
- Researcher: paid staff with training in pollinator sampling/ID; species-level data for bees and hoverflies.
- Consultant: taxonomic experts (England/Wales); species-level data for bees and hoverflies; includes some expert amateur contributors.
- Volunteer: citizen scientists; data from 12 of 14 sites; broad-group classifications (not species-level); observed alongside researchers.
- Data resolution differences:
  - Researchers/Consultants: species-level for key groups (bumblebees, honeybees, solitary bees, hoverflies).
  - Volunteers: broad taxonomic groups only.

## Sampling Methods and Protocols
- Methods trialed in combinations (pan trapping, fixed transects, timed focal flower observations, standardized free searches, floral transects/quadrat surveys).
- Pan trapping: 5 stations per site; researchers only (volunteers could assist under researcher guidance).
- Fixed transects pollinator surveys: 5 transects of 200 m per site; all recorder types could conduct.
- Timed focal flower observations (FFOs): two 10-minute observations per site; conducted by all recorder types.
- Standardised free searches in good habitats: two fixed areas per site; allowed for researchers, consultants, and volunteers (with different involvement levels).
- Floral resources: transect-based floral surveys and floral quadrats to estimate floral abundance.
- Data collection context: transects walked with consistent routes; floral surveys conducted after insect surveys; conditions recorded to support analysis.

## Site and Protocol Design
- Each site defined as a 1 km2 Ordnance Survey grid square (standardised area for sampling and comparability with other schemes).
- Within each grid square:
  - Five pan trap stations placed along an approximately diagonal line through the center.
  - Five 200 m transects (three straight and two following linear features where feasible).
- Floral resource surveys conducted per transect after insect surveys.
- One-day protocols (~8 hours) per recorder type to standardise implementation across sites.
- Locations were adjustable for safety or habitat changes but otherwise kept consistent across rounds.

## Data Files and What They Contain
- NPPMF_PollinatorPilot_2015_SiteVisitConditions.csv
  - Per site visit: date, recorder, environmental conditions, temperature, wind, cloud, habitat, notes.
  - Columns include Site, Site Type, Round, Protocol Type, Recorder, Date Collected, Temp, Wind, Cloud, Sun, Habitat Codes, Notes.
  - Quality Control: No specific QC applied.
- NPPMF_PollinatorPilot_2015_FreeSearchConditions.csv
  - Environmental conditions for consultant-led standardized free searches.
  - Columns include Site, Round, Area Code, Recorder, Time, Temp, Cloud, Wind, Area Size, Time Allocation, Habitat Codes, Expertise levels, Notes.
  - Quality Control: No specific QC applied.
- NPPMF_PollinatorPilot_2015_FFOBConditions.csv
  - Timed focal floral observations: timings, environmental conditions, and floral resource details.
  - Columns include Site, Round, Protocol Type, Recorder, Quadrat No, Date, Start/End Time, Temp, Cloud, Wind, Focal Flower and counts, other flowers and counts, Flower Density Score.
  - Quality Control: No specific QC applied.
- NPPMF_PollinatorPilot_2015_AllInsects.csv
  - All insects recorded across four sampling methods; method, site, round, recorder, taxonomic group, genus, species, full name, date identified, and count.
  - Columns include Site, Round, Protocol Type, Recorder, Method, Section No, Free Search Number, FFOB Quadrat, Group, Genus, Species, Full Name, Date ID, Number.
  - Quality Control: No specific QC applied.
- NPPMF_PollinatorPilot_2015_FloralTransets.csv (FloralTransects)
  - Floral abundance estimates along transects; plant species and abundance units.
  - Columns include Site, Round, Protocol Type, Recorder, Plant Species, Unit (e.g., Head, Spike, Umbel), Abundance Score, Median Abundance.
  - Quality Control: No specific QC applied.
- NPPMF_PollinatorPilot_2015_FloralQuadrats.csv
  - Flower abundance data from 1 m2 quadrats around transects/pan traps.
  - Columns include Site, Round, Recorder, Quadrat, Plant Species, Unit.
  - Quality Control: No specific QC applied.
- Question-Response Dataset (Likert-style survey)
  - Recoder feedback on protocols via agreement scales and open comments.
  - Columns include Recorder, Protocol Type, Method, Question, Strongly Agree, Agree, Neither, Disagree, Strongly Disagree, Comments.
  - Quality Control: No specific QC applied.

## Quality and Limitations
- Across datasets: no formal quality control applied within the data documents.
- Weather and operational extensions occurred due to poor weather, affecting round timing and sampling completion.
- Variation in data resolution between recorder types (species-level vs broad-group classifications) to be considered in analyses.

## Relevance for Environmental Monitoring Analysts
- Provides a structured, area-standardised framework (1 km2 grid cells) enabling temporal and spatial comparisons.
- Enables method-comparison analyses across recorder types and protocols, informing standardised monitoring approaches.
- Produces multi-layered datasets (insects, floral resources, site conditions) suitable for integrated environmental health assessments and policy performance tracking.
- Highlights data integration opportunities and potential demand for data accessibility, given the emphasis on making underlying data accessible to others.

## Practical Considerations for Analysis
- Align datasets by site, round, protocol type, and recorder to enable cross-method comparisons.
- Account for differences in taxonomic resolution across recorder types when aggregating data (species-level vs broad-group).
- Use site-visit conditions to adjust for environmental covariates (temperature, wind, cloud, habitat type) in modeling pollinator activity.
- Consider the absence of explicit QC in planning any data cleaning or validation steps before downstream analyses.
- Leverage the standardized 1 km2 grid and repeated rounds to assess temporal trends and habitat-specific patterns in pollinator communities and floral resources.