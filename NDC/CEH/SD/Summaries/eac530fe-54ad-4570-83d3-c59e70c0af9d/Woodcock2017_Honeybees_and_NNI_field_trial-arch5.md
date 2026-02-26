# Data describing population responses of honeybees to oilseed rape neonicotinoid seed treatments in Hungary, Germany and the UK.

## Overview
- International, field-based study across 33 commercial sites in the UK, Hungary, and Germany (2014–2016) examining the effects of neonicotinoid seed treatments on honeybees (Apis mellifera) for oilseed rape crops.
- Treatments: clothianidin (CTD), thiamethoxam (TMX), and a fungicide-only control.
- Data extend the associated Science paper by Woodcock et al. (2017) by including individual hive level information.
- Focus on population-level endpoints (EFSA primary and secondary metrics) and multiple exposure pathways (crop residues in pollen/nectar, crop expression, and landscape context).
- Three linked data files with rich metadata and multiple derived metrics, suitable for data discovery, reuse, and governance.

## Data structure and content
- apis_median.csv
  - Site-level medians (based on six hives per site) describing honeybee population responses during oilseed rape flowering, and after overwintering.
  - Includes landscape context, neonicotinoid residue metrics, and a combined neonicotinoid index (NNI) corrected by LD50.
  - Metadata fields cover country, site, block, treatment, sampling dates, hive counts, colony weights, brood stages, nectar/pollen storage, and disease metrics.
- apis_allhives.csv
  - Hive-level data across all 33 sites; six hives per site, with per-hive population metrics, weights, brood stages, and exposure durations.
  - Detailed breakdown of pre-exposure, exposure, and post-exposure measurements.
  - Includes hive-level pollen grain analyses, nosema, varroa infestation, and overwintering performance.
- apis_tent.csv
  - Neonicotinoid residue expression data collected by tenting honeybee colonies over the OSR crop.
  - Site-, hive-, and treatment-level measurements for clothianidin, thiamethoxam, and imidacloprid in nectar and pollen gathered by forced foraging.
  - Includes tunnel-level metrics (max/median), events (samples above/below LOQ), and exposure counts.
- Additional residue and exposure datasets (references to methods and protocols) underpin the exposure assessments and analytical approach (LC-MS/MS with specified LOQ/LOD).

## Methods and study design (key elements for data stewardship)
- Experimental design: 33 commercial OSR sites grouped into blocks; three treatments randomized within blocks across the three countries.
- Honeybee deployment: Six hives per site, centralized to the crop area; post-flowering hives moved to overwintering sites with country-specific feeding and Varroa management.
- Endpoints and timing:
  - EFSA primary endpoints: colony strength and overwintering success.
  - Secondary endpoints: broader colony health metrics across development stages, foraging resources, and colony weight dynamics.
  - Sampling during flowering (April–June 2015) at 4–7 day intervals; one centralized overwintering assessment date per country (March 2016).
- Residue and exposure measures:
  - Pollen and nectar residue analysis for clothianidin, thiamethoxam, and imidacloprid (with specified LOQ/LOD and quantification approach).
  - Neonicotinoid expression in the crop assessed via cage-based honeybee vectoring to sample pollen/nectar; caveats include potential crop depletion due to heavy sampling.
  - Additional covariates: Nosema, Varroa, DWV, disease load, and general foraging plant diversity (pollen grain analyses).
- Landscape context: 1.5 km radius around hives categorized into land-use classes (OSR, crops, grassland, woodland, water, urban, etc.).
- Data quality controls:
  - Median hive values used per site to mitigate within-site non-independence and drift between hives.
  - Pre-exposure covariates and post-exposure assessments included to contextualize results.
- Documentation and provenance:
  - Detailed methods and references for sampling, residue analysis, and statistical considerations provided (including links to technical protocols and EFSA references).

## Data governance, provenance, and stewardship considerations
- Data stewardship focus: ensure datasets are discoverable, accurately described, and up-to-date; align with data governance practices for large dataset collections.
- Metadata richness supports data discovery, interoperability, and reuse across researchers and institutions.
- Funding and potential conflicts: study funded by Syngenta Ltd. and Bayer CropScience; metadata and provenance should be clearly captured to support transparency and governance.
- Reuse potential: enables cross-study comparisons of country- and site-specific effects, assessment of combined neonicotinoid exposure indices, and integration with landscape-scale analyses.

## Variable scope and data quality notes (highlights relevant to data stewards)
- Population endpoints: multiple hive- and site-level metrics capturing colony strength, brood staging, adult bee counts, and overwintering outcomes.
- Exposure metrics: concentrations of CTD, TMX, and IMI in nectar and pollen (various sampling routes including stored combs, free-flying bees, and pollen traps), with derived metrics such as medians, peaks, and combined Neonicotinoid Index (corrected for LD50).
- Pollen analyses: pollen grain identification and diversity metrics (breadth of foraging, OSR pollen abundance, and tree/flower taxon counts).
- Disease and parasite covariates: Nosema spore loads, Varroa infestation rates, and DWV considerations included as covariates.
- Temporal structure: measurements across pre-exposure, exposure, and post-exposure periods with multiple sampling rounds; overwintering assessments conducted on a single date per country.
- Data limitations: in situ depletion of crop pollen/nectar reduced the number of samples; residue measurements include LOQ/LOD handling (values below LOQ treated as LOQ/2 as appropriate); model interpretations should account for potential site-level heterogeneity and cross-country differences.

## Practical guidance for data users and cataloguing
- Primary data assets to catalogue:
  - apis_median.csv: site-level medians, landscape context, residue metrics, and derived indices.
  - apis_allhives.csv: per-hive observations with rich covariates and longitudinal sampling.
  - apis_tent.csv: residue expressions from tented crop exposure experiments.
- Metadata considerations:
  - Capture country, site, block, treatment, sampling dates, hive counts, and measurement units.
  - Document LOQ/LOD treatment, residue calculation methods, and the LD50-based NNIndex derivation.
  - Include disease covariates and landscape metrics to support covariate-adjusted analyses.
- Data reuse potential:
  - Cross-country comparisons of neonicotinoid exposure and colony outcomes.
  - Assessing the relationship between crop-level neonicotinoid expression and colony health metrics.
  - Integration with landscape structure and foraging diversity data for ecological risk assessments.
- Sharing and publishing: dataset aligns with publishing practices in data portals and catalogues; ensure proper attribution to original authors and funding disclosures; link to the associated methodological references for reproducibility.

## Key takeaways for Data Stewards
- This collection provides comprehensive, multi-level data on honeybee responses to three neonicotinoid seed treatments across three European countries, including detailed hive-level measurements, colony health endpoints, residue analyses, disease covariates, and landscape context.
- Three linked data files (apis_median.csv, apis_allhives.csv, apis_tent.csv) together enable site-level, hive-level, and crop-exposure analyses, with rich metadata and standardized units.
- The data support transparent governance and reproducibility, with explicit methods for sampling, residue analysis, and derivation of combined toxicity indices; however, some sampling constraints (crop depletion, LOQ handling) and funding disclosures should be carefully documented in data governance records.
- For data discovery and reuse, ensure comprehensive metadata capture (sampling dates, treatments, landscape context, disease covariates, residue metrics, and LD50-corrected indices) and note any data gaps or deviations from planned sampling.