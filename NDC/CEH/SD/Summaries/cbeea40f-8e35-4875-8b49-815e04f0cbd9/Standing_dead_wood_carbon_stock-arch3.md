# DATA HEADER information for Standing_dead_wood_carbon_stock.csv

## Overview
- Purpose: records the carbon stock of standing dead wood to support environmental health monitoring, policy scrutiny, and future decision-making.
- Context: associated with ESPA programme and P4GES project; requires acknowledgment of Laboratoire des Radio Isotopes, Université d'Antananarivo for products derived from these data.

## Data Content and Key Variables
- site_ID: P4GES site code; type Text.
- Surface: information field (present but metadata often incomplete; units/description may be missing or blank).
- DBH: diameter of dead wood trunk at 130 cm height; Numeric; unit: cm; data collection tool noted as forester compass.
- Diam_base: diameter at 30 cm height; Numeric; unit: cm; collected with forester compass.
- Diam_top: estimated diameter at the top of the trunk; Numeric; unit: cm.
- Height: height of the standing dead wood; Numeric; unit: m; noted field resource as vertex.
- Volume: computed volume using formula: volume = (1/3) × π × H × (r1^2 + r2^2 + r1×r2) where H is height, r1 is base radius, r2 is top radius; Numeric; unit: m^3.
- Category: classification of wood density; Categorical with options S (sound), I (intermediate), R (rotten).
- Density: numeric; unit not specified in header.
- Carbon_stock: numeric; unit listed as milligrams per hectare (Mg.ha-1), though the label may reflect Mg/ha (potential unit inconsistency).
- Notes: “Notes” indicate that 'means no data available' where applicable.

## Provenance, Metadata, and Access
- Data provenance: field measurements using forester compass (DBH, Diam_base) and vertex method (Height); Diam_top is an estimate.
- Metadata gaps: several fields show missing or undefined metadata (e.g., Surface, possibly Density; some units/descriptions blank).
- Attribution: requires acknowledgement of the listed institutions; DOIs and project names cited for traceability.
- Data sharing and openness: the header implies data sharing practices and barriers common to environmental datasets (explicitly notes acknowledgment; transparency of underlying data is a governance consideration).

## Data Quality, Gaps, and Governance Implications for Monitoring Frameworks
- Common barriers reflected: incomplete metadata, potential data standardization issues, and the need for robust data governance to ensure datasets meet standards and remain up to date.
- Transformation needs: explicit calculation method for Volume provided; clear documentation essential for reproducibility.
- Data accessibility considerations: public sharing of underlying data is a governance factor; proper attribution is required.

## Practical Implications for Monitoring Frameworks
- Use: informs estimates of standing dead wood carbon stock to support carbon accounting and policy evaluation.
- Quality control: prioritize completing metadata, standardizing units (especially for Carbon_stock), and clarifying Surface and Density details.
- Governance: implement source-level data standards, ensure data are shareable with appropriate attribution, and maintain transparent documentation of methodologies (e.g., volume calculation).