# Dataset Documentation

- Document Version: 1: 20-11-2015

## Scope and purpose
- Describes the Cumbria_Land_Classification dataset detailing 16 Land Classes (strata) in Cumbria, UK.
- Land classes are defined by environmental characteristics (climate, altitude, slope) and, to a degree, human artefacts.
- Aims to provide a structured, hierarchical classification that reflects geomorphology and land use for planning, analysis, and potential modeling.

## Format, extent, and projection
- Format: ESRI Shapefile
- Resolution: 1 km
- Coordinate system: British National Grid (OSGB36), Transverse Mercator projection
- Extent: Great Britain (Cumbria-focused analysis)
- Projection and metadata are intended to support interoperability and discovery via data portals

## Data collection, sampling, and methods
- Sampling design: A county-wide grid created by selecting the central square from blocks of 3 x 3 km, resulting in an approximately 11% sample.
- Characteristics recorded (from 1-inch scale OS maps): includes map features such as roads, water bodies, land features, soils, vegetation, topography, and human artefacts. Geological attributes were included; drift was excluded due to map limitations.
- Classification approach:
  - Indicator Species Analysis (ISA) used to allocate sample squares to Land Classes.
  - Reciprocal Averaging (RA) ordination employed to assess relationships and test correlations between analyses.
- Data processing: Characteristics were recorded, cleaned, and used to derive a 16-class hierarchy; the analyses support generating a dichotomous key for class assignment and exploring relationships with geography and geology.

## The Land Classes (1–16): brief descriptions
- Land Class 1: Lowland, Solway/Southern coastal plain; flat to gentle; medium-quality pasture with leys; variable soils (brown earths, high nutrients).
- Land Class 2: Slightly higher elevation; Eden Valley/Solway Plain; undulating with hedges; medium to good pasture soils (deep brown earths).
- Land Class 3: Lowland characteristics at 152–229 m; western Eden Valley; limestone landscapes; medium–poor quality pasture; stony brown earths with high calcium.
- Land Class 4: Mixed upland-lowland features; margins of central fells; variable agriculture; coniferous/broadleaf woods; varied soils; well-drained moorland.
- Land Class 5: Near-coastal alluvial plains; good-quality agricultural land (mostly arable and short leys); intensive farming; deep brown earths.
- Land Class 6: Lowland with human artefacts (communications/urban use) on alluvial plains; intensive grazing; deep brown earths.
- Land Class 7: Coastal estuarine sand and mud.
- Land Class 8: Coastal with substantial bare sand/mud; shoreline extensive; improved pasture and leys; hedges; deep, nutrient-rich soils.
- Land Class 9: Markedly upland foothills; conifers planted in blocks; few hedges; poor, blanket moorland used for free-range grazing; acidic, organic, waterlogged soils.
- Land Class 10: Upland with some lowland adjacency; valleys and mountainsides; contrast between valley floor improved pastures and upland moorlands; poor, shallow, acidic brown earths.
- Land Class 11: Complex mid-fells; features from both upland and lowland; broadleaved woods; poor agricultural land (upland grassland) with marginal grazing; variable soils.
- Land Class 12: Featureless low fells; extensive conifer plantations; poor land with improved pasture and well-drained moorland; acidic brown earths and peats.
- Land Class 13: Steep margins of Pennines/Skiddaw; few trees; poor, poorly drained moorland; extensive sheep/cattle grazing; deep peat soils.
- Land Class 14: High-altitude summits and plateaux; Pennines and some upland masses; no trees; open-range sheep grazing; deep peat soils with gleys/peats present.
- Land Class 15: Upper slopes of central Lake District fells; rugged, little tree cover; poor land with moorland and upland grassland; peat-rich soils.
- Land Class 16: Summits and highest slopes of central Lake District fells; most mountainous; no trees; poor land with peat-dominated soils.

## Hierarchy and interpretation
- The Land Classes form a hierarchical system (Figure 2) with upland vs. lowland as the major division.
- Altitude strongly influences class separation, but geology and land use (artefacts) also shape the hierarchy.
- The arrangement reflects regional patterns: coastal classes (7–8) are distinct from upland classes (13–16); lowland classes (1–6) show strong block-like distribution, while upland classes form more cohesive patterns due to valley fragmentation.

## Distribution and statistics
- The county-wide summary indicates nearly two-thirds of Cumbria is classed as lowland.
- Some classes occur in large blocks (e.g., 1 and 2), while others occur in smaller clusters (e.g., 4 and 11).
- The pattern of upland classes shows more localized, cohesive distributions due to geomorphology.
- Table 2 provides the frequency of each land class; Table 3 shows associations between Land Classes (which classes tend to co-occur).

## Analysis approach and outputs
- The study used multivariate analysis to derive the land-class hierarchy and to interpret relationships between class membership and environmental attributes.
- A dichotomous key (Figure 3) enables classification of remaining squares based on recorded characteristics.
- Figure 4 maps the spatial distribution of Land Classes.

## Data quality, limitations, and caveats
- Data are from the 1970s (baseline ecological survey and reanalysis published later); applicability to current conditions may require updates.
- 1 km resolution may limit local-scale planning; some attributes (e.g., boundaries, drift) were constrained by historical mapping.
- The sample design (11% systematic sample) may influence representation of rare or fragmented classes.
- The dataset provides broad geographical and ecological context, but linking to other datasets may require careful standardization due to historical data formats and potential mismatches.

## References and further reading
- Bunce, R. G. H., Morrell, S. K., & Stel, H. E. (1975). The application of multivariate analysis to regional survey. Journal of Environmental Management.
- Hill, M. O. (1973). Reciprocal averaging: an eigenvector method of ordination. Journal of Ecology.
- Hill, M. O., Bunce, R. G. H., & Shaw, M. W. (1975). Indicator species analysis, a divisive polythetic method of classification, and its application to a survey of native pinewoods in Scotland. Journal of Ecology.