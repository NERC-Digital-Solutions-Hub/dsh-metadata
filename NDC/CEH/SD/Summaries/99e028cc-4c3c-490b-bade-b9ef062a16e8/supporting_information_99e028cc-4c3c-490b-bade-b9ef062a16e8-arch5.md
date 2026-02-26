# Susceptibility of Scots pine ( Pinus sylvestris ) to Dothistroma septosporum following natural inoculation at Torrs Warren, Galloway 2013-2015

## Overview
- A common garden trial of Scots pine trees transplanted from CEH Edinburgh (April 2013) to Torrs Warren, Galloway.
- 192 trees representing eight Scottish populations (Ballochbuie, Blackwood of Rannoch, Beinn Eighe, Coille Coire Chuilc, Glen Affric, Glen Loy, Glen Tanar, Rothiemurcus) with four families per population, six-year-old at transplantation.
- Objectives include monitoring susceptibility to Dothistroma needle blight (DNB) and related tree phenotypes over time.
- Data collected to support PhD research and PROTREE project activities; some blocks were fungicide-sprayed in 2015 as part of related studies.

## Dataset contents and structure
- Detailed_assessment_Sep_2013.csv
  - Per-needle infection assessments (DNB), conducted 17/09/2013.
  - Measurements include: length of lesions (LNL), number of lesions per needle (LPN), lesion length (LL) for needles with lesions; up to 11 needles examined per infected tree.
- Detailed_assessment_Oct_2014.csv
  - Per-needle assessments conducted 07/10/2014.
  - Measurements include: total needles examined, lesion metrics (LL, LNL, LPN), and visible fruiting bodies on lesions (FBV), for up to 5 needles per infected tree.
- Mean_phenotype_per_tree.csv
  - Per-tree raw data for each assessment: infection assessments, height, chlorophyll fluorescence (Fv/Fm), branching, defoliation.
  - Also includes mean values for detailed needle assessments (September 2013 and October 2014).
  - Additional per-tree metadata: population/origin (Population, Pop, Fam), block/position, original tree numbers, fungicide2015 status, geographic coordinates (lat/long), altitude (ALT), and height measurements across years (2009–2015).
- Supporting documentation and data dictionary notes embedded within Mean_phenotype_per_tree.csv
  - Describes fields such as Block, Position, orig no, height_end2015, and seasonal infection metrics (infection_SS_2013-14, infection_AW_2013-14, infection_Total_2013-14, etc.) with notes about log-transformations used in analysis.

## Data schema, units, and metadata
- Infection data
  - Expressed as estimated percentage infection on current year needles (in 5% increments) with specific seasons (spring/summer, autumn/winter, total annual).
  - Some infection metrics are provided as percentages converted to LOG for analysis.
  - Assessments performed by a single observer (Annika Perry) for consistency; culture confirmation of Dothistroma septosporum conducted from September 2013 samples.
- Phenotypic measurements
  - Height: annual measurements at end of growing season or pre-start of next season.
  - Chlorophyll fluorescence: Fv/Fm values (July 2013) to assess plant stress.
  - Branching metrics: counts of branches (main stem and total).
  - Defoliation: estimated percentage of defoliation of previous year needles (October 2014).
- Needle detail data
  - Detailed assays include precise metrics per needle (length of lesions, number of lesions, total needle length) and presence of fruiting bodies (FBV) for 2014.
  - Per-tree summaries include mean values across sampled needles.

## Sampling design and site context
- Site and transplant
  - Torrs Warren site adjacent to stands of Corsican and lodgepole pine with existing DNB pressure.
  - 6 litre pots, 0.5 m spacing, guard row around trial, annual weeding.
  - GPS coordinates provided for key corner trees; data include latitude, longitude, altitude.
- Trial design
  - Six randomized blocks; one individual per family per block.
- Data scope and time frame
  - Assessments every six months (autumn and spring) from 2013 to 2015.
  - Key measurements span 2009–2015 for height, with detailed infection and needle assessments in 2013 and 2014.
- Population and provenance
  - Eight populations with four families each; seeds germinated spring 2007, transplanted in 2013 at age six.

## Data quality, provenance, and data governance
- Data quality controls
  - Infection assessments centralized to a single observer to ensure consistency.
  - Verification of Dothistroma septosporum presence via cultures from September 2013 needles.
- Data completeness and caveats
  - Several trees died or were removed during 2013–2015; a list of dead/missing trees is provided (NA values indicate missing data for affected trees).
  - Some records reflect missing data due to death or removal (e.g., certain blocks/trees have incomplete time-series data).
- Provenance and project context
  - Data originate from a collaborative research effort linked to Annika Perry’s PhD and the PROTREE project, with additional contributions from related researchers.
  - Some advancement in management practices: copper-based fungicide spray applied to blocks 4–6 in July 2015 as part of separate investigations.
- Data formats and interoperability
  - Data provided as structured CSV files with embedded field definitions and unit annotations to support reuse in data catalogues and analyses.
  - Documentation notes are included within the dataset descriptions and in the detailed field metadata.

## Governance considerations for Data Stewards
- Metadata completeness
  - Ensure population, family, block, position, original tree number, spatial coordinates, and multi-year phenotypes are retained and clearly linked across files.
  - Preserve units and data dictionary details (e.g., LNL, LPN, LL, FBV) to maintain interpretability.
- Data quality management
  - Maintain consistency by tracking who collected each metric, and preserve documentation of any re-measurements or data transformations (e.g., log-transformations for infection data).
- Data availability and limitations
  - Monitor and document missing data due to tree mortality, ensuring users understand data gaps and their implications for analyses.
  - Note seasonality and measurement timing to avoid misinterpretation of longitudinal trends.
- Data access and sharing readiness
  - The dataset is well-documented for reuse in phenotypic analyses, GWAS-like investigations, and cross-study collaborations; ensure licenses, usage rights, and provenance are clearly stated in data portals.
- Ongoing stewardship
  - Maintain cross-referencing between detailed needle-level data and per-tree summaries to support flexible analyses (per-needle vs. per-tree aggregates).
  - Support users with guidance on handling data in logarithmic scale for infection metrics and on integrating multiple data files for comprehensive phenotypes.