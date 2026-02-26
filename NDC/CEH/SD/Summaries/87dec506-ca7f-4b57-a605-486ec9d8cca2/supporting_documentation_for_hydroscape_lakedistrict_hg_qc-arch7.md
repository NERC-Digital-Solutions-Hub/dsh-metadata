# Associated file: hydroscape_lakedistrict_hg _cores_qc.csv

## Overview
- Describes the table headings for results of measurements of reference sediment LKSD2 and procedural blanks.
- Core sediments were measured by Cold Vapour Atomic Fluorescence Spectroscopy (CV-AFS) after reduction with SnCl2.
- Mercury concentrations were measured at UCL Geography using aqua regia digestion of freeze-dried core samples.

## Methods
- Sample preparation: Freeze-dried core samples digested in aqua regia at 100°C for 2 hours in rigorously acid-leached 50 ml tubes.
- Reference material: LKSD2 sediment with certified Hg value 160 ± 19 ng g-1; prepared from Provisional Elemental Values for Lake Sediment Reference Materials.
- Measurement workflow: LKSD2 reference sediment and aqua regia samples run as samples; includes a measured blank (Measured_blank_ng_ml) and quality control checks.
- Quality control: Laboratory standard solutions and QC blanks measured every five samples to monitor instrument stability.

## Table structure and fields
- Lake_District_Hg_Core_Runs: Name of Hg cores run through the CV-AFS machine.
- Tube_Code: Code for the tube, e.g., LKSD2….
- Reference_Sediment_mass_g: Mass of reference sediment weighed out (approximately 0.2 g).
- Hg_ng_g: Mercury concentration in sediment expressed in ng/g.
- Hg_µg_g: Mercury concentration in sediment expressed in µg/g.
- Measured_blank_ng_ml: Mercury concentration measured in the procedural blank (ng/ml).
- Description: Brief description corresponding to the Hg core run and associated measurements.

## Reference material
- LYNCH, J. (1990) Geostandards Newsletter: Provisional Elemental Values for LKSD-series reference materials (LKSD-1 to LKSD-4), underpinning the LKSD2 standard used.

## Relevance for GIS and data products
- Provides a structured, QC-annotated dataset suitable for map-based visualization of Hg concentrations in Lake District core sediments.
- Includes both sample measurements and blanks, enabling assessment of data reliability when integrating with spatial layers.
- Clear units and measurement context facilitate joining with other geochemical or sediment datasets in GIS workflows.

## Quality and provenance considerations
- Measurements tied to a certified reference material with documented uncertainty.
- Regular QC blanks and standards to ensure machine stability and data integrity.
- provenance linked to a published reference material, enabling traceability in GIS metadata.