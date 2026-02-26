# Dataset Documentation

## Purpose and scope
- National estimates of landscape linear feature stock for 1998, calculated using the 2007 ITE Land Classification.
- Outputs are presented as total lengths (metres) for each linear feature type per 1km square per Land Class.
- Notes: negative values may appear in LC2007-related columns due to the statistical model; treat negative values as zero.

## Data structure and key variables
- FID: Feature ID (autonumber), Object ID
- LC2007: ITE Land Class (numeric)
- LC2007_COD: ITE Land Class (text code)
- CSYEAR: Year of survey (1998)
- LCAREA: Total area of relevant Land Class
- LF_1: Hedges (metres per 1km square per land class)
- LF_3: Wall (metres per 1km square per land class)
- LF_4: Line of trees/shrubs/relict hedge/fence (metres)
- LF_5: Line of trees/shrubs/relict hedge (metres)
- LF_6: Bank/grass strip (metres)
- LF_7: Fence (metres)
- LFTOTAL: Total length of linear features (metres)
- Shape_Length: Length of Land Class shape
- Shape_Area: Area of Land Class (square metres)

## Feature definitions and reporting rules
- Six major feature types reported: hedge, wall, line of trees/shrubs/relict hedge/fence, line of trees/shrubs/relict hedge, bank/grass strip, fence; TOTAL sums total linear features.
- Hedge features have precedence: a hedge is counted if present, even if associated with walls/fences.
- No double counting: stock estimates for walls and fences exclude lengths that are found with a hedge.
- Information is reported using a hierarchical coding system that allows reporting in multiple ways depending on code combinations.
- Aims to support clear, policy-relevant indicators of environmental structure and hedgerow ecology.

## Methodology and data provenance
- Based on Countryside Survey data; national estimates derived from the 1km survey sample squares using the 2007 ITE Land Classification.
- References to supporting methodological work and datasets are provided (e.g., Scott 2007; Bunce et al. 2007, 1996; other background reports).
- Data are intended to be verified, quality assured, cleaned, and transformed prior to analysis and reporting.

## Use, outputs, and data management
- Outputs typically delivered as reports, maps, and charts illustrating environmental health indicators (e.g., linear feature stock by land class).
- Datasets are designed to be stored and uploaded to appropriate data portals; data users should follow standard Countryside Survey usage guidelines.
- Acknowledgement and copyright: Countryside Survey data owned by NERC - Centre for Ecology & Hydrology; all rights reserved; use must include the provided acknowledgement.

## Access, citations, and references
- Countryside Survey Website provides project overview and methodological documents: http://www.countrysidesurvey.org.uk/
- Key publications and datasets referenced for context and reproducibility (e.g., 2007 UK results report, technical reports on statistical methods, and ITE Land Classification references).

## Use limitations and acknowledgements
- All use of Countryside Survey data must be acknowledged with the specified statement.
- Includes standard copyright notice: Countryside Survey © NERC - Centre for Ecology & Hydrology; all rights reserved.

## Relevance for environmental monitoring analysts
- Provides standardized, comparable metrics of landscape linear features to assess environmental health and policy performance over time.
- Data quality steps align with typical monitoring practices: source verification, standardised classification, and clear reporting formats.
- Facilitates data integration by offering a consistent structure andClearly defined features, enabling broader analyses when combining with other datasets.
- Supports accessibility goals by highlighting data provenance and the importance of underlying data access for secondary analyses.