# Biota

## Overview
- A structured data dictionary for biological sampling data used in environmental health monitoring.
- Defines key fields related to biota identity, collection metadata, and various mass measurements for different body parts.

## Data schema and fields
- Biota: English name of the biota (with explanation; units not applicable).
- Latin_name: Latin name of the species (with explanation; units not applicable).
- Collection_Date: Date the sample was collected; format is dd month yyyy (with explanation).
- ID: Identifier in the data (where applicable) (no units; notes present).
- Whole_body_g: Mass of the whole body, in grams (units: grams).
- Gut_g: Mass of the gut, in grams (units: grams).
- Tissue_with_thyroid_g: Mass of the sample containing the thyroid when the thyroid is too small to separate; analysis is on the surrounding area (grams).
- Thyroid_g: Mass of the actual thyroid gland (grams).
- Liver_g: Mass of the liver (grams).
- Kidney_g: Mass of the kidney (grams).
- Carcass_g: Mass of the carcass (grams).

## Metadata conventions
- Each field includes an Explanation to clarify what is measured.
- Units are specified for quantitative fields (primarily grams; date format for Collection_Date).
- Notes provide handling details, such as how Tissue_with_thyroid_g is defined when the thyroid is not separable.

## Relevance to monitoring frameworks
- Demonstrates a standardized approach to capturing biological monitoring data, supporting comparability across studies.
- Metadata-rich fields facilitate data interpretation, quality assessment, and reuse in policy evaluation and decision-making.
- Focuses on measurable endpoints (various tissue masses) that can underpin contaminant load assessments and physiological studies.

## Data quality, governance, and use challenges (aligned with authors of monitoring frameworks)
- Standardization of terminology and units is crucial to enable data integration across programs.
- Metadata completeness (explanation and notes) is essential for verifying data suitability and reuse.
- Data sharing and openness must balance transparency with privacy and sensitivity considerations; clear documentation supports governance processes.
- Timely data availability and avoidance of silos improve utility for policy scrutiny and future decision-making.