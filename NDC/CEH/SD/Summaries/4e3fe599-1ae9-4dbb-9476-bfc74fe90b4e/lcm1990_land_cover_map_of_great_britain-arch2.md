# Land Cover Map of Great Britain

## Overview
- Digital land cover dataset for Great Britain produced in 1990 from Landsat Thematic Mapper data.
- Classifies land cover into 25 target classes at 25 m resolution; includes sea, inland waters, bare ground, vegetation, and various land-use types.
- Aimed at supporting planning, management, monitoring, and policy evaluation across agriculture, ecology, conservation, forestry, water, urban development, transport, recreation, and more.
- Stand-alone 25 m data and 1 km summary data (17 key classes) available; data can be licensed for various uses.

## Data Characteristics
- Spatial resolution: 25 m (with some features detected down to ~0.125 ha; effective map-able minimum often around 1 ha).
- Source: Landsat TM imagery; classifications produced with supervised maximum likelihood methods; improved accuracy using combined summer and winter images.
- Coverage: Near-complete Great Britain; minimal cloud-related gaps (0.4% cloud-covered areas on both seasons; offshore islands account for ~0.1% missing).
- Unclassified areas: About 2% of Britain labeled as unclassified (code 0) in the 25 m data; represented in 1 km data as the difference to 100% when summing 17 key classes.

## Classification Scheme
- 25 target classes (labels A–Q) plus UNCLASSIFIED (0).
- Categories include: Sea/estuary, Inland water, Coastal bare ground, Saltmarsh, Grass heath and dune grass, Pasture/meadow/amenity grass (with two subtypes: mown/grazed turf and meadow/verge/semi-natural), Marsh/rough grass, Grass/shrub heath (open), Bracken, Deciduous/Mixed wood (scrub/orchard and deciduous woodland), Coniferous/evergreen woodland, Bogs (upland and lowland), Tilled land, Suburban/rural development, Urban development, Inland bare ground, Felled forest, Ruderal weed, and Open shrub heath.
- 1 km data (17 key classes) provides per-cell percentages for each key class, enabling analysis at a coarser scale.
- Descriptions emphasize ecological meaningfulness and consistency across Britain; some regional variation and spectral ambiguity may occur, especially for grasslands and transitional mosaics.

## Data Quality, Accuracy, and Assessment
- Overall accuracy: Realistic assessment around 80–85% when accounting for definitional differences and temporal change.
- Validation notes: Comparisons with ground truth show variations due to differing class definitions and timing; accuracy is influenced by boundary pixels and mis-registration as well as natural landscape change between dates.
- Boundary effects: About 40% of pixels border vector boundaries; excluding boundary pixels increases apparent accuracy to about 71–82% depending on inclusion of boundaries.
- Ground-truth challenges: Field and satellite classifications use different definitions (e.g., bogs vs. wet moorlands), affecting direct comparability.
- Users should interpret accuracy as an average error rate with local variation; real-world accuracy can vary by region and class.

## Data Products and Access
- 25 m target-class data: single-layer dataset with values 0–25 representing the 25 target cover-types.
- 1 km summary data: 17 layers (one per key class); values are integer percentages representing the proportion of each 1 km cell occupied by that key class.
- Licensing and licensing options: Data supplied under Licence with multiple licensing models (single-user to corporate multi-site); pricing bands include commercial, non-commercial, and research uses; discounts may apply for UK academics.
- Availability: Data can be ordered for specific areas; contact CEH Wallingford for licensing and data delivery; data is distributed via the Countryside Information System data downloads.
- Documentation and support: Notes and guidance provided to aid interpretation; a Data Assessment Report (DAR) form accompanies data for user feedback and good-practice guidance.

## Usage and Applications
- Suitable for planning, management, and monitoring in sectors such as agriculture, ecology, conservation, forestry, water resources, urban planning, transport, telecommunications, recreation, and mineral extraction.
- Example applications include: detecting land cover changes, mapping bracken for health studies, environmental assessments of infrastructure projects, and planning of telecommunication lines.
- The dataset supports broad, standardized environmental monitoring and policy performance assessment over time.

## Related Updates and Access to Future Data
- Land Cover Map 2000 is available as a follow-on product; sample data and download options are described on the Countryside 2000 website.
- Contact: Land Cover Map Sales, CEH Wallingford (spatialdata@ceh.ac.uk; +44 (0)1491 692315).

## Practical Considerations for Analysts
- LCMGB1990 maps land cover (not land use); dominant cover at imaging time governs classification.
- Accuracy reflects dataset design and class definitions; use caution when interchanging classes or comparing with non-standard definitions.
- Data can be integrated with other spatial datasets to enhance monitoring value; licensing facilitates access and reuse across organizations.