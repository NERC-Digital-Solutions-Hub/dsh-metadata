# Description of the Data and file structure

- The dataset records the abundance of freshwater macroinvertebrates in England, provided as a long-form file (year, month, day, site, sample, taxon, abundance) and stored as an RDS file for access via R.
- Coverage and sampling period: samples collected across England from 2002–2019, during March–May (spring) and September–November (autumn).
- Sampling method: three-minute kick-samples using a net to collect invertebrates and debris, standardized semi-quantitative approach for assessing macroinvertebrate ecology and water quality.
- Pre-2002 data: excluded because macroinvertebrate abundance was not widely recorded before 2002.
- Data lineage: derived from the Environment Agency's Ecology and Fish Explorer Macroinvertebrate database; data pooled by family and wider taxonomic groupings; provided as a single RDS file.
- Data columns (selected): riverbasin, agency_area, waterbody, wfd_waterbody_id, site_id, full_easting, full_northing, season, year, month, day, Latitude, Longitude, sample_id, order_taxon, family_taxon, total_abundance, year_scaled, group. Missing values coded as NA.
- Taxa included: Ephemeroptera, Plecoptera, Hemiptera, Megaloptera, Odonata, Coleoptera, Trichoptera, Turbellaria, Annelida, Crustacea, Diptera, Mollusca.
- Data processing: final dataset from 2002–2019, with 67,757 individual macroinvertebrate samples from 5009 sites (out of 10,136 originally); represents about 3764 samples per year across 2774 waterbodies in ten river basins under the Water Framework Directive.
- Scope and distribution: nationally distributed but biased toward mid-to-lower perennial river reaches; designed to reflect monitoring programmes for environmental quality rather than pure biodiversity sampling.
- Data handling and analysis: manipulated and analyzed in R during 2019–2022.
- Quality control: starting in 2002, improved abundance estimation with a quality-control procedure where one in every ten samples was independently re-analysed.
- Nature of recorded values: discrete counts representing the number of individuals observed.
- Sharing/access: publicly accessible at https://environment.data.gov.uk/ecology-fish; used in Powell et al. (2022) Global Change Biology; dataset and methods described in the paper (Abundance trends for river macroinvertebrates vary across taxa, trophic group and river typology).
- Related workflow: data were filtered to include only three-minute kick-samples and sites sampled for at least three years out of 18 spring/autumn windows; analysis and reporting were conducted using R.