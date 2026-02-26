# Tree, vegetation and soil information from an ecological survey of semi-natural woodlands in the English Lake District, 1969

## Overview
- A survey of 48 semi-natural woodlands in the English Lake District conducted in June–August 1969.
- Within each woodland, six randomly placed 20 m × 20 m plots were sampled (some sites sampled with up to eight plots).
- Data collected include trees, shrubs, ground flora, bryophytes, and soils, using standardized methods.
- Aimed to enable objective site classification and provide data for broader woodland surveys and ecological analyses.

## Data content and structure
- Datasets and components:
  - LAKEDISTRICTWOODS_1969_SITES: woodland site identifiers, names, and locations (OS grid references).
  - LAKEDISTRICTWOODS_1969_GROUND_FLORA: ground flora presence/absence data from 10 nests per plot (25 cm × 25 cm sampling areas); includes species names, bryophyte records, nest-level presence/absence, and a QUAD_COUNT summarizing nest data.
  - LAKEDISTRICTWOODS_1969_SoilPH: soil pH values from the top 10 cm at specified nests within plots; includes a QC note and missing-value indicator (999) for absent samples.
  - TREE data: Species, DBH (cm), heights, and related metadata for trees; includes TREE_ID, SITE_ID, PLOT, D_CODE, HT_FT, HT_M, STEM_COUNT, and TYPE (TREE or SHRUB).
  - Additional structure: similar plot-level data (LAKEDISTRICTWOODS_1969_PLOTS) detailing plot-level metadata such as date, weather, aspect, slope angle, and coordinates (EASTING/NORTHING/OSGR).
- Field and coding details:
  - Species names aligned to Latin nomenclature (BRC_NAME; BRC_NUMBER links to a species library).
  - Bryophyte data included in ground flora with taxonomic updates and linkage to the BRC/CS_VEG vocabulary.
  - Plant data captured at the plot level with nest-level sampling and 20 m × 20 m plot geometry.
  - Coordinates and grid references provided for site localization and mapping.
- Site list:
  - A list of 48 woodland sites with IDs and OS grid references (e.g., Addyfield, Arnside Knott, Barton Park, etc.), facilitating site-level aggregation and cross-referencing with maps.

## Methodology and sampling design
- Design:
  - 48 woodlands selected with six (occasionally up to eight) randomly placed 20 m × 20 m plots per site.
  - At each plot, data collected on date, weather, aspect, and slope (angle).
- Measurements:
  - Trees: DBH measured for individuals within the plot; heights of tallest trees recorded; species identified.
  - Shrubs: DBH categories and heights recorded for shrubs within the plot; clumps assessed for tallest shrub height.
  - Ground flora: 10 nest sampling areas per plot (each 25 cm × 25 cm) documenting presence/absence of vascular plants and bryophytes.
  - Soil: top 10 cm sampled at five points per plot for pH (measured with a glass electrode) and loss on ignition (LOI) analysis on a bulked sample.
- Documentation and design notes:
  - Plot sampling is depicted as entire 20 m × 20 m plots divided into a 4 × 4 m grid with nests and specific sampling intersections for trees, shrubs, and nutrients.
  - Data were recorded with standardized forms and templates (e.g., Tree Recording Sheet; Shrub Recording Sheet).

## Provenance, documentation and related datasets
- Origin and management:
  - Originator: Woodland Ecology Section, Nature Conservancy – Merlewood, Grange-over-Sands, Cumbria.
  - Data management credited to Wood, C.
  - Surveyors included representatives such as Bunce, Brown, Shaw, White, Gardiner, Procter, Birkett, McAllister, Smith, Parrington, Wrigley.
- Background and context:
  - Based on site classification concepts developed at Merlewood (1968) and data drawn from Woodland Cards (Steele, 1968) for presence/absence species data.
  - Preliminary analyses used association-analysis techniques to identify representative groups and validate classification procedures.
  - Experience from this Lake District study informed planning for the National Woodland Surveys of 1971.
- Related literature and datasets:
  - Key methodological references: Bunce & Shaw (1973); Williams & Lambert (1959); Allen (1974); and later data compilations (Wood et al., 2015; Wood et al., 2016).
  - Related broader datasets: Woodland Survey of Great Britain, 1971 (Wood et al., 2015).

## Data quality, standards and metadata
- Taxonomic updates:
  - Latinization of species names (BRC_NAME) aligned with current nomenclature; updates linked to standard taxonomic references (e.g., New Flora of the British Isles by Stace, 2010).
- Data structure and interoperability:
  - Data stored in multiple tables with explicit keys (SITE_ID, PLOT, NEST1–NEST10, etc.) to support relational querying.
  - Soil pH values flagged for missing samples (999) and accompanied by quality notes (QC).
- Documentation lineage:
  - Clear provenance from original field sheets, with cross-references to standard methods and published reports.
  - Detailed site and plot metadata (dates, weather, aspect, angle, coordinates) enabling reproducibility and re-use.

## Access, reuse and related datasets
- Rich, multi-table dataset enabling ecosystem and vegetation analyses, including:
  - Species-level records (trees, shrubs, ground flora, bryophytes) with taxonomic standardization.
  - Plot-level environmental context (slope, aspect, weather, date, and location).
  - Soil chemistry and organic content indicators (pH and LOI) across plots.
- Related datasets and publications provide broader context and comparability for longitudinal woodland studies (e.g., Woodland Survey of Great Britain 1971; later Earth System Data compilations).

## Stewardship considerations and challenges
- Expected data stewardship needs:
  - Maintain clear provenance, stable identifiers, and traceable links between sites, plots, and specimens (trees/shrubs/ground flora/soils).
  - Preserve taxonomic mappings (BRC_NAME and BRC_NUMBER) and ensure Latin-name alignment over time.
  - Document data processing decisions (e.g., nest-level aggregation, LOI calculation, pH measurement assumptions) and maintain data dictionaries or codebooks.
- Potential challenges for data stewards:
  - Managing data across multiple interrelated tables with consistent keys and definitions.
  - Handling incomplete data (e.g., missing pH samples indicated by 999) and documenting QC notes.
  - Integrating legacy data with modern vocabularies and ensuring interoperability with newer woodland datasets.
  - Ensuring long-term accessibility and discoverability given the age of the data and potential formatting differences.

## Practical implications for users
- The dataset enables classification and comparative analysis of Lake District semi-natural woodlands from 1969, with robust environmental context and standardized measurement schemes.
- Useful for macro-ecological studies, historical vegetation change research, and methodological evaluation of standardized survey procedures.
- Users should reference the primary methodological sources and provenance records when analyzing or republishing results.