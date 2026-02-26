# Live-trapping surveys of small mammals on arable field margins on the Hillesden estate in Buckinghamshire (England) during 2005-2011

## Overview
- Long-term live-trapping study of small mammals on grassy field margins to evaluate responses to three management regimes as part of a wider agri-environment scheme experiment (Hill esden estate, Buckinghamshire, England).
- Timeframe: 2005–2011; data underpin analyses reported in Broughton et al. (2014).
- Location and design: 1000 ha farming estate with replicated blocks and three treatments (Cross Compliance, ELS, ELSX) to compare habitat management effects on mammal populations.
- Data lineage: Collected by field teams, with specimen marking (PIT tagging and fur clips) and measurement data; used to assess biodiversity outcomes at the farm scale.

## Study design and treatments
- Experimental layout: Randomised block experiment with five replicate blocks; each block includes CC, ELS, and ELSX treatments.
- Treatments:
  - Cross Compliance (CC): 1–2 m field margins from hedgerows; hedgerows cut annually after harvest.
  - Entry Level Scheme (ELS): 6-m-wide field margins; minor habitat enhancements; hedgerows cut biennially.
  - Entry Level Scheme Extra (ELSX): larger scale habitat improvements; 6-m margins with grasses and wildflowers; multiple patches of seed or wildflower management; hedgerows cut biennially.
- Habitat context: Margins and hedgerows provide resources; hedgerow presence and berry production assessed but not found to differ meaningfully across treatments for the purpose of this study.

## Survey methods and data collection
- Sampling periods: Autumn (Nov–Dec) 2005, 2006, 2008, 2010 and Spring (May) in the following seasons.
- Trapping setup: For each replicate, two 100-m trap lines (100 m apart within replicates); each line comprises 11 Longworth traps spaced 10 m apart (22 traps per replicate per season).
- Trapping procedure: Pre-baiting with wheat for four nights; traps baited with wheat, carrot, and blowfly pupae; monitored over three nights.
- Data collected per capture: Species identity, body mass (to 0.5 g), sex, breeding condition; individuals marked using PIT tags (autumn) or fur clips (spring); capture vs. recapture events recorded.
- Spatial data: Trapping coordinates and location identifiers; trap numbers and line details recorded.
- Data completeness: Preliminary results indicated low trap-limitation; captures broadly reflect mammal populations.
- Data structure: Rich metadata schema including Year, Season, Date, Trap_Check_Time, Farming_Regime, Habitat, Sampling_Block, Location, coordinates, Trap_Number, Capture_Type, Species (English and Scientific), Sex, Body_Condition, Weight_g, and Notes.

## Data structure and metadata
- Dataset size: 3172 trapping records, involving at least 1881 individual animals (captures and recaptures; some trap activations without captures).
- Key fields and descriptors:
  - Record: Unique capture record identifier.
  - Year, Season, Date: Temporal context of each event.
  - Trap_Check_Time: Morning vs. Afternoon checks.
  - Farming_Regime: CC or ELS/ELSX.
  - Habitat: Narrow margin (CC) or wider grassy margin (ELS/ELSX).
  - Sampling_Block: Replicate block number (1–5).
  - Location and coordinates: Field names and start coordinates of trap lines (x_coordinate, y_coordinate).
  - Trap_Number: Identifier for each trap within a line.
  - Fur_Clip_or_PIT, PIT_Tag_Code: Marking method and ID codes.
  - Capture_Type: New capture, recapture, or trap activation without capture.
  - Species_English/Species_Scientific: Taxonomic identifiers.
  - Sex, Body_Condition, Weight_g: Biological metadata.
  - Notes: Additional relevant information.
- Data quality: Records were checked and cleaned; errors removed; missing values encoded as No_data.

## Quality control and data curation
- Data cleaning: Systematic review to remove errors; standardization of fields and coding.
- Missing data: Explicitly labeled as No_data; users should account for these in analyses.
- Documentation: Metadata and field descriptions aligned to enable reproducibility and reuse.

## Appendix: Corvid interference with Longworth traps
- Issue: Carrion Crows (and possibly Magpies) disrupted longworth traps, undermining monitoring efforts.
- Observations: Interference escalated from 2008 onward; disturbances occurred across transects within 2.5 km, often during daylight; traps were sometimes displaced or dismantled.
- Investigation: Follow-up observations (including a notable event on 18 May 2011) linked disturbances to corvid activity rather than predators like foxes or badgers.
- Mitigation attempts: Pinning, partially burying traps, or covering with litter had limited success.
- Implication for data: Corvid interference introduced potential biases in capture data and required careful interpretation of population trends; highlights why documenting interference events is crucial for data governance and subsequent analyses.

## Data use, availability, and governance
- Primary analyses: Findings linked to agri-environment scheme effectiveness in a farm-scale context (Broughton et al., 2014).
- Documentation: Dataset includes comprehensive metadata, clear field definitions, and quality-control notes to facilitate reuse by researchers and data stewards.
- Reuse considerations: Users should consider potential trap interference, sampling effort across treatments, and missing data when performing analyses or integrating with other datasets.
- References: Key methodological and contextual sources are cited, including monitoring guides and related analyses of Hillesden and broader avian/mammal trapping literature.

## Key takeaways for data stewardship
- Maintain rigorous metadata and data dictionaries to accompany complex, multi-treatment field experiments.
- Capture and document all quality-control steps, data-cleaning decisions, and any data limitations (e.g., trap interference).
- Ensure data are discoverable via publication links and that datasets are clearly connected to study design (block design, treatment regimes) and protocols.
- Preserve appendices and supplementary observations (e.g., trap interference) as they critically affect data interpretation and reproducibility.