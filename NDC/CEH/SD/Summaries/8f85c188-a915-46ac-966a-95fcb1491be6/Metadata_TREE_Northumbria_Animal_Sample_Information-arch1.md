# TREE_Northumbria_Animal_Sample_information

## Overview
- Metadata schema for Northumbria animal samples, detailing species information, sampling context, morphometrics, mass measurements, counts, sex, and notes.
- Designed to support data-driven analyses of correlations, distributions, and potential predictions about biological samples and their origins.
- Includes fields for specimen identifiers, sampling location (grid reference), and preparation/analysis details.

## Key fields and data types

- Latin_Species_Name
  - Meaning: Latin taxonomic name of species
  - Units: n/a
  - Explanation: Scientific name
- Common_Species_Name
  - Meaning: Common name of species
  - Units: n/a
  - Explanation: Vernacular name
- Site
  - Meaning: Sampling site identifier
  - Units: n/a
  - Explanation: Location name or code
- Date_Sample_Collected
  - Meaning: Date the sample was collected
  - Units: n/a
  - Explanation: Collection date
- Sampling_Location_Or_National_Grid_Reference
  - Meaning: Precise sampling location
  - Units: n/a
  - Explanation: National Grid Reference
- CEH_Sample_Codes_Associated_with_Animal_or_Sample
  - Meaning: CEH lab reference codes linked to the sample
  - Units: n/a
  - Explanation: Associated codes
- CEH_Sample_Description
  - Meaning: Description of the CEH sample
  - Units: n/a
  - Explanation: Sample description
- Length_mm
  - Meaning: Organism length
  - Units: mm
  - Explanation: Measured length; “Not recorded” if unavailable
- Width_mm
  - Meaning: Organism width
  - Units: mm
  - Explanation: Measured width; “Not recorded” if unavailable
- Depth_mm
  - Meaning: Organism depth
  - Units: mm
  - Explanation: Measured depth; “Not recorded” if unavailable
- Wholebody_Fresh_Mass_kg
  - Meaning: Fresh mass of whole organism
  - Units: kg
  - Explanation: Mass; “Not recorded” if unavailable
- Wholebody_Freeze_Dried_Mass_kg
  - Meaning: Freeze-dried mass of whole organism
  - Units: kg
  - Explanation: Mass; “Not recorded” if unavailable
- Wholebody_Ash_Mass_kg
  - Meaning: Ash mass of whole organism
  - Units: kg
  - Explanation: Mass; “Not recorded” if unavailable
- n
  - Meaning: Count of animals or samples
  - Units: n/a
  - Explanation: Number represented; “n” indicates quantity
- Sex
  - Meaning: Sex of animal
  - Units: n/a
  - Explanation: “Male” or “Female”; “Not recorded” if undetermined; “Unknown” if not specified
- General_Notes
  - Meaning: Additional contextual notes
  - Units: n/a
  - Explanation: General remarks
- Sample_Preparation_And_Analysis_Performed
  - Meaning: Information on sample prep and analyses conducted
  - Units: n/a
  - Explanation: Preparation methods and analyses performed (if any)

## Special notes and considerations

- Frogspawn note: “Frogspawn are bulk samples of multiple eggs,” indicating composite samples rather than single organisms.
- Missing data indicators: “Not recorded” (measurement missing) and “Unknown” (unknown sex) are used for data gaps and should be treated accordingly in analyses.
- Location data: National Grid Reference enables spatial analyses and mapping of sampling effort and species distributions.
- Data provenance: CEH sample codes and descriptions provide traceability to laboratory workflows and analyses.

## Data quality and usage for analysis

- Ideal uses:
  - Correlate morphometrics (Length_mm, Width_mm, Depth_mm) with species (Latin_Species_Name, Common_Species_Name) and site.
  - Explore mass relationships (Fresh mass, Freeze-dried mass, Ash mass) across species and sites.
  - Analyze counts (n) by site, date, and sex distribution where data exist.
  - Map sampling effort and distribution using grid references.
  - Review sample preparation and analysis details to assess comparability across samples.
- Potential challenges:
  - Missing measurements flagged as Not recorded; plan for imputation or exclusion as appropriate.
  - Sex data may be Not recorded or Unknown, limiting sex-based analyses.
  - Bulk frogspawn samples require careful interpretation when estimating individual-level metrics.
  - Data may be linked to multiple CEH codes; ensure proper linkage during integration.

## Data collection and integration tips

- Harmonize units where combining multiple datasets (e.g., ensure Length_mm, Width_mm, Depth_mm are consistently in millimetres; masses in kilograms).
- Use National Grid Reference to align spatial analyses and cross-reference with site-level metadata.
- Track and preserve CEH_Sample_Codes_Associated_with_Animal_or_Sample to maintain data lineage through analyses and reporting.
- Document any deviations or notes from Sample_Preparation_And_Analysis_Performed to contextualize results.