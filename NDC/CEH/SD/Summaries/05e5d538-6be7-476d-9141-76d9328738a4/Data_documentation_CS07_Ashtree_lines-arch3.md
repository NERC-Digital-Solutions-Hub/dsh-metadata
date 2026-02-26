# Countryside Survey: Ash tree distribution in woody linear features 2007

## Overview
- Provides estimates of ash trees in Great Britain within woody linear features, derived from Countryside Survey 2007 data.
- Dataset CS07_Ashtree_Linears includes ash-length estimates by land class and feature type; linked to ITE Land Classification (2007) and Countryside Survey outputs.
- Scale and scope: 1 km resolution across Great Britain; coordinate system OSGB36 (British National Grid).

## Dataset content and structure
- Columns and meanings:
  - LC2007: Land Class (numeric)
  - LC2007_COD: Land Class (text)
  - LC_2007: Land Class (same as above, without codes for non-hedge areas)
  - Area of Land Class: area in m2 (from original land classification file)
  - Size_of_LC: same as Area of Land Class
  - WNS_km: length of ash in natural-shaped lines of trees (km)
  - WUS_km: length of ash in unnatural-shaped lines (hedgerows) (km)
  - Belt_km: length of ash in belts of trees (km)
  - All_WLF_km: total ash length across WNS_km, WUS_km, Belt_km (km)
  - Mean_km_km: mean length of all linear features per km2
- Features covered:
  - Woody Linear Features (WLFs): lines < 5 m wide, including lines of trees (natural shape) and hedgerows (unnatural shape)
  - Belts of trees: belts or belts of scrub
  - Minimum recorded lengths: 20 m with gaps up to 20 m
- Ash estimation bands:
  - For lines of trees: ash proportions allocated in bands (e.g., <10%, 10–25%, 25–50%, 50–75%, 75–95%, 95–100%, Individual Tree); bands use midpoints to estimate ash length per 1 km square
  - For belts: same approach, with additional methods for hedges using D plots (vegetation diversity plots) to derive ash proportion

## Methodology and national upscaling
- Sampling design:
  - Countryside Survey uses 1 km square samples across GB, stratified by land classes representing ecological gradients (soils, geology, climate)
  - Enables scaling up from sample means to national estimates by land class areas
- Calculation approach:
  - Lines of trees (natural shapes): estimate ash length per 1 km square per strata using band midpoints; multiply by Land Class area; sum across squares to obtain country totals
  - Belts of trees (and belts of scrub): apply same method as lines of trees
  - Unnatural-shaped WLFs (hedgerows): species composition not recorded per length; ash estimation relies on D plots data adjacent to hedges
    - Use total percentage cover from D plots next to hedges, per sampling strata, to estimate ash proportion
    - Multiply ash proportion by total hedge length within strata, then by 1 km square means, and scale by Land Class areas to national totals
- Data sources and references:
  - Methods and context described in accompanying CS outputs and technical reports
  - Further information available at www.countrysidesurvey.org.uk

## Associated datasets and sources
- ITE Land Classification (2007) (DOI link provided in the dataset documentation)
- Countryside Survey (core outputs and UK results for 2007)
- Related technical reports and papers listed in the documentation (e.g., CS Sampling Strategy, LCM2007 land cover mapping, and distribution analyses)

## Key definitions and notes
- Woody Linear Features (WLFs): landscape elements <5 m wide forming lines (e.g., hedgerows, belts)
- Natural Shape vs Unnatural Shape: natural lines of trees vs hedgerows
- D plots: vegetation diversity plots adjacent to hedges used to infer species composition and ash proportion in hedges
- Data resolution and extent: 1 km grid cells covering Great Britain; OSGB1936 projection

## Practical applications for monitoring and policy
- Enables monitoring of ash distribution in hedgerows and belts as part of environmental health assessments
- Supports policy evaluation on habitat connectivity, tree diversity, and disease risk management (e.g., ash dieback) at national and regional scales
- Provides metadata-rich, governance-ready data for reporting and decision-making, with explicit linkage to data sources and classification schemes

## Data quality, governance, and challenges
- Data quality themes reflected in the dataset:
  - Stratified sampling design helps represent ecological gradients
  - Metadata completeness and alignment with land classifications are essential for verifiable results
  - Transformation steps required to reconcile banded proportion data with line-length estimates
- Governance considerations:
  - Dataset relies on public sharing of underlying data and clear provenance from Countryside Survey outputs
  - Open data and data sharing can be barriers where datasets require transformation or face access constraints
- Common challenges noted in monitoring contexts (as context for using this dataset):
  - Gaps in data availability or access
  - Inter-organizational silos hindering data sharing
  - Metadata inadequacies complicating reuse and verification
  - Need for robust data governance to ensure datasets meet standards and remain up to date

## Further reading
- Distribution of Ash trees (Fraxinus excelsior) in Countryside Survey data (2013) – Maskell et al.
- Countryside Survey: UK Results from 2007 (Carey et al.)
- CS Technical Report No 11/07: Final Report for LCM2007 (Land Cover Map)
- Key methodological references and historical planning documents (sampling strategy, land classification, and related outputs)