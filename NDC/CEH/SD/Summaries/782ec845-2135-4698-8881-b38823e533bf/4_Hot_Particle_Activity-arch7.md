# Metadata for 4_Hot_Particle_Activity.csv

## Overview
- Metadata for a CSV dataset of Chernobyl hot particles, detailing identifiers, spatial sampling coordinates, particle properties, radioisotope activities, measurement dates, and visual/ descriptive attributes to support GIS-based mapping and analysis.

## Spatial and sampling metadata
- Angle_degree: polar coordinate angle around ChNPP, clockwise; 0°/360° = North.
- DIST_km: radial distance from the center (ChNPP); notes mention samples at (0,0) in Shelter.
- Sampling locations noted in notes (e.g., Mikolki, Warsawa, Lomza, Bialystok, Suwalki) and context for Polish samples.
- Coordinates often provided in polar form; GIS workflows may require conversion to planar coordinates.

## Particle properties and classifications
- MAXSIZE_um and MINSIZE_um: particle size range in micrometers.
- VIEW: visual representation category for particle appearance (A, B, C; see notes).
- COLOR: particle color attribute.
- FORM: form or inclusions description.
- STRUCT: structure of the particle or sample location notes (e.g., crystalline, fine grained, fragmented); sample origin codes provided (Warsawa, Mikolajki, Lomza, Bialystok, Suwalki).
- Burnup_MW_d_kg-1: burnup category derived from activity ratios, classified into 17 groups.

## Isotope activities and uncertainties
- Multiple isotopes covered with Activity (Bq) and STD (Bq) values, including:
  - 95Zr, 95Nb
  - 106Ru
  - 125Sb
  - 134Cs, 137Cs
  - 144Ce, 154Eu, 155Eu
  - 54Mn
  - 60Co
  - 241Am
  - 90Sr
- Each entry pairs total activity with corresponding standard deviation; some fields include date and measurement context.

## Temporal metadata
- DATE_Gamma, DATE_Alpha, DATE_Beta: dates of gamma, alpha, and beta measurements (format examples: dd-mmm-yyyy); accompanying data fields indicate measurement-related timing.

## Visual and descriptive attributes
- VIEW, COLOR, FORM, STRUCT: attributes used to describe and symbolise particles in GIS visualisations (e.g., color coding by group, view type, and morphology).

## Data provenance and references
- References to foundational works on Chernobyl hot particles, including Begichev et al. (1990), Kashparov et al. (1996, 1997), Kuriny et al. (1993), and Zhurba et al. (2009), among others, indicating sources for classifications, measurements, and interpretation.

## GIS usage considerations
- Data supports creating map layers of particle sampling points with rich attribute tables (identifiers, spatial coordinates, particle properties, and radiological data).
- Classification and filtering opportunities:
  - Burnup_MW_d_kg-1 groups for thematic mapping.
  - Group A/B/C-like isotope profiles for isotope-based styling.
  - MINSIZE_um and MAXSIZE_um for size-based queries.
- Symbology can leverage VIEW and COLOR to convey particle appearance and classification; STRUCT and FORM provide morphology context.
- Dates enable temporal analyses or validation of measurement campaigns.

## Data quality and challenges
- Data are distributed across multiple sources with potential inconsistencies in standards and resolutions.
- Some sampling coordinates may be incomplete or require coordinate transformation from polar to GIS-ready formats.
- Large or complex datasets may need segmentation and rigorous data cleaning before integration into GIS workflows.