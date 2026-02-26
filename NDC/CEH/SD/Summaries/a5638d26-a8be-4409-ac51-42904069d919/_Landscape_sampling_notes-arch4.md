# Summary Experimental Design/Sampling Regime

- Purpose and scope
  - Field-based study of earthworms across multiple farms/fields with varied land uses (organic and conventional, arable and ley).
  - Aimed at characterising earthworm communities along hedges, margins, and within fields to understand spatial patterns and effects of land use.

- Study sites and sampling units
  - Sites include Little Langton (LL), Hutton Wandesley (HW), Overton (OV), Whenby (WH).
  - Landuse categories include organic arable (A1, A2), organic ley (B1, B2), and conventional arable/ley.
  - Paired transects used in some comparisons (e.g., WH/HW), with transects taken from hedge into field.

- Sampling design and field methods
  - A transect laid at 90 degrees from the hedge, typically mid-field along the hedge length.
  - Soil pits (18 x 18 x 15 cm) excavated at hedge, margin, and at 2, 4, 8, 16, 32, 64 m along transect.
  - Earthworms extracted using a mustard solution, preserved for identification with Sims and Gerard key.
  - Measurements taken at each pit:
    - Number of earthworms and biomass (grams)
    - Distance from hedge; depth indicator (H for hedge, M for margin)
    - Soil moisture (three readings in mV) at 5 cm and 10 cm
    - Soil temperature at 5 cm and 10 cm
    - Soil bulk density at 5 cm and 15 cm (via bulk density rings)
  - Depth/sample coding indicates whether a sample came from mustard-drawn sample (P) or topsoil (S).

- Data collected and recorded values
  - Biological: earthworm counts and biomass; species identities mapped to functional groups.
  - Environmental: soil moisture, soil temperature, soil bulk density.
  - Spatial: distance from hedge; location type (H or M); field/field name; transect code; sampling date.

- Species codes and functional groups
  - Species are coded (e.g., Aporrectodea caliginosa, Lumbricus terrestris, Eisenia fetida, etc.) and linked to functional groups:
    - Endogeic (soil-living, horizontal burrows)
    - Epigeic (litter-living)
    - Anecic (soil-living, deep vertical burrows)
  - Some entries indicate damaged or immature statuses:
    - END-dm, EPI-dm, ANE-dm (damaged)
    - END-im, EPI-im, ANE-im (immature)
    - 1 = damaged (for certain categories)

- Data files and structure
  - Landscape2016_soil_data.csv
    - 14 columns
    - Fields include: Date, Field, Distance, Hedge/Margin indicator, Depth (Mustard vs Topsoil), Sample type (A = abundance, B = biomass), and per-species abundance/biomass data.
  - EW_landscape.csv (and related LL, HW, OV, WH, etc. files)
    - 30 columns
    - Fields include: Date, Field, Transect, Distance, Depth (Mustard vs Topsoil), Sample type (A/B), and per-species counts/biomass.
  - Species and codes listed with corresponding functional groups and taxonomic names.
  - Additional metadata:
    - “blank cell = no data available” (missing data indicator)
    - Date formats, field names, and coded distances from hedge (H) or margin (M)

- Data units and measurement details
  - Earthworm counts (numerical abundance)
  - Biomass (grams)
  - Distances (metres from hedge)
  - Soil moisture (mV readings at 5 cm and 10 cm)
  - Soil temperature (degrees Celsius)
  - Soil bulk density (g/cm^3)
  - Depth indicators: Mustard (P) vs Topsoil (S)

- Data provenance and references
  - Earthworm taxonomy and identification references: Sims & Gerard (1999)

- Data quality, limitations, and notes
  - Spatial and temporal sampling varied by site and transect configuration.
  - Data include explicit paired transect design in some comparisons.
  - Some data gaps indicated by blank cells; some fields have limited replication depending on site and date.
  - Clear documentation of depth, location type, and measurement protocols supports reproducibility.

- Implications for data governance and reuse (relevant to Data Leaders)
  - Demonstrates need for standardized metadata, consistent coding for species and functional groups, and clear depth/location indicators to enable cross-site comparisons.
  - Highlights importance of comprehensive data provenance (sampling dates, field identifiers, transect design) for end users.
  - Provides a rich dataset for analyses of hedgerow effects, land-use impacts on soil biota, and spatial biodiversity patterns, with clear pathways for data sharing and collaboration across networks.