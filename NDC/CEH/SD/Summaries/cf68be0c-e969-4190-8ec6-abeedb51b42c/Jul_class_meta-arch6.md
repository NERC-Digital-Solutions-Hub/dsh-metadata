# July Classification Metadata

## Overview
- All classifications were produced using a maximum likelihood algorithm.
- Full methodological details are available in the referenced Methods_overview document.
- The content focuses on classifying floral unit clusters in imagery, distinguishing between different pixel types and category groupings, with multiple training set variants to explore how data preparation affects results.

## Key Definitions
- Edge pixels: Pixels at the edge of floral unit clusters or within small clusters where mixing with other features is likely.
- Pure pixels: Pixels deeper inside floral unit clusters, less likely to be mixed with other features.
- Merged categories: Regions of interest from different classification categories that are combined into one or more groups, rather than kept separate.

## Training Set Variants
- July_3cm_classification1: All merged categories, includes edge and pure values.
- July_3cm_classification2: All merged categories, pure values only for Centaurea nigra; edge and pure values for Rubus fruticosus.
- July_3cm_classification3: All merged categories; removal of Centaurea nigra 'a5' signature within the merged Centaurea nigra category; edge and pure values maintained.
- July_3cm_classification4: All merged categories; removal of Centaurea nigra 'a5' signature within the merged Centaurea nigra category; pure values only for Centaurea nigra; edge and pure values for Rubus fruticosus.
- July_3cm_classification5: All merged categories; removal of Centaurea nigra 'a5' signature within the merged Centaurea nigra category; Centaurea nigra edge categories separated out; pure and edge values included.
- July_3cm_classification6: Pure values only for Centaurea nigra with pure values not merged; pure and edge values for Rubus fruticosus.
- July_3cm_classification7: Pure values only for Centaurea nigra; Centaurea nigra 'a5' signature removed; pure values not merged for Centaurea nigra; pure and edge values for Rubus fruticosus.
- July_3cm_classification8: All merged categories; pure values only for Centaurea nigra and Rubus fruticosus.
- July_7cm_classification1: All merged categories; pure values only for Centaurea nigra and Rubus fruticosus.