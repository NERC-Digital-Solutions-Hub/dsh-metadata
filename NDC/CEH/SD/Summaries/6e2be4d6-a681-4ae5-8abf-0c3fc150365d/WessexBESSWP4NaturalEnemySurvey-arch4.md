# Natural enemies of crop pests in oilseed rape fields in relation to local plant diversity and landscape characteristics

- Study objective: Document the number and type of natural enemies of crop pests in winter-sown oilseed rape (Brassica napus L.) and relate them to local plant diversity (in-crop and field margins) and landscape characteristics.
- Context: Part of the Wessex BESS project funded by NERC Biodiversity and Ecosystem Service Sustainability program; dataset can be used with other Wessex BESS WP4 datasets.

## Data Scope and Location

- Geographic area: Wessex region, southern England (field surveys in 2013 and 2014; landscape context includes nearby grasslands and semi-natural habitats within up to 3 km).
- Field sampling: 12 fields surveyed each year (total of 24 fields per year across 2013–2014); area characterized as largely arable and intensive grassland.
- Temporal coverage: Field data collected during two growing seasons (2013 and 2014); sampling windows in June–July for canopy invertebrates.

## Data Collection Methods

- Local habitat and plant diversity
  - Field transects: three 58 m transects per field, stratified to include hedged and non-hedged margins.
  - Margin assessment: proportion of hedge, proportion of field margin, width of field margin.
  - Plant diversity: five 1 m2 quadrats in the field margin and a crop quadrat at 8 m, 33 m, and 58 m into the crop; species identified and percent cover recorded.
- Landscape characteristics
  - GIS-based metrics (within 0.5–3 km buffers): grassland area and type (species-rich, restoring, improved, semi-natural), arable habitat, and other semi-natural habitats.
  - Data sources: CEH Land Cover Map 2007, Natural England Priority Habitats Inventory, and local National Vegetation Community surveys.
  - Additional expert inputs on grassland restoration projects.
- Natural enemies and pests
  - Canopy parasitoids: suction sampling (~1 m2, 7 seconds) along transects; specimens identified to species ( Hymenoptera: Parasitica).
  - Ground-dwelling natural enemies: pitfall traps (6 cm diameter, 50% glycol solution) deployed for two 4-day periods.
  - Pest larvae: pest larvae counts from water traps (shallow trays with water) placed during the same periods; sub-samples analyzed in the lab.
  - Taxonomic identification: parasitoids to species where possible; ground beetles (Carabidae), rove beetles (Staphylinidae excluding Aleocharinae), and adult spiders identified to species.
- Data quality and protocols
  - Standardized field and lab data collection protocols; training provided; data entered into MS Access with validation checks.
  - Ethics approval: CLES Penryn Research Ethics Committee (2014/622).

## Data Structure and Files

- Core files and relationships
  - NERCPestNatEnSpeciesList.csv: taxonomic details; links to other datasets via SpeciesCode; includes collection method and gender (for Hymenoptera only).
  - NERCPitfall.csv: pitfall trap data; linking via SampleCode; notes on missing data due to traps being knocked over.
  - NERCSuctionSample.csv: suction sample data; linking via PointCode; notes on data gaps (crop failure in one transect).
  - NERCWaterTrap.csv: pest larvae counts from water traps; linking via SampleCode and SpeciesCode.
  - NERCNatEnLandscapeSurvey.csv: landscape and habitat context data; linking via PointCode and TransectID; includes numerous radii-based and patch metrics (e.g., grassland types, semi-natural habitat, hedge length, plant richness, and various buffer-derived variables).
- Linking and identifiers
  - SpeciesCode, SampleCode, PointCode, TransectID used to join datasets and enable cross-dataset analyses.
  - Rich set of landscape metrics across multiple spatial scales (0.5–3 km radii) and patch-level attributes (nearest patch distances and areas).

## Key Variables and Indicators

- Local plant diversity: margin and in-crop species richness; percent cover of plants; hedge proportion; field margin width and length.
- Landscape context: amount and type of grasslands (species-rich, restoring, improved), semi-natural habitat, arable land within several buffers; metrics for intensive grassland, restored grassland, and species-rich grasslands; proximity and size of grassland patches.
- Natural enemy communities: abundances and taxa from suction samples, pitfall traps, and parasitoid counts; key pest larvae captured in water traps; parasitism indicators (e.g., parasitoid eggs or ectoparasites).
- Field and transect metadata: transect locations, field margins, hedge characteristics, sampling dates, and field-level context (farm and field IDs).

## Data Quality, Limitations, and Provenance

- Data quality
  - Protocols standardised; data entry and validation procedures documented.
  - Missing data notes present for several files (e.g., missing gender data outside Hymenoptera; several pitfall samples missing due to mishaps; field 3.1 transect reduction due to crop failure).
- Limitations
  - Temporal scope limited to 2013–2014; spatial scope limited to the Wessex region.
  - Subsets of data (e.g., water trap sampling) were conducted on a subset of fields.
  - Some taxonomic identifications limited to higher taxonomic levels for certain groups; gender data only recorded for Hymenoptera.
- Data provenance
  - Clear documentation of field collection methods, GIS data sources, and literature references supporting taxonomic identifications.

## Ethics and Access

- Ethical approval: University of Exeter CLES Penryn Research Ethics Committee (2014/622).
- Data are described with file-level metadata and linkage keys to enable re-use within the Wessex BESS WP4 framework and in conjunction with related datasets.

## How to Use and Integrate

- Appropriate for analyses linking plant diversity and landscape context to natural enemy communities and pest dynamics in oilseed rape.
- Can be combined with other Wessex BESS WP4 datasets to build broader ecosystem service and biodiversity assessments.
- Useful for informing data strategy on collection, metadata standards, and cross-dataset linking for data leaders aiming to improve data discoverability, interoperability, and reusability.

## References

- Ferguson, A., et al. (2010). Key Parasitoids of the Pests of Oilseed Rape in Europe: A Guide to Their Identification.
- Joy, N. H. (1932); Lott, D.A. (2009, 2011); Luff, M.L. (2007); Lott & Anderson (2011); Morton et al. (2011); Roberts (1993); Rodwell (1992); Stace (1997); Toynton & Ash (2002); Walker & Pywell (2000).