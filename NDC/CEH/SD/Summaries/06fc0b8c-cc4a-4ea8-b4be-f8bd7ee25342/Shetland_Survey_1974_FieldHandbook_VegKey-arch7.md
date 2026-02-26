# Vegetation Types and Indicator Species (Shetland Islands)

## Overview
- The document defines a comprehensive, map-oriented typology of vegetation communities on Shetland islands.
- It enumerates 30 distinct Type classifications (Type 1 to Type 30) describing dominant cover species, indicator/selective species, and typical habitat characteristics.
- Each Type includes information on occurrence frequency, association with habitat features (peat depth, moisture, pH), and coastal versus inland distribution.

## Data and GIS-Ready Attributes
- Core attributes per Type:
  - Type ID (1–30)
  - Major cover species (e.g., Calluna, Eriophorum angustifolium, Sphagnum spp.)
  - Indicator/Selective species lists (grouped as high-frequency or notable species)
  - Bare ground presence and extent
  - Environment and substrate: soil depth categories, soil moisture/wetness, pH
  - Habitat context: peatlands, streamsides, rocky outcrops, ditches, coastal zones
  - Occurrence frequency: limited, average, widespread, or absent from certain locales (e.g., Yell, Unst)
  - Constant species groups (A, B, C, D, etc.) used to define Type constants
- Spatial relevance:
  - Types are linked to specific island-scale patterns (coastal vs inland; proximity to sea, streams, and peatlands)
  - Some Types are noted as restricted or absent in particular islands (e.g., Unst, Yell)

## Habitat and Environmental Context
- Dominant vegetation patterns revolve around bog/peatland ecotones and wet acidic peat (pH typically around 4.3–4.9, 4.4–4.8, or similar ranges).
- Moisture and depth gradients are crucial, with categories for deep peat vs shallow/moderate depths and moisture scales from dry to submerged.
- Common substrate themes:
  - Deep, wet acidic peat with Calluna spp. as a major cover
  - Sphagnum-dominated lawns with associated species
  - Peat edges, eroded surfaces, and seepage zones near water bodies
  - Coastal rock and debris soils with maritime flora
- Environmental indicators embedded in Types include:
  - Wetness (Dry, Damp, Very Wet, Submerged)
  - Soil depth (shallow, medium, deep >50 cm)
  - pH ranges closely tied to habitat type (e.g., around 4.4–4.9 up to ~6.3)

## Representative Type Profiles (highlights)
- Type 1 (Cladonia–Calluna type): Low heterogeneity, deep wet peat, Calluna as major cover; strong association with wet, acidic peat and bare peat patches; limited occurrence away from coast.
- Type 2 (Drosera rotundifolia–Calluna type): Low heterogeneity; Eriophorum angustifolium and Rhacomitrium lanuginosum as major cover; deep, wet peat near northern areas; sparse bare peat.
- Type 3/4 (Calluna-dominated variants): Calluna with Rhacomitrium lanuginosum; diverse selective species; inland prevalence with deep peat and wet conditions.
- Type 9–12 (Sphagnum-dominated Calluna types): Calluna as major cover with Sphagnum spp. and associated species; widespread island distribution; deep wet peat with tussocks or featureless peat.
- Type 13–16 (Carex/Nardus/Nardus-related types): Moderate to high species complements; carex/nardus major covers; often associated with eroded peat surfaces, ditches, and damp soils.
- Type 17–21 (Coastal/maritime and freshwater interfaces): Plant communities near coastlines, streams, and rock outcrops; marine-influenced soils and damp rocks; variable pH around ~5.0–5.6.
- Types 23–25, 27–30 (Maritime to rocky outcrop communities): Rocky outcrops or debris soils; diverse assemblages with Gentianella, Antennaria, Trifolium, Dactylis, Holcus; often heavily grazed or unmanaged grazed patches; high rock cover and shallow soils.

## Distribution and Occurrence Patterns
- Several Types show restricted geographic occurrences (e.g., absent from Yell and Unst; limited to northern mainland or coastal zones).
- Some Types are described as widespread across the islands, while others are tied to specific features (e.g., serpentine rocks, Serpentine outcrops, peat edges, streamsides).
- Occurrence frequencies are classified descriptively (limited, average, widespread, often near sea or streams).

## Data Quality, Standardization, and Integration Considerations
- The typology relies on qualitative ecological descriptors and lists of indicator/selective species, which can be translated into GIS lookup tables for classification.
- Challenges for GIS mapping:
  - Heterogeneity within Types and overlapping communities require rules for assignment to a single Type or a blended class.
  - Some Types have limited or island-specific distributions, necessitating careful handling of edge cases in regional datasets.
  - Incomplete or garbled text in the source material may require cross-verification with field data or supplementary sources.
  - Consistency in species names and groupings (A, B, C, D, etc.) is essential for reliable attribute coding.

## Practical GIS Implementation Tips
- Build a Type legend (Type 1–Type 30) with standardized attributes:
  - Major cover species, indicator species, selective species
  - Habitat context (peat depth, moisture, pH), bare ground presence
  - Occurrence and distribution notes (coastal, inland, island-specific)
  - Constant species groups (A, B, C, D, F, G, etc.)
- Create tiered map layers:
  - Type polygons as primary vegetation units
  - Indicator/selective species presence rasters or point data to support Type validation
  - Environmental rasters (peat depth class, moisture index, soil pH, depth to water table)
- Develop rules for Type assignment in ambiguous areas (e.g., high heterogeneity Types vs. mixed Type zones).
- Include metadata documenting island-specific constraints and absent areas (e.g., Unst, Yell) to support accurate interpretation.
- Use the environmental context as secondary layers to explain Type distribution (coastal vs inland, proximity to streams, rocky outcrops).

## Summary of Key Takeaways for GIS Specialist Use
- The document provides a comprehensive, island-scale vegetation Type classification (Types 1–30) with detailed species composition, habitat associations, and occurrence patterns.
- Each Type integrates major cover species, indicator/selective species, and environmental drivers (peat depth, moisture, pH) to support map-based representation.
- For GIS production, the data can be structured into Type polygons with rich attribute fields and complemented by environmental rasters to enable analysis of habitat suitability, distribution patterns, and management planning.
- The typology highlights the importance of peatland dynamics, coastal-maritime influences, and island-specific distributions, all of which should inform data standardization, classification rules, and visualization strategies.