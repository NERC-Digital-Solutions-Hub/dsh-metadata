# Countryside Survey: Measuring Habitat Change over 30 years 1978 Data Rescue - Final Report (CEH Project no.: NEC03689)

## Executive summary
- Purpose: rescue and digitize the 1978 Countryside Survey land-cover maps to enable long-term, comparable analysis of Broad Habitat stocks across Great Britain, extending the national time series back to 1978.
- Data created: scanned originals, digitized 1978 maps into a GIS, and linked field codes to Broad Habitat classifications; integrated with later Countryside Survey datasets (1984, 1990, 1998, 2007).
- Methodology: use a 15x15 km grid approach with Indicator Species Analysis to define Land Classes; calculate national habitat stocks from mean habitat per square within each Land Class multiplied by Land Class area.
- Validation: comprehensive data checking against original maps and cross-year datasets; anonymization of survey square locations to protect scientific integrity.
- Key caveats: 1978 uses an older Land Classification (vs. revised 1990 All Squares framework); sample size and class definitions affect direct comparability with later years; several habitat categories required nuanced interpretation (ambiguous codes, upland mosaics).
- Value for analysts: extends the GB habitat time-series, enabling trend analysis, driver assessment (e.g., post-WWII agricultural intensification), and potential data linkage with plant species and soil data.

## What was done (data and workflow)
- Data rescue and digitization
  - Scanned primary field maps (1978) and plot data; digitized maps into a GIS at CEH Lancaster.
  - Digitization performed by ADAS in 2009 following a defined protocol; primary maps moved to secure storage.
  - Spatial data linked to Broad Habitat allocations (via conversion of 1978 field codes to Broad Habitats).
- Data architecture and storage
  - Digitized maps stored in a GIS system at CEH Lancaster; supporting datasets archived in Field Assessment Book (FAB) boxes.
  - Visual and map-based outputs prepared to relate Broad Habitats to species and soil (pH, Loss on Ignition) data collected in 1978.
- Classification framework
  - Early 1978 field codes translated to Broad Habitats (Jackson 2000) with checks against species data and vegetation plots to resolve ambiguities.
  - Data aligned with later Countryside Survey coding structures to facilitate cross-year comparisons, acknowledging that 1978 uses an earlier ITE Land Classification.

## Data checking and validation
- Quality checks
  - Initial scan-verification against original field maps to identify omissions and digitizing errors.
  - Cross-year consistency checks: each survey square for 1978, 1984, 1990, 1998, and 2007 reviewed on separate sheets; annotated maps assessed with staff involved in 1978 surveys.
  - Anonymization: survey square locations spatially manipulated to protect confidentiality.
- Outcomes
  - 1978 dataset deemed sufficiently robust and consistent with other Countryside Survey datasets to support direct comparisons in future work.
  - Visual comparisons across years demonstrated credible attribution of changes to real landscape modification rather than recording bias.

## Broad Habitat allocations
- Mapping decisions
  - Most 1978 field codes mapped straightforwardly to Broad Habitats (e.g., Conifer Woodland to Coniferous Woodland).
  - Some codes were ambiguous (e.g., Mixed Upland Moor could be Bog, Dwarf Shrub Heath, or Acid Grassland); decisions made using habitat maps, vegetation plots, and species data.
  - Visual checks performed on every square to resolve remaining allocations.
- Notable issues and resolutions
  - Upland codes: inherently difficult in heterogeneous upland landscapes; mosaic or patch-like approaches may be needed in future updates.
  - Calcareous Grassland and other grassland types required cross-checks to avoid misclassification due to similar codes in 1978.
  - Inland Rock tended to be overestimated in 1978 due to mapping method differences (primary vs secondary coding in later years).
  - Some 1978 to 1990 mappings differed due to shifts in classification definitions; cross-year harmonization was applied where feasible.

## Note Regarding the ITE Land Classifications
- Classification lineage
  - 1978 used the original ITE Land Classification based on a 15x15 km grid and ISA-derived classifications (6039 classified squares for national estimates; 256 survey squares in 1978).
  - 1990 onward: revised “All Squares” Land Classification with broader class differentiation (32 classes in 1990, expanding to 40 in 1998, 45 in 2007) to improve national estimates and Scottish/Welsh reporting.
- Rationale and impact
  - National estimates for 1978 are calculated with the 1990 Land Classification (where feasible) because 256 core survey squares insufficiently populate all 32 classes from the 1978 framework.
  - Direct comparability between 1978 results and later years is limited due to classification changes and retrospective re-allocations.
- Documentation
  - Appendix III provides a summary of how land classifications evolved, including flowcharts and cross-references to relevant literature.

## Results: National Estimates of Broad Habitat Stock 1978
- Scope and caveats
  - National stock estimates are presented for selected Broad Habitats, with explicit cautions about comparability to 1984, 1990, 1998, and 2007 results.
  - 1978 results use the 1990 Land Classification for consistency in analysis; direct year-to-year comparisons require careful methodological alignment.
- Representative figures (means in '000s hectares)
  - Arable and Horticulture: ~5105 (21.9% of GB)
  - Improved Grassland: ~5188 (22.3%)
  - Neutral Grassland: ~1442 (6.2%)
  - Coniferous Woodland: ~1413 (6.1%)
  - Broadleaved, Mixed and Yew Woodland: ~995 (4.3%)
  - Dwarf Shrub Heath: ~1677 (7.2%)
  - Bog: ~2004 (8.6%)
  - Fen, Marsh and Swamp: ~231 (1.0%)
  - Bracken: ~258 (1.1%)
  - Urban and related categories: substantial components (e.g., Urban ~1441; Unsurveyed Urban ~482)
  - Other categories and detailed breakdowns provided in the report’s table (not reproduced here in full)
- Interpretive note
  - These are not directly comparable to 2007 figures; 1978 estimates reflect older classification and sampling frameworks, and retroactive allocations may shift totals.

## 8.1 Comparison of New Results with Previously Published Data
- Key differences explained
  - Differences arise from non-direct comparability of Broad Habitat reporting classes across publications and the impact of using different Land Classifications (1978 vs 1990/All Squares vs revisions in 1998/2007).
  - Some 1978 areas were edited during harmonization to reflect the later data pools and to minimize apparent change where not supported by species data.
  - The new results align more closely with Barr et al. (1993) due to using the revised All Squares Land Classification rather than the original 1984 Bunce & Heal (1984) framework.
- Example habitat notes
  - Boundary and Linear Features: newer estimates are generally lower than Bunce & Heal (1984) due to changes in classification that reduce small habitat overestimation.
  - Arable and Horticulture: new mean is higher than earlier estimates; reflects Land Classification differences and reallocation.
  - Acid Grassland, Dwarf Shrub Heath, Fen, Marsh and Swamp, Bog: difficult to compare due to shifting definitions and lack of consistent reporting classes across publications.
  - Urban: earlier figures included unsurveyed urban land; later classification treats unsurveyed urban differently, impacting comparisons.
- Overall takeaway
  - Many discrepancies stem from methodological evolution rather than data errors; users should apply the same classification framework when comparing across years.

## 8.1.1 Notes regarding Specific Habitats
- Highlights of potential over- or under-estimation
  - Boundary and Linear Features: overestimation in some older sources due to 1978 Land Classification biases.
  - Fen, Marsh and Swamp: definition ambiguity in 1978; the closest phenology may capture some grassland areas, inflating or deflating estimates.
  - Urban and Unsurveyed Urban: changes in treatment across years affect comparability; unsurveyed urban was treated as a constant in later classifications.
- Implications for interpretation
  - Caution required when interpreting trends for habitats with shifting definitions or limited sampling in 1978.
  - When constructing time-series analyses, maintain consistent classification schemes or apply harmonization adjustments as described.

## Appendices and supplementary information (highlights)
- Appendix II: Habitat Code Lookup Table
  - Provides mappings from 1978 descriptions to Broad Habitat allocations (e.g., various grassland prevails mapped to Improved Grassland or Neutral Grassland; several plant associations linked to Dwarf Shrub Heath, Calcareous Grassland, etc.).
  - Includes crosswalk notes for ambiguous allocations and guidance on when to use species data for allocation decisions.
- Appendix III: Summary of the ITE Land Classification evolution
  - Traces the transition from the 1978 ITE Land Classification to the 1990 All Squares scheme and subsequent refinements (40–45 classes) for 1990, 1998, and 2007.
  - Describes flow of sampling and reclassification procedures across surveys and how national estimates were derived.
- Map outputs and data accessibility
  - Maps illustrating Broad Habitat stock as percentages by Land Class are included in the appendices.
  - Data and code lists are aligned to support reproducibility and cross-year integration for future monitoring analyses.

## Implications for Analysts Monitoring the Environment
- Enables long-term environmental health assessment by extending habitat stock data back to 1978.
- Provides a standardized, auditable workflow for digitizing historic maps and translating field codes into comparable Broad Habitat categories.
- Supports mixed-data analyses (habitat stocks, plant species, soil properties) for climate, policy, and land-use impact studies.
- Highlights the need for consistent classification schemes when building multi-decadal monitoring datasets; clarifies how to handle ambiguous codes and upland mosaics.
- Emphasizes data accessibility and transparency to allow broader use of historical habitat data for policy evaluation and environmental health scrutiny over time.