# Dataset Documentation Countryside Survey data © NERC - Centre for Ecology & Hydrology

## Overview
- National estimates of landscape linear feature stock for 1984, calculated using the 2007 ITE Land Classification.
- Estimates are reported as total lengths (in metres) per 1km square per Land Class.
- Note: negative values may appear in the LC2007 column due to the statistical model; treat these as zero.
- Data describe six major linear feature types and a total length, with associated spatial geometry and area metrics.
- Features are reported in a hierarchical system that prevents double counting; hedges have precedence when co-occurring with other features.

## Data structure and key fields
- FID: Feature ID (autonumber)
- LC2007: ITE Land Class (numeric)
- LC2007_COD: ITE Land Class code (text)
- CSYEAR: Year of survey (numeric)
- LCAREA: Total area of the relevant Land Class (00s ha)
- LF_1: Hedges (metres per 1km square per land class)
- LF_3: Wall (metres per 1km square per land class)
- LF_4: Line of trees/shrubs/relict hedge/fence (metres per 1km square per land class)
- LF_5: Line of trees/shrubs/relict hedge (metres per 1km square per land class)
- LF_6: Bank/grass strip (metres per 1km square per land class)
- LF_7: Fence (metres per 1km square per land class)
- LFTOTAL: Total length of linear features (metres per 1km square per land class)
- Shape_Length: Length of Land Class shape
- Shape_Area: Area of Land Class (square metres)

## Reporting methodology and interpretation
- Six major feature types are used for reporting; combinations of codes allow multiple reporting formats.
- No double counting of multi-element features; hedges take precedence in reporting when co-occurring with other features.
- If a hedge is present alongside walls, fences, or other features, hedge length is reported, and the corresponding wall/fence lengths do not double-count that hedged portion.
- The reporting system is designed to capture stock of features at the 1km square scale across land classes.

## Usage limitations and rights
- All use of Countryside Survey (CS) data must be acknowledged.
- Acknowledgement required: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology.
- Countryside Survey © / Database rights reserved.
- Use in publications, presentations, or datasets should include the above acknowledgement.

## References and related resources
- Carey, P.D., et al. (2008). Countryside Survey: UK Results from 2007. NERC/CEH.
- Scott, W.A. (2007). CS Technical Report No.4/07 Statistical Report.
- Bunce, R.G.H., et al. (1997–2007). ITE Land Classification publications and datasets.
- ITE Land Classification 2007 vector dataset (Bunce, Barr, Whittaker).
- Additional background: Merlewood Land Classification documentation and related handbooks.

## Access and further information
- Countryside Survey Website: http://www.countrysidesurvey.org.uk/
- Related publications and methodologies linked through the Countryside Survey website and referenced reports.