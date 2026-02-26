# Biota

## Overview
- A data dictionary schema for a Biota dataset, detailing species identifiers and a set of mass measurements derived from samples.
- Each field includes an Explanation (description), Units, and Notes to support consistency, discoverability, and data quality.
- Standardizes mass measurements in grams and collection dates in a uniform format to enable reliable analyses and comparisons.

## Core fields and purpose
- Biota: English name of the biota (species or organism).
- Latin_name: Latin (scientific) name of the species.
- Collection_Date: Date the sample was collected (format: dd month yyyy).
- ID: Unique identifier for the data record.
- Whole_body_g: Mass of the whole body (grams).
- Gut_g: Mass of the gut (grams).
- Tissue_with_thyroid_g: Mass of the sample containing the thyroid when the thyroid is too small to separate; analyzed as a whole (grams).
- Thyroid_g: Mass of the thyroid gland (grams).
- Liver_g: Mass of the liver (grams).
- Kidney_g: Mass of the kidney (grams).
- Carcass_g: Mass of the carcass (grams).

## Metadata, units, and data quality
- Units are specified for all mass-related fields (grams); non-mass fields have Units marked as not applicable.
- Each field provides an Explanation to clarify what is being measured or represented.
- Notes fields are available to capture special cases or methodological details; some notes are empty, indicating no additional information.

## Governance, discoverability, and reuse
- The structured metadata supports data discovery, consistency, and interoperability across datasets.
- Linking fields like Biota and Latin_name enables cross-referencing and aggregation by species.
- Clear collection timing (Collection_Date) and standardized units facilitate longitudinal and comparative analyses.

## Practical considerations for Data Leaders
- Use standardized schemas to ensure data products are reusable by policy colleagues and external partners.
- Prioritize completeness and clarity of metadata to address potential data gaps and quality concerns.
- Leverage the explicit mass measurements to support analytical and dissemination workflows, ensuring updates to any field propagate to data products.