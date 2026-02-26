# Campanula rotundifolia study: Cytotype determination and common garden

- Objective: Use standardized data collection and analysis to understand environmental health and variation in Campanula rotundifolia cytotypes across Britain and Ireland, and to compare clone performance in a common garden setting.
- Context for monitoring: Provides geo-referenced, quality-assured datasets on cytotype distribution and phenotypic responses to environment, enabling temporal and spatial scrutiny of plant genetic health and habitat suitability.

## Data collection and materials

- Timeframe and scope:
  - Over 1,700 samples (seeds, leaves, or stem cuttings) collected from geo-referenced locations, focusing on Britain and Ireland with broader context samples.
- Sampling approach:
  - Many samples volunteered and mailed; some from commercial seed lots or Botanic Gardens.
  - Efforts to sample more than one plant per locality when possible; minimum 5 m spacing to reduce clonal redundancy; intensified sampling in regions previously showing hexaploids (Wanlockhead, Teesdale, Cheddar).
- Sample handling and storage:
  - Leaves and cuttings kept cool for transport; seeds germinated; stem cuttings rooted in a cool glasshouse; leaf material stored at -20°C; seeds air-dried and stored at 4°C.
  - Excess material stored at CEH Edinburgh with sample codes for traceability.
- Location data:
  - Cytotype results linked to campanula_cytotype.csv with 0.01° resolution coordinates; anonymized site resolution preserved.

## Cytotype determination

- Reference and calibration:
  - Some individuals previously cytotyped by root tip cytology; flow cytometry used to calibrate and verify results; repeated analyses for conflicting cases.
- Methodology (flow cytometry):
  - Based on Doležel et al. 2007 protocol using Pisum sativum 'Ctirad' as internal standard and propidium iodide dye.
  - Sample prep: leaf tissue chopped with standard reference, nuclei extracted, stained, and measured with flow cytometers (FACSCalibur or Accuri C6).
  - Data handling: gating to isolate nuclei, calculation of DNA content as ratios to the internal standard, repeat analyses if coefficient of variation > 5%.
  - Sample condition checks: time-to-processing, desiccation, and color changes (desiccated or red/brown leaves) can affect results; such samples excluded from Cx analyses.
- Cytotype assignment:
  - Genome size (pg DNA) thresholds used to assign cytotypes:
    - Diploid: 2.27–2.71 pg
    - Tetraploid: 4.22–4.96 pg
    - Pentaploid: 5.33–5.65 pg
    - Hexaploid: 6.2–7.14 pg
  - Samples outside these ranges classified as aneuploids.
- Data outputs:
  - campanula_cytotype.csv contains country, location, sample code, and latitude/longitude.
  - Visual inspection of genome size distributions used to assign cytotypes, with confirmation against chromosome-counted references.

## Common garden study

- Experimental setup:
  - Clones produced from field-collected material (seed or cuttings) and planted October 2008 in a raised bed near CEH Edinburgh (55.86°N, 3.21°W, 190 m a.s.l.).
  - Five randomised blocks including clonal tetraploids, pentaploids, and hexaploids; distribution: 55 tetraploid, 1 pentaploid, 37 hexaploid clones.
  - Layout shown in Figure 1; blocks arranged to randomise clone identity within each block.
- Management:
  - Pollination not restricted; occasional weeding to reduce competition.
- Phenology and performance measurements:
  - Phenology: daily monitoring in 2009–2010; first flowering date (FFD) recorded when largest flowers were bee-accessible.
  - Growth and fecundity: August 2009 measurements of flowering stems, stem height, number of seedheads and open flowers; September 2009 harvests for biomass and stem counts.
- Data thematic scope:
  - Aimed to compare flowering dynamics and seed production across cytotypes under shared garden conditions.

## Description of data files

- Campanula_cytotype.csv
  - Columns: Country, Location, Sample code, Latitude, Longitude
- campanula_FFD.csv
  - Columns: Block number, Clone code, Date of first flowering 2009, Date converted to day-number 2009, 2009 plant condition comments, Date 2010 first flowering, 2010 day-number, 2010 plant condition comments
- Dest_harvest_Aug_2009_blocks_1_and_3.csv
  - Columns: Block number, Clone code, total flowering stems, height of stem 1, number of swollen seedheads on stem 1, number of other seedheads on stem 1, number of open flowers on stem 1, number of flower buds on stem 1, repeated for stem 2 and 3, plant condition comments
- Dest_harvest_Sept_2009_blocks_2_and_5.csv
  - Columns: Block number, Clone code, total stem dry weight (g), number of flowering stems
- Notes:
  - Dead or missing data marked with an asterisk; data arranged in columns; anonymized location details.

## Quality assurance and data handling

- Standardised protocols for flow cytometry and data analysis to ensure consistent cross-sample comparability.
- Validation through cross-check with chromosome counts and repeated analyses where necessary.
- Data storage and provenance:
  - Samples retained at CEH Edinburgh; datasets linked to clear sample codes for traceability.
  - Anonymity preserved by suppressing high-resolution location data where appropriate.

## Potential uses for environmental monitoring and policy

- Tracks spatial distribution of cytotypes and their phenotypic responses to environmental variation.
- Enables temporal monitoring of genetic diversity indicators across landscapes.
- Provides standardized data products (csv files) suitable for integration into environmental health dashboards, biodiversity indicators, and habitat management assessments.
- Supports reproducibility and re-use in future comparative studies of polyploidy and plant adaptation.

## References

- Doležel J, Greilhuber J, Suda J (2007). Estimation of nuclear DNA content in plants using flow cytometry. Nature Protocols 2(9): 2233-2244.
- McAllister HA (1972) The experimental taxonomy of Campanula rotundifolia L. Ph.D. thesis, University of Glasgow.
- Shepherd JR (2007) Polyploidy and the phylogeography of Campanula rotundifolia L. in the British Isles and Ireland. MSc thesis, University of Edinburgh.
- Stevens CJ, Wilson J, McAllister HA (2012) Biological Flora of the British Isles: Campanula rotundifolia. Journal of Ecology, 100(3), 821-839.

## Figure 1

- Layout of clonal plants in the common garden study, showing the 5 blocks and the individual clones randomly arranged within each block.