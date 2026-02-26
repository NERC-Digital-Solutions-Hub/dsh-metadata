# Supporting documentation on the patch-discovery experiment

## What the dataset covers
- Study location: Wytham Woods, Oxfordshire, UK (51°46′N, 1°20′W)
- Species studied: great tit, blue tit, and marsh tit
  - Codes: greti (great tit), bluti (blue tit), marti (marsh tit)
- Purpose: investigate how changes in local population density influence discovery of a novel food patch
- Timeframe: January–March 2021
- Data collected by: field team including Keith McMahon, Sam Croft, and Kristina Beck

## Experimental design and procedure
- Subjects: birds captured during winter (mist nets) or spring (nestboxes) and fitted with metal leg rings and PIT tags
- Patch setup:
  - A novel feeder placed near two existing feeders (~40 m apart) at each site
  - Novel feeders positioned in opposite directions within a site
  - Second patch-discovery phase used different locations during density manipulation
  - Feeders supplied sunflower seeds and accessible to all PIT-tagged birds
  - Design matched to existing feeders to avoid neophobia effects
- Timing:
  - Setup occurred the day before (after sunset) or on the day of (before sunrise)
  - Novel feeders remained in place for one day
- Context: part of a broader experimental manipulation of local population density (linked to Supporting documentation_Exp_density)

## Data structure and fields
- Single CSV file containing:
  - date
  - time
  - logger (the novel feeder identifier)
  - Site (experimental site identity)
  - Bto.ring (individual identifier)
  - Bto.species.code (species code: greti, bluti, marti)

## How this data can be used
- Analyze the time and order in which individuals discover the novel patch
- Compare discovery dynamics before vs. during density manipulation
- Examine species- and site-specific patterns in patch discovery
- Combine with density-manipulation data (Supporting documentation_Exp_density) for integrated analyses

## Data provenance and quality considerations
- Identifies individuals via PIT tags, enabling robust longitudinal tracking
- Consistent coding of species and site for cross-dataset analyses
- Time and date stamps should be interpreted in local time; ensure alignment when merging with other datasets

## References
- Savill P, Perrins C, Kirby K, Fisher N. 2011. Wytham Woods: Oxford's ecological laboratory. Oxford University Press. 
- Supporting documentation_Exp_density (for the density manipulation context)