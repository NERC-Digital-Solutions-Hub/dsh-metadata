# Risk analysis for Phytophthora infection ( P. ramorum and P. kernoviae ) Core Native Woodland fragments across Scotland April  2013

## Purpose and scope
- Updated risk analysis for Phytophthora infection in core native woodlands across Scotland.
- Incorporates new infection sites in larch woodlands and garden/trade premises; uses a climate suitability model to estimate transmission risk per pathogen (P. ramorum and P. kernoviae).
- Produces pathogen-specific risk maps highlighting climate and host-driven risk at national scale.
- Identifies regions distant from known infections for targeted surveillance; climate suitability for Pr is higher than for Pk overall.

## Data and factors considered
- Core Native Woodland fragments: 79,269 across Scotland.
- Risk factors included:
  - Habitat suitability for Rhododendron ponticum (invasive reservoir host).
  - Abundance/cover of Vaccinium myrtillus (host).
  - Climatic suitability for growth and sporulation (species/strain specific thresholds for Pr and Pk).
  - Proximity to garden/trade premises and infected premises.
  - Proximity to larch and infected larch woodlands.
  - Proximity to roads and rivers within a fragment.
- Scotland-wide maps of all factors not provided due to data access restrictions.

## Proximity and infection data inputs
- Premises infections: 2011–2013 data from SASA and FC Scotland; updated to May 2013.
- Infected larch locations: combined 2013 data.
- GIS datasets used for risk scoring include rivers, roads, and larch infection data.

## Risk scoring framework
- Two pathogen-specific risk scores per fragment:
  - Pr (P. ramorum): maximum 17 points.
  - Pk (P. kernoviae): maximum 16 points.
- Final risk scores computed as sums of components:
  - Premises proximity (within 1.5 km, within 250 m, infected premises within 100 m).
  - Larch-related risk (no infection within 500 m, infection within 5 km, infection within 500 m).
  - Rhododendron ponticum habitat suitability (unsuitable to highly suitable).
  - Vaccinium myrtillus habitat suitability/abundance (absent to high abundance).
  - Climatic suitability (specific to Pr or Pk with distinct thresholds).
  - Water courses and roads present (score increments).
- Missing data handling:
  - Missing climate or VM habitat data flagged; final risk scores adjusted by the maximum possible score given available risk factors.
  - Visual missing-data indicators provided (red for climate, blue for VM).

## Outputs and data products
- Two formats provided for use in analyses:
  - FHN_2013.csv: risk scores only (per fragment).
  - FHN_2013.shp: ArcGIS shapefile with full risk calculation fields and original inputs; suitable for detailed inspection.
- Linkage between formats via fragment ID field.
- Key fields for risk interpretation:
  - adj_risk_p: Pr risk score adjusted for maximum possible score given available data.
  - adj_risk_1: Pk risk score adjusted similarly.
  - Avail_pr: maximum possible Pr score given available risk factors.
  - Avail_pk: maximum possible Pk score given available risk factors.
  - Uncert_pr / Uncert_pk: data uncertainty metrics (0 for complete data; increases with gaps).
  - missing_type: indicates which factors are missing (clim=climate, host=VM, both, none).

## Climate and host risk findings
- Risk concentration:
  - For both pathogens: higher risk in the south and west of Scotland, aligning with current infection sites and larch presence.
  - Pk shows substantial risk in areas distant from known infections due to climate and host suitability.
- Species-specific climate insights:
  - Pr climate suitability far more favorable; many areas score higher for Pr than for Pk.
  - Pk climate suitability is generally low (median days suitable around 17.6; mean ~17.5 with SD ~4.4) versus Pr (median ~117.2; mean ~118.4 with SD ~33.9).
  - Some northeast regions show notable Pk risk due to host presence and climate factors, despite lower overall suitability for Pk.
- Hotspot regions (examples):
  - Pr: Argyll & Bute, Ayrshire, Dumfries & Galloway; also notable risk in south-west and near major population belts.
  - Pk: south and west regions, plus clusters in central highlands, Perthshire, north highlands, and some northeast zones.

## Appendix: methodological highlights
- V. myrtillus modeling (abundance):
  - Addressed data overdispersion and interval-censored DOMIN class data.
  - Used a two-phase GLMM within a Bayesian framework:
    - Phase 1: presence/absence (binary) model with site and quadrat random effects.
    - Phase 2: abundance (percent cover) model for sites where present, using a logit-normal model with site and quadrat random effects.
  - Latent variable approach accounts for interval-censored DOMIN data.
- R. ponticum habitat modeling:
  - Maxent models using 11 datasets (designed to predict foliar reservoir habitat).
  - Predictive performance: training and test AUC ≈ 0.838.
- Risk factor scoring details:
  - Table 1 provides the weighting scheme for each risk factor category (premises proximity, larch presence, host habitat suitability, climate suitability, water, roads).
  - Final scores reflect relative, not absolute, species-specific risk due to differing climate suitability.

## Visualization and interpretation
- Figures (described but not reproduced here) map:
  - Overall risk scores across Scotland (low to high risk).
  - Current premises and larch infection coverage overlaid on risk maps.
  - Species-specific risk maps for Pr and Pk, including regional variations.
- Uncertainty and data gaps:
  - Fig. 4–5 indicate where climate or VM data are missing, influencing confidence in local risk scores.
  - Risk estimates explicitly include data availability and uncertainty adjustments.

## Practical implications for data support and surveillance
- The framework integrates diverse data sources into a coherent, species-specific risk scoring system suitable for prioritizing surveillance and resource allocation.
- Outputs deliver actionable data products (score tables and GIS shapefiles) for local and regional decision-making, with explicit handling of data gaps.
- Emphasizes the influence of climate and host distribution on spreading risk at national scale, guiding targeted monitoring in high-risk zones, including regions distant from current infections.