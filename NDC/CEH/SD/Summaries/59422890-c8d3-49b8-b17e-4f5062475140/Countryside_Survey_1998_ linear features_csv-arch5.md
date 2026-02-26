# Dataset Documentation

## Overview
- National estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
- Results are total lengths (in 000s of km) for each linear feature type per Land Class, with lower, mean, and upper estimates and land class area.
- Data are derived from field survey codes and are reported so that multi-element features are not double-counted; hedges have reporting precedence when co-occurring with other features.

## Data structure and fields
- YEAR: Year of Survey (data type = number)
- LAND_CLASS: ITE Land Class (data type = text)
- FEATURENO: Linear feature code (data type = text)
- FEATURE: Linear feature description (data type = text)
- LOWER_ESTIMATE: Lower 95% CI estimate (000s km) (data type = number)
- MEAN_ESTIMATE: Mean estimate (000s km) (data type = number)
- UPPER_ESTIMATE: Upper 95% CI estimate (000s km) (data type = number)
- LAND_CLASS_AREA: Total area of the relevant Land Class (00s ha) (data type = number)

## Feature codes and definitions
- _1 = Hedge: A line of woody vegetation managed to alter natural shape; may occur with other features.
- _3 = Wall: Built stone/manufactured wall; may include fences or banks/grass strips.
- _4 = Line of trees/shrubs/relict hedge/fence: Line of trees/shrubs in natural shape, including those planted as hedges with a fence.
- _5 = Line of trees/shrubs/relict hedge: Line of trees/shrubs in natural shape; includes avenues; may include banks/grass strips.
- _6 = Bank/grass strip: Earth or stone-faced bank or grass strip, with/without a fence.
- _7 = Fence: Permanent post-and-wire/rail structure; may be alongside grass strip, ditch, or stream.
- TOTAL: Total length of all linear features.
- Reporting rule: No double counting of multi-element features; hedges take precedence in reporting when alongside other features.

## Methodology and interpretation
- Features are reported using a hierarchical six-major-feature system.
- Hedge lengths are prioritized when co-occurring with walls or fences; walls/fences are not counted where they coincide with a hedge.
- Negative values may appear in LOWER_ESTIMATE (due to the statistical model); treat negative values as zero for analysis.
- The full dataset links field codes to descriptive metadata to facilitate interoperability and reuse.

## Use limitations and licensing
- All use of Countryside Survey data must be acknowledged.
- Acknowledgement: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey ©; Database Right/Copyright NERC- Centre for Ecology & Hydrology; all rights reserved.

## Provenance and references
- Data originate from Countryside Survey field surveys; national estimates are generated from 1 km survey squares (see Scott 2007).
- Related references and background:
  - Scott, W.A. (2007). CS Technical Report No.4/07 Statistical Report.
  - Bunce, R.G.H., Barr, C.J., Clarke, R.T., Howard, D.C., Lane, A.M.J. (1996, 2007). ITE Land Classification references.
  - Haines-Young, R.H. et al. (2000). Accounting for nature: assessing habitats in the UK countryside.
- Key documents and metadata available via the Countryside Survey Website:
  - http://www.countrysidesurvey.org.uk/
  - Carey, P.D. et al. (2008) Countryside Survey: UK Results from 2007.
  - Additional methodological and technical reports listed in the dataset documentation.