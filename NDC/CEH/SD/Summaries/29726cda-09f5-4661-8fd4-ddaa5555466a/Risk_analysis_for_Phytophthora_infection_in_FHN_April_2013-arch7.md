# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) Core Native Woodland fragments across Scotland April 2013

- This study updates a prior assessment with new infection sites in larch woodlands and garden/trade premises, using a climate suitability model to estimate climatically-driven risk for P. ramorum and P. kernoviae at a core native woodland fragment level across Scotland.
- Key outcome: pathogen-specific risk maps and scores showing where risk is highest, with climate and host presence driving spatial patterns. Risk is generally higher in the south and west, but P. kernoviae also shows notable risk distant from known infections, including parts of the north and east.

## Data scope and study area

- Core Native Woodland fragments analyzed: 79,269 fragments across Scotland.
- New infection data incorporated from Forest Commission Scotland (FC Scotland) and SASA, up to May 2013.
- Outputs focus on relative (not absolute) risk across space, with separate assessments for P. ramorum and P. kernoviae.

## Risk factors and data sources

- Factors used to calculate risk scores (for each fragment):
  - Proximity to premises and infected premises (garden/trade outbreak data and current infections).
  - Proximity to infected larch stands.
  - Habitat suitability for Rhododendron ponticum (reservoir host).
  - Habitat suitability/abundance for Vaccinium myrtillus (host plant abundance proxy).
  - Climatic suitability for pathogen growth and sporulation (species-specific thresholds for Pr and Pk).
  - Landscape features: presence of rivers and roads within the fragment.
- Data sources and partners:
  - Premises infection data (2011–2013) from SASA and FC Scotland; larch infection data from FC Scotland.
  - Rhododendron ponticum habitat modelling; Vaccinium myrtillus data from Scottish Natural Heritage surveys.
  - Roads and rivers datasets; climate and environmental covariates from available national data layers.
- Data handling: Missing data addressed by indicating missing risk factors and adjusting the final score to reflect maximum possible risk given available data; maps include missing-data notes.

## Host species modelling

- Rhododendron ponticum (R. ponticum)
  - Modelling method: Maxent habitat suitability modelling using 11 datasets (landscape, soil, climate).
  - Output: binary habitat suitability and associated uncertainty; continuous suitability maps used as risk factors.
  - Key finding: broadleaved woodland, low elevation, and moderate soil moisture favor R. ponticum presence.
  - Predicted suitable habitat covers significant parts of Scotland (approx. 24% of 1 km grid cells).
- Vaccinium myrtillus (V. myrtillus)
  - Data: 335 NVC woodland surveys; 89 sites with non-zero presence.
  - Abundance measure: DOMIN scale (1–10) converted to probability/cover models.
  - Modelling approach: two-phase GLMM within a Bayesian framework to handle presence/absence (binomial) and, conditional on presence, percent cover (logit-normal). Accounted for interval-censored DOMIN data and site/quadrat random effects.
  - Resolution: predictions at 1 km.
  - Results: abundance linked to climate (temp, precipitation), soil pH, carbon/water content, elevation, bracken, and grazing; west coast hotspots (e.g., Argyll and Bute) predicted for higher abundance.

## Climate suitability vs. pathogen risk scoring

- Climate suitability is species-specific:
  - Pr (P. ramorum) enjoys higher climatic suitability in Scotland; typical Pr-friendly conditions yield 50–200+ suitable days per year in many areas.
  - Pk (P. kernoviae) generally has far fewer suitable days (<30 days/year average, median ~17.6).
- Because of species-specific climate responses, climate scores are not directly comparable between Pr and Pk; separate climate scoring is used for each pathogen to reflect spatial variation in climate suitability.

## Scoring framework and outputs

- Core native woodland risk framework assigns scores to risk factors; maximum scores differ by pathogen:
  - Pr risk: up to 17 points.
  - Pk risk: up to 16 points.
- Risk factor scoring (highlights from Table 1):
  - Premises proximity (within 1.5 km, 250 m, or within 100 m of infected premises) yields escalating scores.
  - Larch proximity: risk increases if larch is within 500 m, or infected within 5 km (larger weight for closer proximity).
  - R. ponticum habitat suitability: presence of suitable habitat increases risk (higher score for higher suitability).
  - Vaccinium myrtillus habitat suitability/abundance: absence yields low score; higher predicted DOMIN classes yield higher scores.
  - Climatic suitability: Pr scored by thresholds of days suitable (<100, 100–150, 150–200, >200); Pk scored by thresholds (<17.5 days; >17.5 days with a separate 2-point category).
  - Water courses and roads: presence adds small increments to risk.
- Outputs provided in two data formats:
  - FHN_2013.csv: risk scores only (per fragment).
  - FHN_2013.shp: ArcGIS shapefile with full risk calculation details (large and comprehensive).
- Linkage: ID field serves as the key to connect the CSV and shapefile records.
- Key risk fields to use:
  - adj_risk_p: adjusted Pr risk score for a fragment (recommended for comparing Pr risk across fragments).
  - adj_risk_1: adjusted Pk risk score for a fragment (recommended for comparing Pk risk across fragments).

## Results: spatial distribution and interpretation

- Overall pattern:
  - For both pathogens, higher risk concentrates in the southern and western parts of Scotland (consistent with current infection sites).
  - P. kernoviae (Pk) shows comparatively broader risk than P. ramorum (Pr) in some eastern areas due to host and climate suitability.
- Pathogen-specific observations:
  - Pr risk also high in southern/western woodlands distant from known infections, driven by Rhododendron ponticum habitat and larch presence plus climate suitability.
  - Pk risk is notable in the south, west, and also in northeast regions where host and climate conditions align, indicating surveillance should extend beyond currently infected zones.
- Relative vs. absolute risk:
  - Maps present relative risk (not absolute probabilities) and are species-specific; differences in climate suitability between Pr and Pk mean direct cross-species risk comparisons should be interpreted cautiously.

## Outputs and delivery details

- Data layers and formats:
  - FHN_2013.csv: fragment-level risk scores and enabling fields (e.g., river length, road length, host scores, climate scores, etc.).
  - FHN_2013.shp: spatial polygon layer for Core Native Woodland with risk fields and all original inputs from FC; large and comprehensive.
- How to use:
  - Use adj_risk_p and adj_risk_1 to compare relative risk across fragments for Pr and Pk, respectively.
  - Combine with proximity and host layers (R. ponticum, V. myrtillus, larch, infection premises) to interpret drivers of risk in specific areas.
- Uncertainty and data gaps:
  - Some fragments lack climate data or VM data; these are flagged, and missing data is partially accommodated by adjusting risk scores to the maximum possible given available factors.
  - Presentations include uncertainty measures (e.g., standard deviation across model iterations for host habitat predictions).

## Appendix and methodological details (highlights)

- Detailed methodology for V. myrtillus modelling:
  - Addressed overdispersion, unequal quadrat counts, and interval-censored DOMIN data.
  - Implemented a two-phase Bayesian GLMM (presence/absence with random effects; then abundance given presence) using a latent variable approach for interval-censored data.
- Appendix tables document risk scoring rules and field mappings (CSV and shapefile fields) and the exact data-processing steps to generate the risk scores.

- Visuals referenced (Figures 6–13):
  - Maps illustrating risk scores for Pr and Pk across Scotland, including overlays of current premises and larch infections, to inform surveillance and management planning.