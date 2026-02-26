# A dataset of stable isotope concentrations (  13 C or  15 N) and community abundance data   for   stream   macroinvertebrate   taxa   measured   during  a   mesocosm   drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK.

## Context and Aim
- Purpose: identify environmental health measures to scrutinise and evaluate policy, informing future decisions through monitoring data.
- Focus: how stream macroinvertebrate communities and their diets respond to habitat and food availability changes during a hydrological drought.
- Setting: Llyn Brianne Experimental Observatory, Wales, UK.
- Data types: stable isotope concentrations (δ13C, δ15N) and community abundance data for stream macroinvertebrates.

## Experimental Setup
- Four mesocosm blocks: Carpenter (Ll6), Davies (Ll7), Hanwell (Ll3), Sidaway (Ll8).
- Each block comprises three cobble-channel mesocosms (20 m × 0.2 m × 0.2 m) fed by water from four upland streams.
- Water parameters: two streams circumneutral (pH ~6.8–7.2) and two acidic (pH ~5.3–5.8).
- Baseflow discharge ≈ 1 L s⁻¹; channel flow ≈ 2 m s⁻¹.
- 6-month colonisation prior to treatments (January–July 2023).

## Experimental Design
- BACI design: before-after-control-impact.
- Treatments: 100% baseflow (control), 50% baseflow, 10% baseflow; random block arrangement.
- Flow manipulation via intake valves; maintenance based on water depth and stage–discharge curves.
- Sampling timepoints: Before drought (T0, 20 July 2023), During drought (T1, 24 Aug 2023; ~30 days), After drought (T3, 9 Oct 2023; ~40 days post-recovery to baseflow 100%).
- Post-treatment recovery: all mesocosms returned to 100% baseflow.

## Macroinvertebrate Sampling and Diet Analysis
- Sampling method: Hess samplers (165 cm², 500 μm mesh); nine replicates per channel per time point (three from each of three segments).
- Sample handling: six replicates preserved in absolute ethanol for community composition, metabarcoding, and macronutrient analyses; three samples kept in channel outflow water to depurate gut contents for 24 h (stable isotope analyses).
- Total samples: 216 across the study.
- Taxonomy: identified to family level; Chironomidae morphotaxa (filterers and predators) distinguished by head capsule morphology.
- Data captured: abundances of macroinvertebrate taxa.

## Stable Isotope Analysis
- Preparation: depurated individuals frozen, then freeze-dried and homogenised; weighed into tin capsules.
- Measurement: δ13C and δ15N via Flash EA 1112 → Conflo III → Delta Plus XP IRMS.
- Standards: USGS40 (δ13C and δ15N) and USGS41a; USGS40 also used for carbon and nitrogen concentrations.
- QA/QC: long-term precision reported for C, δ13C, N, and δ15N.
- Data processing: Isodat 2.0.

## Data Structure and Content
- Datasets:
  - netfreshexpsi.csv: Stable isotope data.
  - netfreshexpcomm.csv: Macroinvertebrate community data.
- Organization: replicates as rows; columns identify mesocosm, treatment, replicate, and other metadata.
- netfreshexpcomm.csv
  - Site: mesocosm blocks (Ll3, Ll6, Ll7, Ll8; Hanwell, Carpenter, Davies, Sidaway).
  - Treatment: flow level (100%, 50%, 10% baseflow).
  - Time: Before, During, After drought.
  - Segment: 1–9 (1 at channel top, 9 at bottom; each segment 1 m).
  - Taxa abundance data by macroinvertebrate families.
- netfreshexpsi.csv
  - Site: as above.
  - Treatment: as above.
  - Time: Before and During drought (stable isotopes measured pre- and during-drought).
  - Taxon: resource or macroinvertebrate taxon analyzed for isotopes.
  - d13C, d15N values.
- Data documentation: Table 1 describes column contents.

## Data Quality, Metadata, and Governance
- Metadata structure: explicit data columns and dataset descriptions provided to facilitate interpretation and reuse.
- Data quality: QA/QC procedures described for isotope data; transparent reporting of standards and precisions.
- Data governance considerations: acknowledges potential barriers common to monitoring frameworks (data accessibility, metadata completeness, data sharing, and data transformation needs); data are organized to support transparency and reuse.

## References
- Taxonomic keys and methods referenced (e.g., Edington & Hildrew; Wallace et al.; Dobson et al.).
- Experimental and ecological context literature (e.g., Durance et al.; Seymour et al.; related freshwater invertebrate guides).