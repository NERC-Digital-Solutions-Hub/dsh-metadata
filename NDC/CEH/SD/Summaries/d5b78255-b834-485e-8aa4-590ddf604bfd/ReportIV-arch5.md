# SUMMARY

- The document reports on four years of the NERC Soil Biodiversity Thematic Programme at the Sourhope site, focusing on above-ground productivity, plant community composition, and diversity under five main treatments across a replicated block design.
- It links above- and below-ground processes by documenting botanical responses to mowing, fertilisation, lime, and insecticide (Dursban) applications, with attention to functional plant groups (CSR framework) and bryophyte dynamics.
- Data collection has been extensive and multi-faceted, intended to support cross-project synthesis on soil biodiversity, vegetation structure, and ecosystem processes.

## Data assets and variables

- Above-ground indicators:
  - Biomass production per plot, measured repeatedly across five cuts each summer (1999–2002), with full biomass per plot and per year.
  - Normalised biomass relative to Control 1 to compare treatment effects over time.
  - Species composition and relative abundance (point analyses, hits per species).
  - Shannon diversity indices calculated from point analyses (1998 baseline and 2000–2002 surveys).
  - Functional grouping of plants (stress tolerant S, competitive-stress C-S-R, ruderal SR/CSR) and their changes over time.
- Bryophytes and non-vascular components:
  - Bryophyte abundance and species identification enhanced in 2002; overall bryophyte hits tracked across treatments.
- Soil data:
  - Soil pH measured at 5 cm depth (baseline 1998; repeated in 2002).
  - Soil moisture content measured at corners of point-analysis cells (theta probe; 2002).
- Weather data:
  - On-site Automatic Weather Station data (rainfall, radiation, air/soil temperatures) starting from 1999, with detailed measures for 1999–2002.
- Site- and plot-level treatment metadata:
  - Plot layout, block structure (5 replicate blocks), randomised treatments within blocks, sub-plots, and mowing/treatment schedules.
- Appendices and datasets:
  - Appendix 1–8 include site maps, treatment summaries, species lists (vascular and bryophyte), biomass data, PCA results, and species-hit rankings.
  - Appendix 5 provides weather data; Appendix 6–8 provide biomass, rank, and diversity data.

## Data collection methods and schedule

- Experimental design:
  - Rigg Foot site with 5 replicate blocks; each block has 6 main plots subdivided into 10 sub-plots; treatments allocated at random.
- Treatments:
  - Control 1 (no treatment), Control 2 (no treatment), Nitrogen, Lime, Nitrogen & Lime, Insecticide (Dursban 4 OPA).
- Management and treatments:
  - Monthly mowing May–September to ~6 cm; insecticide applied after mowing; nitrogen and/or lime applied in spring as per schedule.
- Data collection procedures:
  - Above-ground biomass: random 0.5 m^2 cell within sub-plots S, T, U, V; clipping dried at 80°C and weighed (1999–2002).
  - Baseline vegetation: 0.5 m^2 25-point quadrat survey in 1998.
  - Point analysis: annual surveys in July/August using a 0.5 m^2 cell with a 100-hole grid; large pin dropped to record the first species touched by the pin (2000–2002; bryophyte-focused enhancement in 2002).
  - Soil: pH measured in center of plots (2002), soil moisture measured in 2002.
  - Weather: continuous weather data from on-site station (1999–2002).
- Data management and activity:
  - Phase I projects largely completed by 2002; Phase II projects conducted with fieldwork visits (including labelled 13CO2 pulses and trace gas measurements) using CEH mobile labs.

## Data quality, processing, and analysis

- Data processing:
  - Biomass data analyzed with log transformation; ANOVA (split-plot Genstat) to test effects of Treatment, Year, and their interaction.
  - Normalisation of treatment biomass against Control 1 to compare year-to-year changes.
  - PCA performed on point-analysis data to identify groupings by treatment and to explore species associations.
- Key findings related to data interpretation:
  - Biomass productivity remains highest in plots receiving both nitrogen and lime, with long-term increases vs. starting values; however, 2002 showed a general fall in biomass across many treatments, with stronger declines observed in certain blocks.
  - Positive association between soil pH (especially with lime) and biomass in many plots; nitrogen effects are more variable depending on moisture and pH.
  - Functional-group shifts: stress-tolerant (S) species increase in unfertilised plots; C-S-R species expand in plots with nitrogen and lime; SR-C-S-R groups decline with lime and/or insecticide.
  - Representation of bryophytes increased across the site, particularly in unimproved plots; moss dominance rose as vascular plant dominance declined in some treatments.
  - Insecticide treatment shows complexity; while not conclusively linked to higher diversity, may enable certain palatable species to persist under relatively infertile conditions.
  - Trampling (notably in C2 plots) likely reduced productivity during intense sampling activities.
- Data limitations:
  - 2002 weather-station malfunction caused missing data periods; some dates were supplemented with data from a nearby Konza station.
  - Some blocks exhibited spatial (slope) effects on productivity, complicating between-treatment comparisons.
  - Control 2 plots were not surveyed in 2000–2001, creating gaps in cross-year comparisons for biomass and point analyses.

## Data governance, accessibility, and stewardship implications

- Data governance context:
  - Data generated across multiple projects (Phase I and Phase II) with centralized coordination at the Sourhope site; consistent labeling of plots, treatments, and years is essential for cross-project synthesis.
  - Documentation is extensive, including site maps, treatment summaries, species lists, and method details (Appendices 1–8), enabling reproducibility and secondary analyses.
- Metadata and provenance considerations:
  - Detailed metadata needed for each dataset: plotID, block, year, treatment, sub-plot, sampling method (biomass vs. point analysis), measurement units (e.g., g m^-2 for biomass; pH units; % hits for species), and data transformation steps (e.g., ln biomass).
  - Taxonomic updates (e.g., improved bryophyte identification in 2002) require versioning and explicit taxon authority lists to maintain comparability across years.
- Data sharing and access:
  - Data are documented and organized for sharing with Soil Biodiversity Programme researchers (and via the Soil Biodiversity website); ensure ongoing maintenance of central data repositories and documentation for long-term discoverability.
- Governance challenges and mitigation:
  - Coordinating data across many projects and years necessitates data quality checks, standardized ontologies, and robust data dictionaries.
  - Address data gaps due to weather issues and field restrictions (e.g., foot-and-mouth restrictions in 2001) with clear notes in the metadata and, where possible, documented data imputation or substitution protocols.

## Practical implications and recommendations for data stewards

- Ensure a centralized, versioned data repository with:
  - Plot-level metadata (plot, block, year, treatment, mowing date, sampling method).
  - Species-level data with identifiers for vascular plants and bryophytes; include taxonomic authorities and any reclassifications over time.
  - Biomass data per plot per year, including normalization references (Control 1) and transformation steps.
  - Environmental variables (soil pH, soil moisture, weather data) with timestamps and measurement depths.
- Maintain data quality controls:
  - Implement validation rules for units, ranges, and consistent labeling.
  - Track data provenance and transformation steps (e.g., ln transformation for biomass).
  - Document exceptions (e.g., missing data due to weather station malfunction) and data substitutions (e.g., Konza data) with justification.
- Preserve and communicate context:
  - Provide detailed methodological metadata for all surveys (baseline 1998, point analyses 2000–2002, biomass sampling protocols).
  - Include appendices or data dictionaries that map species names to standard references and note any identification enhancements (e.g., bryophyte species-level identification in 2002).
- Plan for long-term accessibility:
  - Ensure the Soil Biodiversity website and any data portal continue to host datasets and provide user-friendly search and download capabilities.
  - Record data lineage to enable future researchers to trace back results to raw measurements and processing steps.
- Align with governance objectives:
  - Facilitate cross-project data integration by harmonising variable definitions and ensuring consistent treatment labeling.
  - Prepare dashboards or reports that translate complex ecological trends (e.g., CSR functional shifts, bryophyte expansion, productivity trends) into actionable insights for data users and funders.

- Key takeaways for data stewardship relevance:
  - The Sourhope dataset offers a rich, longitudinal view of plant productivity, diversity, and functional composition under controlled management regimes, underscoring the importance of well-documented, accessible metadata and transparent data processing to enable cross-project synthesis and future reuse.