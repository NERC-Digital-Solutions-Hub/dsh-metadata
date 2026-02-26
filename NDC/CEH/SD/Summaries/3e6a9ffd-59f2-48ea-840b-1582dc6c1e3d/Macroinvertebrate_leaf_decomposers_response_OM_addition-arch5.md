# Macroinvertebrate leaf decomposers of Welsh upland rivers in response to organic matter addition

## Purpose and scope
- Document a BACI (before-after-control-impact) study assessing how added leaf litter influences macroinvertebrate assemblages in Welsh upland rivers.
- Compare upstream reference zones with downstream experimental zones across eight streams.
- Capture both field manipulation details and organismal response data to support reuse and re-analysis.

## Experimental design and timeline
- Structure: Each stream has an upstream reference (control) zone and a downstream experimental zone, separated by 20–50 m.
- Before period (T1): 61–65 days (early Nov 2012 to early Jan 2013); no manipulation; zones treated equivalently.
- After period (T2): 57–62 days (early Jan 2013 to Mar 2013); experimental zone receives leaf litter additions.
- Leaf litter: Proportional 1-tonne bags (oak, birch, alder) placed above the experimental zone; additional 630 kg added after two storm events (Feb–Mar 2013).
- Mesh bags: Nylon bags (10 x 15 cm) with 500 µm (fine) and 5 mm (coarse) apertures; each bag contains ~5 g air-dried leaves.
- Replication: 48 mesh bags (24 reference, 24 experimental) per mesh type across 8 streams.
- Collection points: Bags collected and replaced at T1; half of bags retrieved at T2; remaining bags retrieved ~18 weeks after T1 (T18) for a total of 18-week and 2–week post-manipulation observations.

## Data collection and processing
- On-site preservation: Leaves in 70% ethanol; labelled codes; transported to the lab.
- Laboratory processing: Leaf material rinsed (250 µm sieve) and air-dried; macroinvertebrates separated and identified to species where possible; some taxa (e.g., Chironomidae, Tipulidae, Limoniidae, Pediciidae, Oligochaeta, Limnephilidae) identified at coarser taxonomic levels.
- Field and lab instrumentation: Standard field collection and a microscope for identification.
- Metadata and provenance: Includes site-level context and sampling periods; supporting site description data provided.

## Data structure and content
- Bag data (10 columns):
  - site_code: sampling site identifier
  - region: stream basin
  - date: sampling date
  - time: Before/After manipulation indicator
  - landuse: basin land-use
  - reach: Experimental or Control site designation
  - Replicate: A-F (within weeks T1, T2, T18)
  - BagMesh: fine or coarse mesh type
  - taxon_name: lowest resolvable taxonomic name
  - abundance: count of individuals per taxon
- Site Description (supporting file, 10 columns):
  - Site_code: site identifier
  - Name: site name
  - Eastings/Northings: British National Grid coordinates
  - Grid: grid reference
  - Latitude/Longitude: GPS coordinates
  - Elevation: metres above sea level
  - Survey: campaign name
  - Catchment: river catchment

## Data quality, limitations, and notes
- Taxonomic resolution varies; some taxa reported at genus/family/coarse levels when species-level ID not possible.
- Quality control details are not explicitly described; standard lab and field protocols applied (density and temporal replication captured via T1/T2/T18 and A–F replicates).
- Data are time-bounded (Nov 2012–Mar 2013) and location-specific (Welsh upland streams); cross-study interoperability requires harmonized taxon nomenclature and consistent metadata.

## Governance and reuse considerations for Data Stewards
- Ensure clear metadata mapping: harmonize site codes, reach designation (Experimental vs Control), Replicate labeling, and time point nomenclature (T1, T2, T18).
- Maintain data provenance: link bag data to corresponding site descriptions and collection periods; preserve original units (abundance per taxon per bag) and mesh type.
- Data formats and accessibility: store as structured tabular data (CSV/TSV) with accompanying metadata file; provide readme detailing methods, taxonomic resolution, and sampling timeline.
- Licensing and access: attach explicit data usage license; consider DOIs for data subsets; include notes on any embargoes or data-sharing restrictions.
- Data quality improvements: implement basic quality checks (taxon name standardization, validation of replicate codes, date formats) and capture any methodological deviations.
- Documentation for reuse: reference the BACI design assumptions, leaf litter manipulation details, and sampling schedule to facilitate secondary analyses (e.g., decomposition rates, community responses, habitat associations).

## Practical implications for potential data users
- Enables analysis of how organic matter inputs influence stream invertebrate communities over time and across controlled vs. manipulated habitats.
- Provides both organismal data (taxon-level abundances) and geospatial context (site coordinates, catchments) for spatial analyses.
- Suitable for meta-analyses on leaf litter processing and aquatic food webs, provided taxonomic resolution is accounted for.