# Metadata for 4_Hot_Particle_Activity.csv

## Purpose and context
- Provides metadata for a dataset of hot particle activities to support consistent environmental monitoring.
- Aims to demonstrate environmental condition and enable scrutiny of environmental health and policy performance over time.
- Intended for analysts who verify, quality assure, clean, transform, and standardise data, then present findings in clear formats and ensure data are stored in appropriate portals.

## Data structure and content
- Each entry describes a hot particle with multiple descriptive and quantitative fields.
- Key descriptive fields:
  - Code (database serial number, unique ID)
  - Identifier (UIAR unique label - chemical analysis number)
  - Angle_degree (polar coordinate angle around ChNPP; 0/360° = North; sampling reference point)
  - DIST_km (distance from sampling point in polar system; notes about some coordinates and Polish samples)
  - MAXSIZE_um and MINSIZE_um (particle size range)
  - Burnup_MW_d_kg-1 (burnup category, defined from radionuclide ratios; cited sources)
  - VIEW (visual representation category; see notes)
  - COLOR, FORM (appearance descriptors)
  - STRUCT (particle structure or sampling location notes; e.g., Warsaw, Mikolajki, Lomza, etc.)
  - TYPE (Chernobyl hot particle classification: fine-dispersed fuel vs condensed particles; Polish context groups A/B/C)
  - DATE_Gamma (date of gamma measurement; format; notes)
  - DATE_Alpha, DATE_Beta (dates of alpha and beta measurements)
  - Total_alpha_activity_Bq, Activity_of_90Sr_Bq, and a wide set of isotope-specific activities (in becquerels) with related STD_of_*_Bq values (standard deviations)
  - Specific isotopes covered (examples): 95Zr, 95Nb, 106Ru, 125Sb, 134Cs, 137Cs, 144Ce, 154Eu, 155Eu, 54Mn, 60Co, 241Am, 90Sr, among others; each with activity and uncertainty fields
  - Related references for measurement interpretation and classification (e.g., gamma, alpha, beta measurements)

## Measurements and isotopes
- Gamma, alpha, and beta measurement data included:
  - DATE_Gamma, Total activity and associated standard deviation for 95Zr, 95Nb, 106Ru, 125Sb, 134Cs, 137Cs, 144Ce, 154Eu, 155Eu, 54Mn, 60Co, 241Am
  - DATE_Alpha and DATE_Beta with total alpha activity and 90Sr activity
  - Std deviations provided for many isotope activities (e.g., STD_of_95Zr_Bq, STD_of_137Cs_Bq, etc.)
- Isotope set reflects Chernobyl-origin hot particles and related measurement practices from the references cited.

## Sampling geometry and locations
- Angle_degree and DIST_km define the sampling geometry in a polar system with ChNPP as center.
- Some particles labelled with coordinates (0,0) were sampled in the Chernobyl Shelter or sarcophagus, indicating a link to the immediate Chernobyl context.
- Structure and location notes reference multiple places (Warsaw, Mikolajki, Lomza, Bialystok, Suwalki) for sample origin or classification.

## Classification, groupings, and interpretation
- Polish samples categorized into three groups:
  - Group A: Dominated by isotopes Ru-103 and Ru-106
  - Group B: Rich in Ru-103, Ru-106, Ce-141, Ce-144, Zr-95, Nb-95, Cs-134, Cs-137
  - Group C: Similar to Group B but with higher Ru abundance (intermediate between A and B)
- Burnup_MW_d_kg-1 classification derived from activity ratios of low-mobile refractory radionuclides and caesium isotopes; references Kuriny et al., Kashparov et al., Begichev et al., etc.

## Data quality, provenance, and references
- Metadata includes explicit data provenance notes (measurement dates, formats, and standardisation practices).
- References provide foundational background on hot particles, their formation, properties, and measurement approaches (e.g., Pubs from Begichev et al., Kashparov et al., Kuriny et al., Zhurba et al.).
- Date formats and measurement descriptions are specified to support reproducibility and QA.

## How this supports environmental monitoring
- Enables standardised representation of hot particle characteristics for longitudinal monitoring.
- Facilitates categorisation of environmental health risk through standardized activities across multiple isotopes and measurement dates.
- Designed to be integrated with other datasets and made accessible through appropriate data portals for broader analysis and policy scrutiny.

## Particular challenges and opportunities
- Challenge: Increasing the value of these datasets by combining with other relevant data sources beyond single-use analyses.
- Challenge: Enabling broad access to the underlying data used to create final outputs to support transparency and external scrutiny.