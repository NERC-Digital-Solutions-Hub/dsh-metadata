# July Classification Metadata

- All classifications were performed using a maximum likelihood algorithm. For full methods, refer to 'Methods_overview'.

- Definitions
  - Edge pixels: Pixels at the edge of floral unit clusters or in centers of small clusters where the pixel appears mixed with other features.
  - Pure pixels: Pixels deeper in the center of floral unit clusters, less likely to be mixed with other features.
  - Merged categories: Regions of interest for different classification categories that are merged into one or multiple groups rather than left separately.

- Training set variants
  - July_3cm_classification1: All merged categories, edge and pure values.
  - July_3cm_classification2: All merged categories, pure values only for Centaurea nigra; edge and pure values for Rubus fruticosus.
  - July_3cm_classification3: All merged categories, removal of Centaurea nigra 'a5' signature within merged Centaurea nigra category, edge and pure values.
  - July_3cm_classification4: All merged categories, removal of Centaurea nigra 'a5' signature within merged Centaurea nigra category, pure values only for Centaurea nigra, edge and pure values for Rubus fruticosus.
  - July_3cm_classification5: All merged categories, removal of Centaurea nigra 'a5' signature within merged Centaurea nigra category, Centaurea nigra edge merged categories separated out, pure and edge values.
  - July_3cm_classification6: Pure values only for Centaurea nigra and pure values not merged; Pure and edge values for Rubus fruticosus.
  - July_3cm_classification7: Pure values only for Centaurea nigra, Centaurea nigra 'a5' signature removed, pure values not merged for Centaurea nigra; Pure and edge values for Rubus fruticosus.
  - July_3cm_classification8: All merged categories, pure values only for Centaurea nigra and Rubus fruticosus.
  - July_7cm_classification1: All merged categories, pure values only for Centaurea nigra and Rubus fruticosus.