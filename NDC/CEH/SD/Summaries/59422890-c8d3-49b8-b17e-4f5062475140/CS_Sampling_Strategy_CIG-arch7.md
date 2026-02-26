# The Sampling Strategy for Countryside Survey (up to 2007)

- Purpose and scope
  - Documents the field survey sampling strategy used in Countryside Survey up to 2007.
  - Builds on the ITE Land Classification (ITE LC) framework first used in 1978 to stratify a national ecological survey.
  - Emphasizes the linkage between stratification, sampling design, data collection, and generation of national estimates for habitat features.

- Core concepts for GIS work
  - Spatial stratification: using the ITE Land Classification to carve GB into discrete strata (land classes) to ensure representative sampling.
  - 1 km squares as sampling units: central square of a 15 x 15 km grid, with surrounding squares allocated to refine class membership and context.
  - National estimates: derived by multiplying the mean habitat area per square within a class by the total area of that class, then aggregating across classes.
  - Data products: maps and land-class allocations underpin habitat and landscape-change estimates; results are tied to specific Survey years and country units.

- Evolution of the ITE Land Classification and the sampling framework
  - 1978 (CS1978): first GB-wide land classification using Indicator Species Analysis (ISA) on 1228 centre squares; 32 land classes; eight samples per class (256 total); classify surrounding four squares per centre, totaling ~6040 squares classified.
  - 1984 (CS1984): land-use focus; same sampling framework but 12 squares per class (384 total); eight squares previously visited retained.
  - 1990 (CS1990): shift to All Squares LC; satellite-derived Land Cover Map linked to the program; 508 squares surveyed; extended LC to classify every GB square using surrogates for climate, geology, etc.; incorporation of urban/sea corrections.
  - Post-1990: LC refinement to enable regional/local estimates; substantial reclassification (best surrogate-based classification) led to 62% class correspondence with the original, affecting representation of some classes.
  - 1998 (CS1998/CS2000 planning): LC updated to support separate Scotland reporting; total classes increased to 40; discussion of separate country estimates and representation issues; more GB-wide alignment with policy needs.
  - 2000 (CS2000): formalized separate country estimates (England & Wales, Scotland); LC subdivided into country-unit classes; 40 strata expanded to 40 distinct country-unit strata; additional squares were allocated to ensure adequate representation of new classes; upland habitat sampling added to improve accuracy for England & Wales uplands.
  - 2007 (CS2007): Wales-focused adjustments for Wales-only reporting post-devolution; introduction of five Welsh country-unit classes (5w, 6w, 7w, 15w, 18w) increasing strata to 45; 43 additional Welsh squares added to ensure minimum representation; some English classes reduced to four squares; upland sampling module added (30 extra squares) to improve upland estimates; Wales and England sample distributions adjusted accordingly.

- Sampling and data collection details
  - Sampling units: 1 km squares, selected from a grid centered on 15 x 15 km units; square surrounding strategies applied to classify into land classes.
  - Field surveys: multi-year sequence of field data collection across the evolving LC framework, including habitat types, land-use features, and related environmental attributes.
  - Upland module: independent module added in CS2000/CS2007 to target upland and marginal upland habitats with additional squares for better statistical power.

- Country-specific framework and representation
  - England, Scotland, Wales: LC sub-division into country-unit versions to support country-specific reporting.
  - Wales-specific enhancements: introduction of Welsh LC sub-classes and increased Welsh sample density to support Wales-only estimates.
  - Isle of Man: sampling squares removed from country-unit estimates and replaced to maintain country-specific sampling integrity.

- Outputs and GIS implications
  - Revised LC maps: England with Wales and Scotland LC maps updated to reflect country-unit stratifications (post-2000 and post-2007 revisions).
  - Spatial data for national estimates: class-level means tied to class areas to produce national habitat estimates; changes in classification over time affect cross-survey comparability.
  - Data integration: approach enables longitudinal assessments of habitat change by aligning sampling strata across survey years, while acknowledging classification changes.

- Practical considerations for GIS specialists
  - Class definitions and cross-walks: updated LC schemes require careful cross-walking when integrating multi-year data; be aware of country-unit subdivisions and new Welsh/Scottish subclasses.
  - Sampling rate metrics: “1:x” sampling rates per class and country (as provided in tables) indicate the sampling intensity; important for spatial bias assessment and uncertainty evaluation.
  - Data products workflow: use LC maps as the backbone for stratified sampling, then apply field-derived metrics to produce national estimates of habitat areas and changes.
  - Interpretation caveats: national estimates across years may reflect LC changes in addition to real ecological change; note the “Note Regarding the Creation of National Estimates” about using the latest classification vs. maintaining cross-survey consistency.

- Timeline snapshots (high-level)
  - 1978: 32 Land Classes; 256 samples; ISA-based stratification.
  - 1984: 32 classes; increased sampling per class.
  - 1990: All Squares LC; 508 samples; first GB-wide country-scale volumes; Land Cover Map linked.
  - 1998: 40 classes; Scotland reporting added.
  - 2000: CS2000; separate England&Wales and Scotland estimates; upland module introduced; expanded sampling.
  - 2007: CS2007; Wales-only refinements; 45 strata; Wales-specific class subdivisions; enhanced upland sampling.

- Appendix and references (conceptual)
  - Maintains a detailed history of ITE LC development, key methodological papers, and CS reports that document the sampling design, class definitions, and statistical treatments across survey years.