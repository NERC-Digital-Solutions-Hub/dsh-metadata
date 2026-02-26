# Susceptibility of Scots pine ( Pinus sylvestris ) to Dothistroma septosporum following natural inoculation at Torrs Warren, Galloway 2013-2015

## Overview
- Longitudinal common garden trial of Scots pine trees transplanted from CEH Edinburgh (April 2013) to Torrs Warren, Galloway.
- Aims to study susceptibility to Dothistroma septosporum (DNB) across multiple populations and families, with six randomized blocks.
- Data cover infection dynamics, growth, and needle-level pathology from 2013 to 2015, plus metadata for provenance, site, and management.

## Dataset contents
- Height data: pre-translocation height (recorded annually from 2009) and post-translocation height measurements (end of growing seasons 2014, 2015).
- DNB infection assessments: estimated percentage of current-year needles infected (measured semi-annually from Sept 2013 onward; values in 5% increments).
- Additional phenotypes: branching architecture (Mar 2015), chlorophyll fluorescence (July 2014), and defoliation of previous-year needles (Oct 2014).
- Needle-level detailed measurements: two assessment periods with raw needle data (Sept 2013 and Oct 2014) including lesion metrics and, in Oct 2014, visible fruiting bodies.
- Per-tree mean and raw data: aggregated records for each tree across assessments, plus mean values from detailed needle assessments.

## Data files
- Detailed_assessment_Sep_2013.csv
  - Needle-level subset data for infected trees (up to 11 needles per tree).
  - Variables include: block, position, needle number; LNL (length of needles with lesions), LPN (lesions per needle), LL (lesion length).
  - Date of collection: 17/09/2013.
- Detailed_assessment_Oct_2014.csv
  - Needle-level data from infected trees (up to 5 needles per tree).
  - Variables include: total needle count, needle-specific counts, FBV (visible fruiting bodies), LL, LNL, LPN.
  - Date of collection: 07/10/2014.
- Mean_phenotype_per_tree.csv
  - Per-tree raw data and mean values for infection assessments, height, chlorophyll fluorescence, branching, and defoliation.
  - Contains provenance and site metadata: Population, Pop, Fam, Block, Position, orig no, lat/long, altitude (ALT).
  - Management and treatment: fungicide_2015 (Y/N/NA); date fields for height measurements (end2009 to end2015).
  - Infection measures across years: infection_SS_2013-14, infection_AW_2013-14, infection_Total_2013-14; infection_SS_2014-15, infection_Total_2014-15; infection_AW_2015-16 (values converted to LOG for analysis).
  - Defoliation, chlorophyll fluorescence (cf_jul2014), branching counts (branches_main, branches_main_inc_dead, branches_total), top_missing.
  - Dates for key measurements and notes on data structure (e.g., raw vs mean values).

## Data quality and provenance
- Infection assessments conducted by a single observer (Annika Perry) to ensure consistency.
- Cultures confirming Dothistroma septosporum presence were isolated from needles (Sept 2013).
- Data origin: trees from eight Scottish populations, four families per population (192 trees), grown from seed in 2007, transplanted in 2013 at age six.
- Site and trial design: Torrs Warren site adjacent to infected stands of Corsican and lodgepole pines; six randomized blocks; guard row around edge; annual weeding.
- Data quality notes: some trees died or were removed (2013–2015); a list of dead/missing trees is provided with positions and family identifiers.
- Missing data are denoted as NA in the dataset; a subset of trees experienced death or removal by certain assessments (dates provided).

## Site, trial design, and timing
- Location coordinates for corner trees are provided (GPS): 
  - 54.86421543, -4.88794564 (1/1-RM1845)
  - 54.86417167, -4.88799501 (3/4-CCC1807)
  - 54.86413689, -4.88789602 (6/32-GA1892)
  - 54.86417863, -4.88785151 (4/29-GT1860)
- Trial design: six randomised blocks; one individual per family per block (192 trees total).
- Assessments conducted every six months (autumn and spring) for infection; height measured annually; chlorophyll fluorescence measured in July 2013; defoliation recorded in Oct 2014.

## Origin and management of trees
- Eight populations: Ballochbuie, Blackwood of Rannoch, Beinn Eighe, Coille Coire Chuilc, Glen Affric, Glen Loy, Glen Tanar, Rothiemurcus.
- Four families per population; six individuals per family; germinated spring 2007; transplanted 2013.
- In 2015, three blocks (4, 5, 6) were sprayed with copper-based fungicide as part of the PROTREE project.

## Purpose and context
- Data used for PhD research (Annika Perry, chapter 4) and the PROTREE project (Tree Health and Plant Biosecurity Initiative), focusing on natural inoculation and susceptibility to Dothistroma septosporum.

## Related datasets and usage notes
- The same trees were previously measured in situ at CEH Edinburgh for chlorophyll fluorescence and needle morphology.
- The design was maintained across sites; researchers Matti Salmela and Kevin Donnelly also worked with these trees.
- Users should treat Mean_phenotype_per_tree.csv as the integrated per-tree record, with detailed needle data providing the raw measurements for infection and lesion metrics.

## Summary of applicability for data leadership
- Comprehensive, multi-level dataset linking provenance, site, management, and longitudinal phenotype.
- Rich metadata facilitates understanding of data lineage, quality controls, and updates.
- Examples of potential data systems challenges addressed: fragmented data sources (multi-file structure), variable data quality and metadata clarity, and coordination across datasets (population/family provenance, site data, and treatment events).
- Suitable for analyses of heritability, infection dynamics, and the impact of management practices within a defined network of partner datasets.