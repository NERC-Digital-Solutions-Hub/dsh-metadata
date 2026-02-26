# COUNTRYSIDE SURVEY 2000 QUALITY ASSURANCE EXERCISE

- Purpose: Assess consistency and reliability of CS2000 field work across plot relocation, species recording, vegetation cover, landcover mapping, and change detection; compare with CS1990 QA; inform data quality for GIS-based data products.

## Aims and Scope
- Quantify accuracy of field recording in CS2000 and comment on change statistics.
- Examine plot relocation efficiency and observer bias.
- Explain recording differences due to plot location, management, season, and plot type.
- Relate findings to CS1990 performance; assess landuse mapping accuracy and change recording.

## Methods and QA Design
- Sample: 38 of 519 squares from 1998; in each, one quarter resurveyed (234 species plots across nine plot types).
- Plots and squares: 234 plots across 38 squares; seven main CS2000 plot types (quadrats and linear plots); 210 plots aligned to QA assessment.
- Plate/plot relocation: Locate buried plates and original plot positions; evaluate relocation success and distance from original.
- Data types assessed: species presence/absence, percentage cover, landcover codes (primary, secondary, and cover codes), hedge/boundary features, landuse changes.
- Analysis: Concordance between CS2000 and QA; DECORANA ordination for change direction; various tables and figures summarizing agreement, errors, and changes.

## Key Findings

### Plot Relocation and Location
- Relocation success: 86.7% of 210 plots satisfactorily relocated; 60% accurately relocated (plate and plot), ~25% approx relocated, ~15% inadequately relocated.
- Difficulty by plot type: Y-plots most challenging (23% failure).
- Eight-year relocation feasibility: comparable to 12-month relocation, indicating markers and plots can be relocated after eight years, but accuracy varies.
- Overall implication: reasonable relocations but notable room for improvement in precise positioning to support GIS analyses.

### Species Concordance and Recording Accuracy
- Concordance: ~71% of species records confirmed; ~2% non-concordances due to management or seasonal changes.
- Initial accuracy: ~73% (CS2000 vs QA) with ~5% non-concordance attributable to plot relocation errors; when contextual differences are accounted for, efficiency parallels CS1990.
- Assessment of mis-matches: detailed breakdown shows most discrepancies tied to plot location/orientation and recording errors rather than systematic observer bias.

### Estimates of Vegetation Cover
- Broad agreement: QA cover estimates generally aligned with CS2000, but six of the top 30 frequent species showed significantly different cover levels between surveyors and assessors (some due to season).
- Overall cover agreement: about 74% across principal species; some notable species differences include Holcus lanatus, Dactylis glomerata, Anthoxanthum odoratum, Elymus repens, Anthriscus sylvestris, and Eriophorum vaginatum.
- Seasonal and plot-location effects contribute to cover discrepancies.

### Direction of Vegetation Change
- DECORANA analysis: overall axis shift between original survey and QA was not significant; no directional bias detected when partitioned by plot type or landclass.
- Interpretation: changes observed are not driven by systematic bias, but rather by recording and location/orientation factors and natural variation.

### Landcover Mapping and Coding
- Code-group concordance (CS2000 vs QA):
  - Primary landcover codes: 88% agreement
  - BAP codes: 77%
  - Primary boundary codes: 85%
  - Principal qualifying landcover codes: 73%
  - Species awarded cover: 63%
  - Species cover codes: 74%
- Overall primary landcover agreement: 87.5% (excluding BAP), 91.6% if BAP codes are excluded from the concordance calculation.
- Notable mapping issues: occasional misclassifications (e.g., Lolium-rich pasture vs. acid grassland); small sample sizes can exaggerate disparities.
- BAP coding: relatively easier to assign; still some misclassifications in boundary/wet/dry classifications due to boundary delineation.

### Change Recording and Change Concurrence
- Change concurrence: 51.4% overall; 33.9% of changes were not noted by CS2000; 14.7% recorded but not substantiated by assessors.
- Implication: a substantial portion of changes since 1990 may be missed by the CS2000 coding; the survey data may be less reliable for change detection without QA verification.
- Example issues: miscodings or omissions in 1990 strings; some change additions by surveyors not supported by QA.

### Boundary Features, Hedge Boundaries, and Wall Conditions
- Primary boundary features: high concordance; total boundary concordance ~85% with code concordance ~92%.
- Hedge/wall condition: moderate concordance (67.5%); boundary height: high concordance (~89.2% overall); stockproof status: ~83.8%.
- Issues: new hedge codes (374–380) had limited success; some codes omitted or misapplied; occasional mis-match between wall condition codes.

### Hedge Diversity and Arable Plots
- Hedge diversity: 19 hedge samples; total species 124; common species 92; overall concordance ~74.2% (surveyors vs assessors), with surveyor efficiency ~77.4%.
- Arable margins: only five plots; very low concordance (approx. 30.6%), attributed to seasonality and less familiarity with ruderal species; recommendation for two visits to improve reliability.

### Species Frequency and Change Across Plots
- Frequency comparisons indicate general similarity in ranking between CS2000 and QA, but with notable discrepancies for some common grasses and forbs.
- Some species more prone to recording differences due to season, misidentification within Poa/Agrostis groups, mosses, and other taxa.
- Overall trend: frequency data show that some mis-matches balance out across plots, but significant differences remain for certain taxa.

## Overall Interpretation for GIS Applications

- Data reliability: Landcover mapping and boundary coding are generally reliable for GIS use, with high concordance for primary codes and boundaries. BAP codes and fine-grained cover codes have lower but still acceptable agreement and should be used with awareness of specific uncertainties.
- Spatial accuracy: Plot relocation and precise placement are decent but not perfect; eight-year relocation demonstrates feasibility but suggests caution when linking historical points to current maps. Ensure metadata captures relocation confidence and plate/marker status.
- Change detection: Change data between 1990 and 1998 show substantial uncertainty; use QA-verified change strings if using CS2000 change for GIS time-series analyses.
- Data integration: When merging CS2000 with QA data, be mindful of known areas with higher disagreement (e.g., hedge boundaries, arable margins, certain grass taxa, and cover estimates). Consider separate QA flags or confidence levels for specific layers.
- Recommendations for GIS workflows:
  - Use QA-derived concordance indicators to weight or qualify map features (e.g., higher confidence for primary landcover codes, boundaries; lower confidence for hedges and arable margins).
  - Maintain permanent markers and robust plate/plot location records to support future re-surveys and longitudinal GIS analyses.
  - Incorporate seasonality considerations when interpreting vegetation cover and change in arable margins; plan multiple field visits forMarginal plots.
  - Provide clear metadata on plot types, boundary features, and coding schemes (primary/secondary/cover) to support reproducibility and cross-survey comparisons.

## Endnotes and Annex Highlights

- Annex B outlines survey dates and efficiency metrics by square; Annex A describes QA protocol and plot-type sampling; Annex C documents code systems for landcover and boundaries.
- The QA framework demonstrates robust data integrity where coding and location accuracy are solid, while identifying key areas for improvement to strengthen GIS-ready data products (notably plot relocation precision, change detection reliability, and hedge boundary coding).