# FIELD HANDBOOK Freshwater , Version 2013.02

## Objective and scope
- Documentation for the Glastir Monitoring & Evaluation Programme (GMEP) freshwater field surveys.
- Aims to assess pond condition and ecological quality using standardized field methods and datasets.
- Data collected feed into PSYM-based biological quality assessments and are stored in structured CSV datasets.

## Sampling design and site selection
- 1 km square survey framework with stratified random sampling:
  - Proportion of squares sampled within each stratum reflects stratum size.
  - Half of sampled squares additionally targeted at Glastir priority areas.
- Exclusions: squares where more than 75% urban land or more than 90% sea (per LCM2007 and census data).
- Distribution mapped and plotted at 10 km resolution to protect data confidentiality.

## Pond survey workflow and pond selection
- Within each square, ponds are identified; one pond per square is randomly selected for the condition assessment (the SURVEY POND).
- Full pond surveys (macrophytes, macroinvertebrates, water chemistry) may extend beyond the square boundary if necessary.

## Pond definitions and boundary rules
- Axis II pond definition: standing water 25 m² to 2 ha, typically holding water for at least four months per year.
- Includes temporary ponds; outer boundary defined by the maximum winter water level.
- If a pond lies on a square boundary, only the portion inside the square is used for area measurement, but the entire pond is surveyed.

## Data collection forms and data entry
- Field data collected via tablet-based forms:
  - Pond checklist (water chemistry and macroinvertebrate data)
  - Pond attributes (pond characteristics and environmental information)
  - Pond plant survey (macrophyte data)
- Critical identifiers recorded at top of forms: square number, pond reference, survey date.
- Data entered directly into a central database; pond location details included to ensure site attribution.

## Pond measurements and methods (pond condition survey)
- Water chemistry (field measurements): conductivity, pH, turbidity.
- Water chemistry (lab analyses): SRP, total oxidisable nitrogen (TON), alkalinity (50 ml filtered samples).
- Sampling protocol emphasizes undisturbed water collection and correct labeling and units.

## Macrophyte (aquatic plant) survey
- Aims: record all wetland plant species within the outer pond boundary; estimate abundance; assess total cover and shading.
- Procedures:
  - Identify outer boundary; walk/wade accessible areas; grapnel sampling for deeper areas.
  - Identify plants to species when possible; record rare species for verification.
  - Use standardized forms (Pond Plants form sheets) with species lists aligned to The New Atlas of the British and Irish Flora.
  - Rare species verification requires careful handling; samples may be pressed, pickled, or photographed for identification.
- Data and specimens handling:
  - Specimens may be pressed or preserved; label with pond and square IDs; return to Freshwater Habitats Trust.
  - Table 2 provides recommendations for problematic groups (e.g., Callitriche, Potamogeton, Ranunculus, Charophytes).

## Sampling and data handling for macrophytes
- Quantitative data: abundance categories (dominant, abundant, frequent, occasional, rare) and percent cover for submerged, floating-leaved, and emergent groups.
- Shade assessments: percent overhang and percent of pond margin shaded to at least 1 m from shore.
- Data entry: two macro- vegetation sheets; total plant cover by group; PSYM-ready metrics.

## Macroinvertebrate survey
- Aim: maximize species list within a 3-minute netting window plus 1-minute visual search.
- Habitat-based sampling: target main pond habitats (e.g., Carex stands, shallow substrates, submerged macrophytes, inflow zones, overhangs).
- Netting protocol: 25 cm2 pond-net with 900 µm mesh; equal time across habitats; additional area searches before/after net sampling.
- Handling and preservation: samples stored in polythene bags, preserved with formalin (4% final), labeled with site details; transport in clearly labeled pots; ensure minimal cross-contamination.
- Amphibians/fish observed during sampling are recorded and released; dead specimens removed if encountered.

## Additional macroinvertebrate sampling
- Extra 1 minute field search (surface, under stones/logs) to supplement the 3-minute net sample.
- Additional species added to main sample; ideally conducted before disturbing the water.

## Data preservation and transit for macroinvertebrates
- Samples placed in labeled pots with preserved material; transit in designated storage boxes with Transport Emergency (TREM) cards.

## Field survey checklists
- Ensure pond checklist, pond attributes, aquatic plant survey, and macroinvertebrate survey are completed before dispatching samples.

## Laboratory protocols and analytical methods
- Phosphate (PO4-P): colorimetric analysis using automatic analyser with standard curves.
- Total dissolved nitrogen (TDN) and Total nitrogen (TN): combustion and chemiluminescence detection.
- Alkalinity: UKAS-accredited titration method using standardized reagents and QA standards.

## Calculation of biological quality (PSYM)
- PSYM (Predictive System for Multimetrics) combines plant and invertebrate metrics to compare observed data with a predicted undegraded state.
- Steps:
  - Gather simple environmental data (area, grid reference, geology, etc.).
  - Conduct biological surveys; process net samples.
  - PSYM compares observed metrics to predicted metrics to derive an overall integrity score.
  - Outputs a single PSYM-based quality category; supports diagnostic metrics when degradation is suspected (e.g., eutrophication, metal contamination).

## Quality assurance and governance
- Adherence to DEFRA Joint Codes of Practice (JCoPR) for scientific quality and reproducibility.
- Systematic QA of data collection, field procedures, and laboratory analyses to ensure robust results and auditability.

## Data structure and datasets
- GMEP_POND_INVERTS_2013_16.csv: pond macroinvertebrate species lists with counts per square; fields include SQ_ID, YEAR, TAXA_NAME, COUNT, location coordinates, LC.
- GMEP_POND_MACROPHYTES_2013_16.csv: macrophyte records per pond; fields include SQ_ID, SPECIES, CATEGORY, ABUNDANCE, coordinates, YEAR, LC.
- GMEP_POND_MACROPHYTES_SUMMARY_2013_16.csv: summary metrics for macrophytes (overall vegetation % cover, submerged/floating/emergent cover, pond overhang, shade, adequacy flag, IBI, PSYM).
- GMEP_POND_ENV_SURVEY_2013_16.csv: pond environmental attributes with variable descriptions and values (LC, coordinates, YEAR, VARIABLE, DESCRIPTION, VALUE).
- GMEP_POND_CHEMISTRY_2013_16.csv: chemistry data per pond (SAMPLE_DATE, DETERMINAND, VALUE, UNITS, LC, coordinates, YEAR).

## Key references and contributors
- Core references: Bunce et al. 2007 (ITE Land Classification); Howard 2002 (PSYM methodology); O'Hare et al. 2013 (FIELD HANDBOOK Freshwater); Emmett et al. 2014–2017 (GMEP reports); Freshwater Habitats Trust guidelines.
- Team and institutional involvement: UK CEH, Freshwater Habitats Trust, Welsh Government, DEFRA QA standards; field survey teams and data management personnel listed in the document.

## Implications for data analysts
- Data are multi-modal and time-bound (2013–2016) with integrated field and laboratory measurements.
- Analyses rely on standardized protocols to ensure comparability across ponds and years, enabling PSYM-based quality assessment and trend analyses.
- Data quality hinges on rigorous site attribution, boundary definitions, and consistent data entry on tablet-based forms.
- The PSYM framework provides a single, aggregate ecological quality metric but also supports breakdown by individual metrics for diagnostics.
- The dataset structure supports cross-tabulation of species, habitat types, abundance, and environmental variables, enabling correlation analyses between biotic communities and physico-chemical or land-use factors.