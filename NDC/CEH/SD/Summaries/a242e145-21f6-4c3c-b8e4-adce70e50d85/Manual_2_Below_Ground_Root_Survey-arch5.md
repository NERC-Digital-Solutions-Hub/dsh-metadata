# ESPA p4ges PROJECT Work Package Carbon (WP4-Carbon)

## Context and aims
- The p4ges project in Madagascar aims to influence payment for ecosystem services by quantifying carbon stock across land uses, with a focus on belowground biomass (BGB) in the Ankeniheny Zahamena corridor (CAZ).
- WP4-carbon specifically quantifies carbon in BGB (root biomass) across five IPCC pools, emphasizing accurate direct measurement and comparison of BGB estimation methods.
- Objectives include: direct BGB measurement on selected trees, evaluation of BGB quantification methods, calculation of BGB per tree to enable later stand-level estimates, and development of allometric equations linking BGB to tree metrics.

## Datasets and archiving
- Datasets generated include direct BGB measurements by tree, root categories (stump, coarse roots CR ≥10 mm, medium roots MR 2–10 mm, fine roots FR <2 mm), soil horizons, and associated field measurements.
- Aboveground biomass (AGB) was measured directly in parallel for cross-validation and allometric modeling.
- All data produced under the methodology described in this manual have been archived at Environmental Information Data Centre (EIDC), ensuring long-term preservation and sharing readiness.

## Study area
- Location: humid tropical CAZ forest corridor in eastern Madagascar (370,032 ha).
- Four Zones of Interest (ZOIs): Lakato (ZOI1), Andasibe (ZOI2), Anjahamana (ZOI3), Didy (ZOI4). ZOI selection based on biophysical criteria, access, and deforestation history.
- For BGB direct measurements, two ZOIs (Anjahamana and Andasibe) were retained due to pronounced differences in stand-level AGB and field access considerations.

## Data design and sampling strategy
- Focus on Closed Canopy forest within the four ZOIs.
- Site and target-tree selection aimed to represent the contribution of different DBH classes to site AGB, prioritizing dominant species and ensuring feasible fieldwork within time and cost constraints.
- Target trees: 54 individuals across two zones, three sites per zone, three dominant species per site, and three DBH classes (large ≥20 cm, medium 10–<20 cm, small 5–<10 cm).
- Tree selection and sampling balance representation across zones, sites, species, and diameter classes while respecting field and regulatory constraints.

## Field methods

### Method: Voronoï polygon
- Purpose: allocate root influence area for a target tree by constructing a Voronoï polygon using the target and neighboring trees’ positions and DBH.
- Experimental design:
  - Record target tree and up to four neighboring trees (species, DBH, height).
  - Measure distances from the target to neighbors; compute relative area share xi% of the target’s space.
  - Delimit the Voronoï polygon in the field and calculate its area by triangulation (area of triangles from height and base).
- Root data collection within each polygon:
  - Select 1 triangle for small trees (5–<10 cm DBH) and 2 triangles for medium/large trees.
  - Excavate around the target within the polygon, separating root categories (FR, MR, CR; plus CR0 above soil).
  - Weigh stump separately; wash roots; collect samples for lab analysis.
  - Measure ramification details for coarse roots (length, diameters, and diameter changes along ramification), then weigh and sample.
- Depth horizons considered: 0–10 cm (topsoil), 10–30 cm (subsoil), 30–50 cm (deep soil).

### Method: Pits
- Purpose: alternative direct measurement by excavating roots in three pits around the target tree.
- Design: three 1 m² pits arranged at the vertices of an equilateral triangle with center at the target tree; 10 m distance from center to vertices; 120° between vertices.
- Data collection: same root categories, soil depths, washing, weighing, and lab sampling as in Voronoï method.

## Laboratory work
- Samples dried in an oven at 75°C until constant weight.
- Dry weights recorded for every root category (FR, MR, CR, stump) per method.
- Dry weights used to compute total tree-level BGB and to develop allometric equations for stand-level estimates.

## Calculation and data processing

### Root biomass (tree level)
- For Voronoï, root biomass per tree derived by combining measured dry weights with the corresponding polygon area (triangles within the polygon).
- For pits, sum dry weights from the three pits.
- Resulting tree-level BGB data feed into allometric model development to enable stand-level BGB and carbon estimates.

### Aboveground biomass (direct measurement)
- AGB components (trunk, branches, leaves) measured directly after tree harvest.
- Direct AGB data used in tandem with Chave et al. (2014) allometric equations to benchmark or develop site- and species-specific models.

### Allometric modeling and upscaling
- AGB site values estimated with a robust allometry (Chave et al., 2014) using DBH and wood density where applicable.
- Tree-level BGB used to derive allometric equations; stand-level BGB and carbon stock estimated by upscaling across sites and zones.
- Carbon units reported as appropriate (e.g., Mg C ha^-1) for consistency with IPCC conventions.

## Data governance, metadata, and standards
- Glossary, abbreviations, and units included to standardize terminology and ensure consistent interpretation across datasets.
- Data archiving at EIDC supports discoverability, reuse, and long-term stewardship.
- Data collection protocols emphasize reproducibility (clear field methods, root category definitions, soil horizons, and excavation procedures) and transparent calculation steps.
- Potential data governance considerations include: field access restrictions, site exclusions, embargoes or usage restrictions due to protected areas, and documentation of deviations from planned sampling (e.g., selection of only 2 ZOIs).

## Challenges and limitations
- Incomplete or evolving understanding of user needs for BGB data and broad dataset interoperability.
- Timely collection and processing of data given field constraints, regulatory access restrictions, and the complexity of root excavation in humid tropical forests.
- Interoperability across methods (Voronoï vs pits) and large, heterogeneous root data across multiple zones, species, and DBH classes.
- Use of direct measurement requires destructive sampling and careful documentation to enable reproducibility and future modeling.

## Conclusions and outcomes
- Data collected support development of direct BGB measurements and the creation of allometric models for root and aboveground biomass.
- The generated carbon stock data contribute to understanding carbon dynamics in CAZ forests and support REDD+-related sustainability efforts in Madagascar.
- Datasets archived at EIDC will enable future analyses, cross-site comparisons, and integration into broader ecosystem service assessments.

## References and further reading
- References cited reflect methods and foundational allometric models (e.g., Chave et al., 2014) and root biomass methodologies (Levillain et al., 2011; Saint-André et al., 2005; Vogt et al., 1998; Ravindranath & Ostwald, 2008).