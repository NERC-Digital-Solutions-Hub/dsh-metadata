# Description of the Data and file structure

- What the dataset is
  - A single rds file containing processed abundance data for freshwater macroinvertebrates in England (2002–2019), collected via three-minute kick-samples and expressed as long-form data (year, month, day, site, sample, taxon, abundance). Data have been pooled by family and wider taxonomic groupings.

- Geography and spatial attributes
  - Spatially distributed across England with fields for river basin, EA agency area, waterbody name, Water Framework Directive waterbody code, site identifiers, and precise coordinates (full_easting, full_northing; Latitude, Longitude in decimal degrees).
  - Designed for map-based analyses and GIS visualisations of spatial patterns.

- Sampling, data collection, and processing
  - Collected 2002–2019; sampling occurred in spring (March–May) and autumn (September–November).
  - Three-minute kick-sample method used to collect invertebrates and debris; samples primarily used for water quality indicators.
  - Data filtered to include sites sampled for at least three years out of 18 in both spring and autumn.
  - Taxa retained: Ephemeroptera, Plecoptera, Hemiptera, Megaloptera, Odonata, Coleoptera, Trichoptera, Turbellaria, Annelida, Crustacea, Diptera, Mollusca.
  - Abundances summed at the family level within these taxa; dataset derived from Environment Agency Ecology and Fish Explorer Macroinvertebrate database and manipulated in R (2019–2022).

- Data structure and key fields
  - Core columns include: riverbasin, agency_area, waterbody, wfd_waterbody_id, site_id, full_easting, full_northing, season, year, month, day, Latitude, Longitude, sample_id, order_taxon, family_taxon, total_abundance, year_scaled, group.
  - Missing data coded as NA.

- temporal scope and coverage
  - Final dataset covers 2002–2019.
  - 67,757 samples from 5,009 sites (out of 10,136 originally); about 3,764 samples per year.
  - Spans 2,774 waterbodies across ten WFD river basins in England (Anglian, Humber, North West, Northumbria, Severn, Solway Tweed, South East, South West, Thames).
  - Notable bias toward mid-to-lower perennial river reaches (reflecting monitoring program design for environmental quality rather than intrinsic biodiversity).

- Quality control and data provenance
  - QC implemented since 2002: approximately one in ten samples independently re-analysed.
  - Although some data exist from earlier years (1991), the dataset is restricted to 2002–2019 due to improvements in abundance estimation and QC.

- Data usage, access, and provenance
  - Publicly accessible via Environment Agency: https://environment.data.gov.uk/ecology-fish
  - Used in Powell et al. (2022) Global Change Biology to examine abundance trends across taxa, trophic groups, and river typology.

- Units and nature of the data
  - Abundance values are discrete counts of individuals (per sample at the family level).