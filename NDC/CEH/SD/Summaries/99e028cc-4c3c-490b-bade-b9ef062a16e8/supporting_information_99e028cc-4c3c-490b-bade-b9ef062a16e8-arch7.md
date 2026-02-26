# This dataset is for a common garden trial of Scots pine trees which were transplanted from the cottage garden in CEH Edinburgh in April 2013 to Torrs Warren forest in Galloway.

## Overview
- A common garden trial of Scots pine (Pinus sylvestris) to study susceptibility to Dothistroma septosporum following natural inoculation.
- Trees originated from eight Scottish populations ( Ballochbuie, Blackwood of Rannoch, Beinn Eighe, Coille Coire Chuilc, Glen Affric, Glen Loy, Glen Tanar, Rothiemurcus) with four families per population (192 trees total).
- Transplanted in 2013 to Torrs Warren, Galloway; six randomised blocks; measurements collected over 2013–2015.
- Data captures infection progression, growth and health traits, including needle-level pathology and canopy metrics.

## Dataset contents
- Detailed_assessment_Sep_2013.csv
  - Needle-level infection data (Dothistroma needle blight), lesion metrics, and related measurements for up to 11 needles per tree collected on 17/09/2013.
  - Variables include block, position within block, needle number, lesion length (LNL), number of lesions per needle (LPN), and lesion length on needles with lesions (LL).
- Detailed_assessment_Oct_2014.csv
  - Needle-level data from a second assessment (07/10/2014) including total needle count per tree, lesions, lesion length (LL), length of needles with lesions (LNL), number of lesions per needle (LPN), and presence of visible fruiting bodies on lesions (FBV).
- Mean_phenotype_per_tree.csv
  - Per-tree data across assessments: infection estimates (spring/summer, autumn/winter, and total), height measurements (end of each year 2010–2015), chlorophyll fluorescence (Fv/Fm), branching counts, and defoliation estimates.
  - Summary statistics: mean values for detailed-needle measurements (from the Sep 2013 and Oct 2014 assessments) and metadata on tree origin, block/position, and site measurements.
  - Metadata fields include Population, Pop (abbreviation), Fam, Block, Position, orig no, fungicide treatment in 2015, latitude, longitude, altitude, and annual height records.
- Supporting documentation
  - PhD-related and PROTREE project context for the susceptibility study, with notes on data provenance and usage.

## Measurements and timeframe
- Infection assessments (DNB): six-monthly autumn and spring visits (approx. 2013–2015); expressed as percentage of current-year needles that are green and healthy (severity).
- Height: annual measurements at end of growing season or start of next season (autumn or early spring) from 2010–2015 for selected trees.
- Other traits: branching (captured March 2015), chlorophyll fluorescence (July 2014) to assess plant stress (Fv/Fm threshold ~0.8).
- Needle-level measurements: detailed lesion metrics and, in 2014, fruiting bodies on lesions (FBV) and other needle features.

## Site, origin, and trial design
- Site: Torrs Warren, Galloway, near Corsican and lodgepole pine stands with existing pine blight; trial placed in pots (6 L) at 0.5 m spacing with a guard row of Scots pines around the edge; annual weeding of brambles/bracken.
- Transplant details: six-year-old trees transplanted in 2013 from CEH Edinburgh; pots and staking used; GPS coordinates provided for corner trees:
  - 54.86421543, -4.88794564 (1/1-RM1845)
  - 54.86417167, -4.88799501 (3/4-CCC1807)
  - 54.86413689, -4.88789602 (6/32-GA1892)
  - 54.86417863, -4.88785151 (4/29-GT1860)
- Trial design: six randomised blocks; one tree per family per block (192 trees total).
- Data collection cadence: infection and health assessments every six months; height annually; one-time branching assessment; chlorophyll fluorescence in 2013; defoliation assessment in 2014.

## Data quality and validation
- Infection assessments conducted by a single person (Annika Perry) for consistency.
- Cultures of Dothistroma septosporum isolated from needles in Sep 2013 to confirm presence of the pathogen.
- Some trees died or were removed (dead/missing) during 2013–2015; the log lists affected trees with status and dates, resulting in NA data for some periods.

## Data provenance and context
- Purpose: used for Annika Perry’s PhD research (chapter 4) funded by NERC and Forest Research; part of the PROTREE project (Tree Health and Plant Biosecurity Initiative).
- Earlier and related datasets exist for the same trees, including in-situ chlorophyll fluorescence and needle morphology measurements; copper fungicide treatment occurred in July 2015 for blocks 4–6 as part of PROTREE endophyte studies.
- Data integrated across multiple files to provide both raw (needle-level) and derived (per-tree) phenotypes, enabling GIS-style spatial analysis of infection and growth across the trial layout.

## How GIS specialists can use this dataset
- Spatial mapping: leverage Block and Position within block identifiers to map phenotypes (infection severity, height, branching) across the six-block trial grid.
- Spatial features: use GPS coordinates for corner trees and block layout to infer trial geometry and perform spatial interpolation of health metrics.
- Temporal analysis: combine six-monthly infection data with annual height records to study spatial-temporal disease dynamics and growth responses.
- Data integration: link per-tree phenotypes with population/origination metadata (Population, Fam, orig no) for population-level spatial analyses and visualization of genetic diversity effects on disease susceptibility.
- Quality assessment: account for dead/missing trees and NA periods when creating GIS layers or conducting longitudinal spatial analyses.