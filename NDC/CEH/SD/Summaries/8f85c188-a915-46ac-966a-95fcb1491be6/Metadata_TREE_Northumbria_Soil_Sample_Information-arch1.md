# TREE_Northumbria_Soil_Sample_Info

## Overview
- Defines the data schema for Northumbria soil samples collected by CEH.
- Captures both sampling metadata and key soil properties/analyses to support analysis, comparison, and modeling.

## Fields and Definitions

- CEH_Sample_Description — CEH sample name. Units: n/a. Explanation: CEH sample name.
- Site — Sampling site. Units: n/a. Explanation: Site.
- National_Grid_Reference — National grid reference of soil sampling site. Units: n/a. Explanation: National grid reference of soil sampling site.
- Date_Sample_Collected — Date sample collected. Units: n/a. Explanation: Date sample collected.
- CEH_Sample_Code — CEH sample code related to soil sample. Units: n/a. Explanation: CEH sample code related to soil sample.
- pH — pH of soil sample. Units: n/a. Explanation: pH of soil sample.
- LOI — LOI of soil sample. Units: n/a. Explanation: LOI of soil sample.
- Soil_Sampling_Depth_cm — Soil sampling depth in cm. Units: cm. Explanation: Soil sampling depth in cm.
- Mass_Fresh_Soil _kg — Fresh mass of soil sample in kilograms. Units: kg. Explanation: Fresh mass of soil sample in kilograms.
- Mass_Dry_Soil_kg — Dry mass of soil sample in kilograms. Units: kg. Explanation: Dry mass of soil sample in kilograms.
- General_Notes — General notes. Units: n/a. Explanation: General notes.
- Sample_Preparation_And _Analysis_Performed — Sample preparation of animal or sample and analysis performed. Units: n/a. Explanation: Sample preparation of animal or sample and analysis performed.

## Data Characteristics
- Data types and units are specified or noted for each field; several fields use n/a units (descriptive/identification fields).
- Measured properties include soil pH, LOI (loss on ignition), and physical sampling details (depth, fresh and dry mass).

## Usage for Analysis
- Enables linking sample metadata with analytical results to explore relationships (e.g., pH vs. LOI, depth effects, mass changes).
- Supports traceability and reproducibility, as each sample has descriptive name, site reference, collection date, and preparation/analysis information.
- Facilitates data integration and comparison across samples through standardized fields like grid reference, depth, and masses, along with preparation/analysis records.