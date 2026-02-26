# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

- Objective of QA: assess consistency and reliability of CS2000 field work across major components (plot relocation, species recording, vegetation cover, landcover mapping, change recording) to support data quality for GIS analyses.
- Scope: QA exercised on 38 of 519 squares from 1998 CS2000 survey; one quarter of each square rerecorded (234 plots across 9 plot types); comparison with CS2000 originals and with CS1990 where applicable.

## Key Aims and Methods

- Aims
  - Quantify field-recording accuracy and change statistics for CS2000.
  - Examine plot relocation efficiency and observer/bias effects.
  - Relate findings to prior CS1990 results and assess mapping change accuracy.
- QA Design
  - Plates and plots relocation assessed using original 1990 sketch maps, photos, and metal detectors where possible.
  - Plot types include quadrats, road verges, streamsides, boundaries, arable margins, hedge diversity; new plots added for CS2000 protocol.
  - Mapping and boundary features recorded at the same points as the original survey for direct comparison.

## Plot Relocation

- overall plot recovery: 86.7% of 210 plots fully relocated; ~60% were precisely relocated, ~25% approximately relocated, ~15% inadequately relocated.
- plate recovery by assessors: 69.3% (vs. 87.1% in the 1991 QA for CS1990 relocation after 12 months).
- CS2000 surveyors: about 60% accurate relocation, ~25% approximate, ~15% poor relocation.
- conclusion: eight years on, relocation is feasible but less reliable than the one-year QA; some mis-sites and mis-placements occurred (e.g., wrong boundary side, wrong side of hedge, or misidentified markers); practice of reusing plates increased future search difficulty.

## Species Concordance and Recording Accuracy

- Recording accuracy: of ~6000 records across 210 plots, ~71% confirmed by assessors; ~2% non-concordances due to management/seasonal changes; overall initial accuracy ~73%, with some shortfall attributed to plot relocation errors.
- Comparison CS2000 vs QA (across 38 squares): QA tended to yield longer species lists; mean species per plot CS2000 17.9 vs QA 20.4; CS2000 % agreement around 87.7–89% across landclasses, indicating substantial but not complete concordance.
- Observed change in species lists over time: QA increases over CS2000 similar to earlier QA vs CS1990 (about 13–14% increase); suggests consistent assessor efficiency and similar search effort across QA efforts.
- Common issues: mis-identifications (notably grasses such as Poa/Rumex/Ranunculus), overlooked species (especially mosses and some grasses), and geographic/orientation mis-matches contributing to mismatches.

## Vegetation Cover

- Overall cover comparison shows substantial agreement between surveyors and assessors, with some species showing significant differences (e.g., Holcus lanatus, Dactylis glomerata, Anthoxanthum odoratum, Elymus repens, Eriophorum vaginatum) possibly due to season or identification challenges.
- Some species exhibited notable discrepancies in cover magnitude, while others (Lolium perenne, Agrostis spp.) showed better agreement.
- Inference: cover estimates are reasonably robust but sensitive to season, plot positioning, and species familiarity.

## Change in Vegetation and Land Use

- Change analysis: DECORANA-based ordination used to assess shift in vegetation change; for most plot types, no directional bias detected in axis scores between CS2000 and QA.
- Change concordance: overall, 51.4% agreement on landuse/landcover changes between CS2000 and QA; 33.9% changes not noted by CS2000; 14.7% changes noted but not substantiated by assessors.
- Interpretation: substantial under-recording or misclassification of changes since 1990; many real changes may have been missed; changes require careful interpretation and may rely more on plot data than on field strings alone.

## Land Cover Mapping and Boundary Features

- Primary land cover codes
  - Concordance CS2000 vs QA: 88% for primary landcover codes; including BAP codes, overall primary land cover agreement 87.5%.
  - BAP codes alone: 77.4% concordance.
  - Interpretation: mapping of broad habitat categories is generally reliable, with some misclassifications between close or nested habitat types.
- Landuse and boundary changes
  - Primary boundary codes: overall concordance 92% when compared to QA; including boundary vs. feature presence/absence shows high consistency.
  - Primary boundary features (walls/hedges) and hedge shapes: boundary feature concordance around 67.5%; height and stockproofness coding show high agreement (Boundary height ~89–92% concordance; stockproof ~83–89%).
  - Boundary changes: some mismatches due to new or removed features; changes between 1990 and CS2000 often not captured consistently, suggesting need for rigorous change-coding discipline.

## Hedge Diversity and Arable Margins

- Hedge diversity: 19 samples show QA yielded somewhat higher total species counts than CS2000; hedge species concordance reasonable but observed some omissions.
- Arable plots: only five plots; concordance between CS2000 and QA was very poor, likely due to seasonality, greater difficulty identifying ruderal species, and less familiarity with arable weeds among surveyors.

## Overall Findings and Implications for GIS Data Products

- Strengths
  - High concordance for primary land cover codes and primary boundary features; robust mapping framework.
  - Strong boundary/height/stockproof coding consistency; boundary data reliable for GIS workflows.
  - General consistency in major plot types and in the ordination pattern when aggregating data across landclasses.
- Limitations
  - Plot relocation accuracy varies; eight-year displacement introduces spatial uncertainty that can affect change analyses.
  - Change recording between CS1990/CS2000 is inconsistent; many changes are missed or not substantiated, reducing reliability for time-series analyses.
  - Arable margin and hedge datasets show greater discrepancies; hedges and hedgerows require careful verification and possibly more detailed coding.
  - Arable plots show especially low concordance, indicating seasonality and identification challenges in weed communities.
- GIS implications
  - CS2000 land cover codes and boundary codes are solid for mapping and spatial queries; use them with reasonable confidence but be wary of potential changes over time and event-driven misclassifications.
  - Change detection should rely on plot-level data and explicit change-coding; treat automated change in strings with caution.
  - Maintain or improve permanent marking and plate regression strategies to enhance future relocations and spatial integrity.
  - Consider targeted QA sampling for arable margins and hedges to improve reliability where these layers are critical.

## Annex and Data Quality Highlights

- QA included periodic plotting of efficiency and agreement by square (Annex B), revealing variability across squares and plot types.
- Primary code concordance and boundary code concordance metrics provide benchmarks for GIS data quality and codebook alignment with field practices.
- The exercise documents explicit mis-match types (mis-identifications, overruns/overlooks, orientation/location errors) to guide data cleaning and validation in GIS workflows.