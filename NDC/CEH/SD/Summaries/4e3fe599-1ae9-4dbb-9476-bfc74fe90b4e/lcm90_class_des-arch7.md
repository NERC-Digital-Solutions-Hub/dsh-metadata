# The Land Cover Map of Great Britain: an automated classification of Landsat Thematic Mapper data

## Aim and approach
- The Land Cover Map of Great Britain (LCMGB) is produced from supervised maximum likelihood classifications of Landsat Thematic Mapper (TM) data.
- Base data: 25 m grid with 25 target cover-types (e.g., sea, inland water, beaches/bare ground, arable land, and 18 semi-natural vegetation types).
- Two-level product structure:
  - Full 25-class dataset (25 m resolution) plus two additional summarised outputs.
  - Two aggregated outputs: 17 key classes (uppercase A–Q) and 1 km summary data.
- Classification uses summer–winter data combinations to improve accuracy over single-date analyses.
- End-users can tailor outputs by aggregating subclasses in GIS or using non-standard customized data.

## Data characteristics and outputs
- Spatial resolution and data products:
  - 25 m native resolution: 25 target classes (values 0–25; 0 = unclassified).
  - 1 km summary: for each of the 25 target classes, the percentage within each 1 km cell (e.g., if 320 of 1600 TM pixels in a 1 km cell are class 10, layer 10 shows 20%).
  - 17 key-class dataset: available as 1 km summary data; designed to improve consistency when rare classes are inconsistently mapped.
- Class mapping structure:
  - 25 target classes cover a broad range of land cover categories (marine, terrestrial, vegetation, agricultural, woodland, wetlands, moorland, urban/suburban development, bare ground, etc.).
  - 17 key classes provide a coarser, more consistently mappable schema, with a defined mapping between the 25 target classes and the 17 key classes (Table 1 in the document).
- Minimum mapping unit:
  - The practical minimum mappable area is close to 1 ha; theoretically, features down to 0.125 ha (two pixels) can be represented, but not all 0.125 ha features are consistently shown.
- Regional differentiation:
  - The data provides lowland vs. upland distinctions; some regional inconsistencies may remain, and regional masks may be used to refine classifications in GIS.

## Classification methodology and accuracy
- Methodological notes:
  - Class labels reflect ecologically meaningful groupings rather than purely spectral separability.
  - Ground-truth data are limited and variations in definitions across surveys affect apparent accuracy.
  - A significant portion of error arises from mixed boundary pixels (pixels spanning vector boundaries) and from temporal changes between survey dates.
- Accuracy assessment:
  - Comparisons with independent ground-reference data show varying correspondences depending on detail level and class definitions.
  - When boundary pixels are excluded, correspondence improves; including boundary pixels reduces accuracy.
  - Overall, a realistic accuracy range is approximately 80–85%, accounting for definition differences, temporal change, and data limitations.
  - Typical observed figures: ~67–71% correspondence after accounting for definition differences and time gaps; ~76% when allowing for boundary issues and time-based changes.
- Implications for users:
  - The 80–85% realism figure is an average; local accuracy may differ.
  - Users should be cautious of cross-class confusion (e.g., between similar vegetation/land-use types) and misregistration impacts in dissected landscapes.
  - Ground-truth limitations mean exact validation against a single standard is not feasible; use cross-survey comparisons to understand potential error sources.

## Land cover classes: overview of the 25 target and 17 key types
- The 25 target classes cover a spectrum from sea and inland water to bare ground, arable land, and various vegetation types (grasslands, heaths, bogs, scrub, woodland, moorland) plus urban development and bare ground.
- The 17 key classes provide a consolidated set to improve consistency, with clear crosswalks to the 25 target classes.
- Each class is described in terms of spectral characteristics, typical land-use context, seasonal behavior (summer vs. winter imagery), and limitations (e.g., difficulty distinguishing certain subtypes or regional variations).
- Examples of broad categories:
  - Sea/Estuary and Inland Water
  - Beach/Mudflat/Cliffs and Saltmarsh
  - Grass Heath, Pasture/Meadow/Amenity Grass, and various grassland management types (e.g., mown/grazed turf vs. meadow/verge)
  - Marsh/Rough Grass, Bracken, Moorland Grass, and various heath/moor types
  - Bogs (lowland and upland)
  - Deciduous and Coniferous Woodlands
  - Arable/Tilled Land and temporarily bare ground
  - Suburban/Rural Development and Urban Development
  - Inland Bare Ground
- Subclass aggregation and mapping flexibility:
  - Subclasses (e.g., specific crops) are aggregated into ecologically meaningful target classes.
  - Users can recombine subclasses in GIS to suit objectives, accepting potential reductions in cross-class consistency.

## Using the data for GIS work
- Standard products:
  - 25-class dataset (25 m) with values 0–25.
  - 1 km summary data for each target class (percentage area per 1 km cell).
  - 17-class 1 km summary dataset for consistency-focused mapping.
- Customization:
  - Non-standard outputs (e.g., a reduced set of target classes) can be generated digitally from the original maps.
  - Aggregation decisions can be made in GIS, recognizing that some subclass distinctions may not be reliably separable in all imagery dates.
- Practical considerations:
  - The minimum mappable unit and regional differences imply some caution when applying the data to fine-scale planning.
  - Where context (altitude, latitude, climate) would improve separations, GIS-based contextual rules are recommended.

## Limitations and caveats
- Definitions and sampling differences between different surveys influence accuracy assessments.
- Boundary pixel misclassification and misregistration can affect map fidelity, especially in dissected landscapes.
- Temporal changes (e.g., land-use changes between dates) can reduce direct comparability across surveys.
- Some rare or regionally inconsistent classes (e.g., ruderal weeds) may be mapped less consistently; a simplified 17-class approach can mitigate this.

## References and further details
- Key methodological and accuracy references are provided, including Congalton (1991) on accuracy assessment, Fuller et al. (1989–1995) on remote sensing classification of grasslands and land cover, Townshend (1983) on resolution effects, and Wyatt et al. (1994) on land cover definition comparisons.
- The document notes that additional evaluation work is in preparation to compare ground and satellite survey correspondences in greater detail.

## Practical takeaways for GIS Specialists
- The LCMGB provides a robust, map-based land cover product derived from Landsat TM data, with both high-resolution (25 m) and coarser (1 km) outputs and a standardized 25-class schema plus a more consistent 17-class aggregation.
- Users should leverage the 1 km summary data for regional analyses and the 25 m data for detailed mapping, while being mindful of inherent accuracy limits and boundary effects.
- Custom aggregation and context-driven classifications are feasible in GIS, but users should document any reclassifications or regional generalizations due to potential inconsistencies.
- The dataset is especially useful for policy, planning, and ecological assessments where understanding broad land cover patterns and changes over time is important, provided that the caveats regarding accuracy and temporal differences are considered.