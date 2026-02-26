# Metadata for Woody species

- Purpose and use
  - Provides coded metadata for GIS mapping and map-based data visualisations of woody species.
  - Facilitates linking species names and functional groups to spatial data for analysis and presentation.

- Woody species metadata (structure and notes)
  - Each entry uses a code (e.g., ANAGFOET) linked to:
    - Scientific name (e.g., Anagyris foetida L.)
    - Functional group / life form (e.g., Legume)
  - Characteristics
    - Extensive list of codes with corresponding scientific names and, where available, functional group/life form.
    - Some entries have missing functional group (FG) data.
    - Taxonomic notes include instances of subspecies not differentiated (e.g., JUNIPHOE with 2 subspecies not differentiated; COROVALE with 3 subspecies not differentiated).
  - Examples of patterns
    - ANAGFOET, ANAGSSPS, ARBUUNED, ARTEARBO, etc., with FG entries often listed as Legume or left blank.
    - Some entries indicate subspecies detail but lack differentiation in the metadata (e.g., JUNIPHOE, CISTCRET subsp. eriocephalus, COROVALE with subspecies not differentiated).

- Herbaceous species metadata

  - Structure
    - Similar code-based scheme (e.g., AGROPOUR) paired with:
      - Scientific name (e.g., Agrostis pourretii Willd.)
      - Functional trait / growth form (e.g., Graminoid, Forb, Geophyte/forb)
  - Notes
    - Rich listing across many taxa with diverse growth forms: Graminoid, Forb, Geophyte/Forb, Legume, etc.
    - Some entries show partial data (e.g., “.” or blanks) for the functional trait/growth form.
    - Includes unidentified entries (UNIDENTA, UNIDENTB) and numerous subspecies/varieties distinctions without full differentiation.

- Key observations for GIS work
  - The woody and herbaceous sections provide a comprehensive code-to-name-to-growth form mapping, enabling attribute joins to spatial data.
  - The dataset acknowledges incomplete data in places (missing FG/growth form, unresolved subspecies), which could affect classification and symbolization in maps.

---

# Metadata for spatial and environmental data

- Spatial coordinates and topography
  - LATITUDE: Latitude in decimal degrees
  - LONGITUDE: Longitude in decimal degrees
  - ALTITUDE: Altitude in metres
  - SLOPE: Slope in degrees
  - Aspect: Aspect in compass degrees

- Geological and soil context
  - ROCKCROP: Percentage of rock outcropping
  - SOILPH: Soil pH (measured for 50 sites)

- Vegetation and land-use context
  - Grazing index: Ranked index with 1 to 4, defined as:
    - 1) unbrowsed
    - 2) lightly browsed
    - 3) moderate to heavy browsing
    - 4) severely clipped
  - This provides a qualitative measure of herbivory pressure affecting vegetation structure.

- Olive-tree metrics (structured in height and diameter classes)
  - OLIVDIAA, OLIVDIAB, OLIVDIAC, OLIVDIAD, OLIVDIAE: Olive diameter classes at 30 cm height (0–5 cm to >20 cm)
  - OLIVBREA, OLIVBREB, OLIVBREC, OLIVBRED, OLIVBREE: Olive diameter classes at breast height (0–5 cm to >20 cm)
  - MEAN30: Mean number of olive trees (30 cm height)
  - MEANDBH: Mean number of olive trees (breast height)
  - FREQ30: Frequency of olive trees (30 cm height)
  - FREQDBH: Frequency of olive trees (breast height)

- Application considerations for GIS
  - The dataset combines precise geospatial points with rich site-level environmental variables and olive-tree metrics, enabling:
    - Spatial analysis of olive stand structure and distribution
    - Habitat and biodiversity mapping in relation to site conditions (slope, aspect, rock outcrop, soil pH)
    - Assessment of grazing influence on vegetation patterns

- Data quality and integration notes
  - The spatial and environmental data are clearly structured with explicit units, but care should be taken to:
    - Ensure coordinate reference system consistency for LATITUDE/LONGITUDE
    - Validate the climbing of "Soil pH for 50 sites" and ensure site correspondence with species metadata
    - Address any missing or incomplete data fields (e.g., blank FG in woody/herbaceous sections) before map production or analysis

- GIS use-case suggestions
  - Create maps showing species distributions by coding framework, layered with environmental variables (slope, aspect, rock outcrop, soil pH)
  - Visualize olive stand structure across sites using MEAN30/MEANDBH and frequency metrics
  - Analyze how grazing intensity correlates with woody/herbaceous species presence and growth forms
  - Develop thematic maps distinguishing unidentified species entries (UNIDENTA/B) to guide data curation efforts