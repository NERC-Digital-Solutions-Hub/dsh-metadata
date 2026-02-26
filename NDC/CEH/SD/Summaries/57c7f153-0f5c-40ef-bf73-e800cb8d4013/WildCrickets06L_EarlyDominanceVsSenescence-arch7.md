# WildCrickets06L_EarlyDominanceVsSenescence

## Overview
- Dataset describing singing activity per crickets' sample and per individual male.
- Includes early-life dominance classification as high (H) or low (L) relative to the population median (EarlyDominance).
- Key attributes: Year, ID, Temp (ambient °C at sampling), Age (days at sampling), Sings (1 = singing, 0 = not singing).

## Data fields (variables)
- EarlyDominance: H or L (dominance classification early in life).
- Year: year when the cricket was alive.
- ID: individual identification.
- Temp: ambient temperature at sampling (°C).
- Age: age at sampling (days).
- Sings: 1 if singing at sampling, 0 otherwise.

## GIS relevance and usage
- Potential to map behavioral patterns and senescence if spatial data is available or linked by ID.
- Useful for spatiotemporal analyses of activity and dominance across landscapes or habitats.
- Can be enriched by joining with location, habitat, or environmental covariates using ID.

## Data quality, challenges, and requirements for GIS
- No explicit spatial coordinates in this description; location data may be stored separately.
- Requires data cleaning and type validation (numeric Year, Age; binary Sings; categorical EarlyDominance).
- Multiple samples per ID imply hierarchical structure; consider per-individual and per-sample analyses.
- Temporal dimension (Year) enables time-based mapping but depends on complete sampling records.

## Best practices for GIS specialists
- Establish a join workflow linking ID to geographic locations or shapefiles.
- Create maps by Year, by Sings status, and by EarlyDominance category to reveal patterns.
- Validate and document data quality; handle missing values and ensure consistent unit usage (e.g., Temp in °C).