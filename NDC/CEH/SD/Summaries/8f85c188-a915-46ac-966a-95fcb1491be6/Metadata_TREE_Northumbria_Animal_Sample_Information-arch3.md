# TREE_Northumbria_Animal_Sample_information

## Overview
- A dataset schema for animal sampling information used in environmental health monitoring.
- Designed to support scrutiny of policies, evaluation, and informing future decisions.
- Focuses on metadata, specimen measurements, and sample processing details to enable transparent reporting and data reuse.

## Data Schema: Key Fields and Meanings
- Latin_Species_Name: Scientific (Latin) name of the species.
- Common_Species_Name: Common name of the species.
- Site: Sampling site.
- Date_Sample_Collected: Date when the sample was collected.
- Sampling_Location_Or_National_Grid_Reference: Location reference for the sampling site (e.g., grid reference).
- CEH_Sample_Codes_Associated_with_Animal_or_Sample: Codes associated with the animal or sample.
- CEH_Sample_Description: Description of the CEH sample.
- Length_mm: Length of the organism in millimetres.
- Width_mm: Width of the organism in millimetres.
- Depth_mm: Depth of the organism in millimetres.
- Wholebody_Fresh_Mass_kg: Fresh mass of the whole body (kilograms).
- Wholebody_Freeze_Dried_Mass_kg: Freeze-dried mass of the whole body (kilograms).
- Wholebody_Ash_Mass_kg: Ash mass of the whole body (kilograms).
- n: Number of animals or samples.
- Sex: Sex of the animal (male/female); “Unknown” if not determined.
- General_Notes: Any general notes about the sample.
- Sample_Preparation_And_Analysis_Performed: Information on sample preparation and analyses performed.

## Data Quality and Governance Implications
- Data completeness: Fields may be “Not recorded,” indicating gaps that limit comparability or trend analysis.
- Metadata availability: Adequate metadata is essential to verify suitability and reuse; incomplete metadata is a barrier.
- Data provenance: Clear linkage to originators and datasets is necessary for quality assurance and reproducibility.
- Data standardization: Consistent units (e.g., mm, kg) and standardized field naming reduce the need for costly transformations.
- Open data considerations: Some datasets or details may be sensitive or restricted when publicly shared; governance processes must address sharing appropriately.
- Data silos: Potential barriers if information is held in separate organisations; integration is required to maximise utility for monitoring frameworks.

## Use in Monitoring Frameworks
- Enables tracking of biological measurements alongside sampling metadata for environmental health assessments.
- Supports reporting through standardised fields (species, site, date, measurements, and processing methods).
- Provides a basis for dashboards and summaries that inform policy scrutiny and future decisions.

## Special Notes and Considerations
- Frogspawn: Noted as bulk samples of multiple eggs; implications for per-sample measurement and analysis.
- Measurement scope: Includes morphological (Length, Width, Depth) and mass metrics (fresh, freeze-dried, ash) to support diverse analyses.
- Data interpretation: “Not recorded” and “Unknown” markers require careful handling during analysis and reporting to avoid misinterpretation.