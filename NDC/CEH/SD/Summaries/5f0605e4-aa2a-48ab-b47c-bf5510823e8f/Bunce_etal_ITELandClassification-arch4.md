# ITE LAND CLASSIFICATION: CLASSIFICATION OF ALL SQUARES IN GB

## Executive overview
- Aim: classify every 1 km square in Great Britain into land classes, preserving the original classification details while using automated, machine-readable data to enable scalable classification.
- Challenge: replicate the trusted original ISA-based 1212-square classification while expanding to all GB squares (auto-classification imagined to save about 20 man-years).
- Rationale for automation: extensive prior use of the original classification; large pre-existing databases; need to maintain sample-based distribution for representative analyses; enable refined, scalable land classification beyond the original dataset.
- Overall approach: evaluate multiple multivariate and machine-learning techniques using a common set of evaluation criteria to determine the best method to classify all GB squares.

## Data architecture and data sources
- Data requirements: data either available from existing datasets or recordable automatically at the 1 km scale.
- Data sets used (feature groups):
  - COASTAL: coastal cliff, rock, sand, mud, shingle, tidal
  - ALTITUDE: hill behind, distance to hill, gradient, distance to valley, mean altitude, etc.
  - MAPDATA: sea, woodland, villages, roads (A, B), canals, inland water, towns, railways, rivers; grid-aligned 0.1 hectare units
  - DISTANCE: distance to south coast and to west coast
  - ISLAND: island presence/absence
  - CLIMATE: mean daily sunshine, snow days, mean January temp
  - GEOLOGY: broad rock types (Cretaceous, limestone, chalk, sandstones, etc.)
  - DRIFT: drift types (glacials, loess, river terrace, etc.)
- Data provenance and tools: map data from OS digital sources via Reader’s Digest contract with Mapdata; altitude data from MOD 100 m DTM; climate and geological data digitized onto environmental gradients; ARC/INFO used for geospatial location of features.

## Classification methodologies evaluated
- ISA/TWINSPAN baseline: replication attempts of the original ISA approach yielded differences due to data balance, recording scale, and data availability.
- Discriminant Function (DF): tested as a faster, continuous-variable alternative; initial results showed high correspondence for many classes but poor performance for certain coastal classes and regional balance.
- Logistic Regression / Discriminant Function (LR/DF): combined approach tested across multiple levels; demonstrated improved correspondence with the original classification.
- Other multivariate techniques: explored various algorithms from phytosociology; distance measures useful but geographic dispersion issues (e.g., Midlands vs. southern Scotland) limited applicability.
- Indicators and simulation ordination: used to approximate original ISA structure; offered good environmental gradient alignment but produced problematic regional allocations in some cases.
- Field sampling and dispersion metrics: assessed using cross-tabulations, environmental gradient correlations, standard errors, and dispersion maps to gauge stability and representativeness.

## Key results and conclusions
- Primary recommendation: Logistic Regression/Discriminant Function (LR/DF) should be used for GB-wide classification.
  - Why DF alone was insufficient: failed to identify southern coastal classes (7 & 8) and caused regional misdefinitions (e.g., class 25 extending into southern Britain).
  - LR/DF advantages:
    - Better alignment with proportional sampling, improving representativeness across strata.
    - Higher correspondence with the original classification relative to other methods.
    - Lower standard errors and reduced dispersion compared with the original classifications.
    - Produces tighter, more coherent class clustering; coastal classes are preserved without extensive redefinition.
  - Overall metrics: LR/DF achieved closer environmental-gradient alignment to the original than DF alone, with substantial improvements in error metrics and geographic distribution consistency.
- Additional findings:
  - The original 1212-square ISA classification, when extended with 4800 squares using indicator attributes, showed notable divergences, underscoring the value of a robust LR/DF approach.
  - Cross-tabulations and scatter plots indicated LR/DF had superior diagonal alignment and fewer outliers relative to the original classification.
  - Distribution maps and dispersion analyses supported LR/DF as the preferable method for nationwide automation.

## Outputs, maps, and ecological insights
- Output products:
  - Distribution maps of the two methods (emphasis on LR/DF) showing classification across GB.
  - Altitude means and standard errors by class, to assess geographic dispersion and class stability.
  - Environmental gradients and correlations with vegetation data, to validate ecological coherence.
  - Overlay of individual attributes and coastal features for richer interpretation.
  - Estimates of land cover for GB using 1978 baseline data as a stringent test, with LR/DF showing lower errors and coefficients of variation than the original.
- Ecological characteristics:
  - Analyses linking land-class assignments to soil properties (pH and soil pits), vegetation composition, and other ecological descriptors.
  - Comparisons indicating LR/DF maintains ecological relationships more consistently with observed vegetation gradients than the original or Discriminant-only approaches.

## Implications for data leaders
- Demonstrates a scalable path to building a nationwide, governance-ready data asset by:
  - Reusing and harmonizing diverse, large-scale datasets (coastal, altitudinal, map-derived, climatic, geological, drift-related).
  - Prioritizing reproducibility of a trusted legacy classification while enabling automated, consistent nationwide coverage.
  - Employing a rigorous, multi-criteria evaluation framework to select the most robust modelling approach.
  - Providing transparent performance metrics (correspondence to original, standard errors, gradient coherence, dispersion) to justify method choice.
- Data stewardship considerations:
  - Need for standardized data formats, metadata, and documentation to ensure discoverability and future updates.
  - Importance of maintaining the link between new automated classifications and the original 1212-square framework for continuity and user confidence.
  - Prospects for collaboration with wider data communities to refine classifications and share methodology and outputs (e.g., maps, attribute tables, and gradient analyses).

## Recommendations and next steps (summary)
- Adopt Logistic Regression combined with Discriminant Function (LR/DF) as the standard method for classifying all GB 1 km squares.
- Ensure sampling and data balance are proportional to stratum size to optimize representativeness.
- Maintain and publish output with supporting metadata: distribution maps, environmental gradients, standard errors, and ecological associations.
- Preserve alignment with the original ISA-based framework to sustain continuity with existing studies while enabling scalable updates.
- Consider extending outputs to overlays of coastal features and attribute combinations to support policy, planning, and environmental assessments.