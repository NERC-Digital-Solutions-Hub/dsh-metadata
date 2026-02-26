# Description of the Data and file structure

- Scope and content
  - Recorded data: abundance of freshwater macroinvertebrates in England.
  - Data format: long-form (year, month, day, site, sample, taxon, abundance) stored as a single RDS file; accessible via R.
  - Time frame: 2002–2019 (data prior to 2002 excluded due to limited recording of abundance).
  - Sampling method: three-minute kick-samples (net disturbance for 3 minutes downstream of a sampled area).
  - Purpose: originally collected to understand water quality; derived from EA Ecology and Fish Explorer Macroinvertebrate database; data pooled by family and wider taxonomic groupings.

- Spatial and temporal coverage
  - Sites across England; 5009 sites included in final dataset (out of 10,136 originally).
  - Sampled in ten river basins under the EU Water Framework Directive.
  - Seasons: spring (Mar–May) and autumn (Sept–Nov).
  - Dataset includes 67,757 macroinvertebrate samples across 2002–2019.

- Dataset structure and fields
  - Key columns: riverbasin, agency_area, waterbody, wfd_waterbody_id, site_id, full_easting, full_northing, season, year, month, day, Latitude, Longitude, sample_id, order_taxon, family_taxon, total_abundance, year_scaled, group.
  - Data quality indicator: missing data coded as NA.
  - Taxa included: Ephemeroptera, Plecoptera, Hemiptera, Megaloptera, Odonata, Coleoptera, Trichoptera, Turbellaria, Annelida, Crustacea, Diptera, Mollusca; abundances summed to the family level within these groups.

- Data collection and processing
  - Data extracted from EA’s ecological monitoring database; filtered to three-minute kick-sample data (≈99% of samples).
  - Included only sites sampled for at least three of eighteen years in both spring and autumn.
  - Final dataset: 3764 samples per year on average; spanning 2774 waterbodies.
  - National distribution biased toward mid to lower perennial reaches, reflecting monitoring program aims for environmental quality.
  - Data manipulation and analysis conducted in R (2019–2022).

- Quality control and limitations
  - 2002 onward: enhanced quality control with one-in-ten samples independently re-analysed.
  - Original data cover 1991 onward, but the usable, high-quality dataset is 2002–2019.

- Nature and units of values
  - Values are discrete counts: the number of individual macroinvertebrates observed.

- Access, provenance, and downstream use
  - Access link: https://environment.data.gov.uk/ecology-fish
  - Related published work: Powell et al. (2022) Global Change Biology on abundance trends across taxa and river typology.
  - Data provenance: derived from EA monitoring data; used for national-scale ecological insights and monitoring framework decisions.

- Relevance for monitoring frameworks
  - Highlights need for robust metadata and data governance to enable reuse, transparency, and comparability.
  - Demonstrates challenges in data access, standardization, and timely updates.
  - Provides a case study of data transformation (long-form to analyzed summaries) and quality assurance practices to inform future monitoring designs.