# July Classification Metadata

## Overview
- All classifications were carried out using a maximum likelihood algorithm.
- Full methods for carrying out classifications are available in 'Methods_overview'.

## Key Definitions
- Edge pixels: Pixels at the edge of floral unit clusters or in the centre of small clusters where the pixel appears mixed with other features.
- Pure pixels: Pixels deeper in the centre of floral unit clusters, less likely to be mixed with other features.
- Merged categories: Regions of interest for different classification categories are merged into one or multiple groups rather than left separate.

## Training Set Variants
- 'July_3cm _classification1': All merged categories, edge and pure values.
- 'July_3cm_classification2': All merged categories, pure values only for Centaurea nigra; edge and pure values for Rubus fruticosus.
- 'July_3cm_classification3': All merged categories, removal of Centaurea nigra 'a5' signature within merged Centaurea nigra category, edge and pure values.
- 'July_3cm_classification4': All merged categories, removal of Centaurea nigra 'a5' signature within merged Centaurea nigra category, pure values only for Centaurea nigra, edge and pure values for Rubus fruticosus.
- 'July_3cm_classification5': All merged categories, removal of Centaurea nigra 'a5' signature within merged Centaurea nigra category, Centaurea nigra edge merged categories separated out, pure and edge values.
- 'July_3cm_classification6': Pure values only for Centaurea nigra and pure values not merged; pure and edge values for Rubus fruticosus.
- 'July_3cm_classification7': Pure values only for Centaurea nigra, Centaurea nigra 'a5' signature removed, pure values not merged for Centaurea nigra; pure and edge values for Rubus fruticosus.
- 'July_3cm_classification8': All merged categories, pure values only for Centaurea nigra and Rubus fruticosus.
- 'July_7cm_classification1': All merged categories, pure values only for Centaurea nigra and Rubus fruticosus.

## Implications for Monitoring Frameworks
- Demonstrates use of a maximum likelihood approach and the need to reference full methodological details (Methods_overview) for reproducibility.
- Highlights the importance of clearly defined pixel categorization (edge vs. pure) and the handling of merged categories in analysis workflows.
- Shows how multiple training set variants can be used to explore how category merging, signature removal, and selective inclusion of pure/edge values affect outcomes.
- Underscores the need for thorough metadata and documentation of dataset configurations to enable transparent, comparable monitoring results.