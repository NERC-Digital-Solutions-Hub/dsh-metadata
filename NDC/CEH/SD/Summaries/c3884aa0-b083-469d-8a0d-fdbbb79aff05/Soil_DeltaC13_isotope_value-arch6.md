# DATA HEADER INFORMATION for Soil_DeltaC13_isotope_value.csv

## Overview
- The dataset records the Soil organic carbon content obtained with 13C isotope analysis.
- Related references: Manual_1_Classical_Survey.rtf (page 15, section 3.2); Programme ESPA; Project P4GES.
- Acknowledgement of the Laboratoire des Radio Isotopes, Université d'Antananarivo is required for products derived from these data.

## Data fields and units
- ZOI (Zone of Interest): Categorical; Units = ZOI1: Lakato / ZOI2: Andasibe / ZOI3: Anjahamana / ZOI4: Didy.
- Location: Sampling point location; Text String.
- Site: P4GES site code; Text String.
- C%: Carbon content percent; Numeric; Unit = %.
- delta13C: Delta 13C; Numeric; Unit = ‰ (per-mille).
- Depth: Depth of soil sampling; Numeric; Unit = cm.

## Data quality and handling
- Blank cells denote no data available.
- Data derive from 13C isotope analysis; interpret delta13C values with appropriate context.
- Data may exhibit gaps across ZOI/locations; prepare for missing values when integrating.

## Usage and provenance
- Useful for exploring and comparing soil carbon content across zones, locations, and depths.
- When sharing outputs, cite the DOI/project and acknowledge the contributing laboratory as specified.

## Access and notes
- The header defines data types, units, and structure to aid data cleaning, merging, and reuse.
- No additional access restrictions stated beyond standard acknowledgment requirements.