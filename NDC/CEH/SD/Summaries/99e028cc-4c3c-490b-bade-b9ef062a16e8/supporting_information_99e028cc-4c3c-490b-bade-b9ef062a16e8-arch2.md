# Susceptibility of Scots pine ( Pinus sylvestris ) to Dothistroma septosporum following natural inoculation at Torrs Warren, Galloway 2013-2015

## Overview
- A common garden trial of Scots pine trees transplanted from CEH Edinburgh (April 2013) to Torrs Warren, Galloway.
- Objective: assess susceptibility to Dothistroma septosporum infection and environmental interactions; data used in PhD research and the PROTREE project.

## Dataset contents
- Regular assessments (infection, height, branching, chlorophyll fluorescence, defoliation) from 2013–2015.
- Detailed needle-level measurements from two assessments: September 2013 and October 2014.
- Data files included:
  - Detailed_assessment_Sep_2013.csv
  - Detailed_assessment_Oct_2014.csv
  - Mean_phenotype_per_tree.csv
- Mean_phenotype_per_tree.csv includes raw data and mean values for measurements from the detailed needle assessments.

## Detailed assessment files (content and structure)
- Detailed_assessment_Sep_2013.csv
  - Variables include: Block, Position, Needle number, Length of needles with lesions (LNL), Number of lesions per needle (LPN), Lesion length (LL).
  - Up to 11 needles examined per infected tree.
  - Date data collected: 17/09/2013.
- Detailed_assessment_Oct_2014.csv
  - Variables include: Total needle count, Needle number, Visible fruiting bodies on lesions (FBV), Lesion length (LL), Length of needles with lesions (LNL), Lesions per needle (LPN).
  - Up to 5 needles examined per infected tree.
  - Date data collected: 07/10/2014.

## Mean phenotype per tree (Mean_phenotype_per_tree.csv)
- Per-tree measurements across assessments:
  - Population, Pop (abbreviation), Family, Block, Position, orig no.
  - Fungicide2015 (Y/N/NA) and other metadata (lat, long, altitude).
  - Height data from 2009–2015 (annual end-of-season measurements).
  - Branch counts (main, main including dead, total), top_missing.
  - Infection metrics: infection_S_S_2013-14, infection_AW_2013-14, infection_Total_2013-14, infection_S_S_2014-15, infection_AW_2015-16, infection_Total_2014-15, infection_S_S_2015-16.
  - Chlorophyll fluorescence (cf_jul2014: Fv/Fm), defoliation_oct2014.
  - Detailed needle metrics at various years (LL, LNL, LPN across 2013 and 2014).
  - Notes indicate transformations (e.g., LOG) were applied to infection metrics for analyses.

## Origin of the trees
- Eight Scottish populations represented (Ballochbuie, Blackwood of Rannoch, Beinn Eighe, Coille Coire Chuilc, Glen Affric, Glen Loy, Glen Tanar, Rothiemurcus) with four families per population (192 trees total).
- Trees grown from field-collected seed; germinated spring 2007; transplanted in 2013 at six years old.

## Site and trial design
- Location: Torrs Warren, near stands of Corsican and lodgepole pines infected with Dothistroma needle blight.
- Design: six randomized blocks; one tree per family per block.
- Planting: 6 L pots, stake-grounded at 0.5 m spacing; guard row around edge to minimize edge effects.
- Management: annual weeding of surrounding brambles/bracken.
- GPS coordinates provided for key corner trees with Block/Position/Family identifiers.

## Assessments and measurements
- Assessments every six months (autumn and spring) for infection; infection measured as the percentage of current-year needles that are green/healthy (in 5% increments; <1% indicates negligible infection).
- Height measured annually at end of growing season or start of next.
- Branching recorded once (March 2015) across 2013–2015 following translocation.
- Chlorophyll fluorescence measured in July 2013 (HandyPea fluorometer) to detect stress (Fv/Fm < 0.8 indicates stress).
- Defoliation recorded for previous-year needles in October 2014.

## Data quality and quality assurance
- Infection assessments performed by a single observer (Annika Perry) to ensure consistency.
- Dothistroma septosporum presence confirmed via culture from September 2013 needles.

## Data provenance and related work
- Data collected to support Annika Perry’s PhD and the PROTREE project (Tree Health and Plant Biosecurity Initiative).
- Related datasets include in situ chlorophyll fluorescence and needle morphology measurements at CEH Edinburgh, and copper fungicide treatment in July 2015 for subset blocks.

## Notes on data integrity
- Some trees died or were removed during 2013–2015; a list identifies missing data by tree, position, and date.
- Data include raw values and transformed measures; some values are NA due to death/missing data or later modifications.