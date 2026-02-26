# Supporting Information

- The document provides supporting data and methods for the NERC Soil Biodiversity Programme project focused on earthworm diversity and soil biogeochemical interactions at Sourhope/Sweethope, Scotland.
- Key aim: examine interactions between earthworms, soil microbial processes, organic matter transformations, and soil structure; evaluate effects of targeted earthworm inoculations and lime treatment.

## Study site and context

- Location: Sourhope Experimental Site, upland grassland in southern Scotland; nearby Sweethope mesocosm enclosure (~100 m from main plots).
- Soil: Brown Forest Soils (Sourhope series) on glacial till, with varied properties across the site; base-poor, damp mineral soils.
- Historical context: NERC Soil Biodiversity Programme (1999–2008 era) studied soil biota diversity and functional roles.

## Experimental design and treatments

- Sweethope mesocosm setup mirrored the main plots: 5 rows with control and limed treatments, randomized within rows.
- Soil handling: 100 soil boxes (approx. 8 t) removed from Sourhope controls/limed plots in Nov 1999, rebured 100 m away at Sweethope; half the boxes hand-sorted to remove earthworms.
- Earthworm inoculation: three functional groups plus all groups, plus a no-inoculation control.
  - Inoculated species (available locally): Lumbricus rubellus (epigeic), Allolobophora chlorotica (endogeic), Lumbricus terrestris (anecic).
  - Inoculation per box: 20 L. rubellus, 15 A. chlorotica, 4 L. terrestris; applied April 2000.
  - Treatments: No inoculation; one epigeic; one endogeic; one anecic; all three groups (ABC).
- Lime treatment: applied to main Sourhope plots and mirrored in Sweethope boxes.
- Box design: dimensions ~ Depth 24.5 cm, Width 33 cm, Length 43 cm, Volume 0.035 m3; fine mesh lids and base mesh to prevent escapes; drainage holes evenly distributed.

## Data collected

- Earthworm census (end of Sweethope experiment, Oct 2001): abundance and biomass of earthworms, by species, per m2.
- Botanical composition (end of Sweethope mesocosm, Oct 16–17, 2001): plant species presence and Braun-Blanquet cover scores (0–6) per treatment plot.
- Sampling method: hand-sorting earthworms, ethanol fixation (40%), identification to species (Sims & Gerard, 1985); biomass and abundance calculated per m2.
- Sampling oversight: blocks, main plots, sub-plots recorded; replication achieved via five blocks.

## Datasets and data structure

- Dataset 1009: Sweethope Endpoint Botanical Composition Data (2129_BOTANICAL_COMPOSITION.csv)
  - Key fields: SAMPLE_ID; SAMPLING_DATE; BLOCK; MAIN_PLOT; SUB_PLOT; CELL_X; CELL_Y; TREATMENT (C=Control, L=Limed); SPECIES; BOTANICAL_COMPOSITION (Braun-Blanquet scale 0–6; 0 = not present).
  - Purpose: botanical composition by treatment and plot cell at endpoint.
- Dataset 1010: Sweethope Endpoint Earthworm Survey Data (P2129_EARTHWORM_SURVEY.csv)
  - Key fields: SAMPLE_ID; SAMPLING_DATE; BLOCK; MAIN_PLOT; SUB_PLOT; CELL_X; CELL_Y; TREATMENT (C/L); SPECIES; ABUNDANCE (total per m2); BIOMASS (per m2).
  - Purpose: final census of earthworm populations by species and community metrics.
- Data structure notes: both datasets are comma-separated with standardized identifiers for samples, plots, and cells to enable cross-linking by treatment and location.

## Methods and processing

- Earthworm detection: hand-sorting as preferred method over chemical extraction due to multi-user plot constraints; samples stored cold and processed for identification.
- Species identification: via Sims & Gerard (1985) key after preservation in ethanol.
- Biomass calculation: earthworms weighed after gut clearance (24 hours on damp tissue, blotted dry); results expressed per m2.
- Botanical data: presence assessed with Braun-Blanquet scale on end-point sampling.

## Quality control and limitations

- Quality assurance steps included numeric range checks, format conformity, and logical integrity checks.
- Caution on data use: data are subject to QA but with no guarantee of accuracy or fitness for a given use; no liability accepted by NERC for data use outcomes.

## References and further reading

- Bishop et al. (2008). Liming upland grassland: effects on earthworm communities and carbon in casts. European Journal of Soil Science.
- Scott et al. (2003). SOURHOPE FIELD DATA HANDBOOK 2003. Supporting Information.
- Sims & Gerard (1985). Earthworms: keys and notes for identification.
- Spring (2003). The effects of earthworms on soil structure in upland grassland. PhD thesis, University of Stirling.
- Usher et al. (2006). Understanding biodiversity in soil: UK Soil Biodiversity Programme. Applied Soil Ecology.