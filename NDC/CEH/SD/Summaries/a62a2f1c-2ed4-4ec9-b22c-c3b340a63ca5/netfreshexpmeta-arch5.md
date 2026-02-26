# Overview A dataset of stable isotope concentrations ( δ13 C or δ15N) and community abundance data for stream macroinvertebrate taxa measured during a mesocosm drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK.

## Purpose and scope
- Provides linked data on stable isotope concentrations (δ13C and δ15N) and macroinvertebrate community abundances.
- Collected to understand how aquatic communities and their diets respond to habitat and food availability changes during hydrological drought.
- Study site: Llyn Brianne Experimental Observatory, Wales, UK, using a four-mesocosm BACI experiment with different flow treatments.

## Study design and environment
- Experimental setup: Four mesocosm blocks (Carpenter/Ll6, Davies/Ll7, Hanwell/Ll3, Sidaway/Ll8), each with three cobble-channel mesocosms fed by water from four upland streams; two streams circumneutral, two acidic.
- Treatments: Randomized flow reductions to 100% (control), 50%, and 10% baseflow, maintained for ~30 days.
- Design framework: Before-After Control-Impact (BACI); colonisation period of 6 months prior to treatments.
- Sampling timeline:
  - Before (T0): 20 July 2023
  - During (T1): ~24 August 2023 (after ~30 days of treatment)
  - After (T3): ~9 October 2023 (approx. 40 days after recovery to 100% baseflow)
- Channel and sampling details:
  - Hess samplers used; nine replicates per mesocosm channel per time point (three per segment across three segments; total 216 samples).
  - Three “live” samples used for gut-content depuration; six preserved in absolute ethanol for taxonomy, metabarcoding, and macronutrient analyses.

## Data and methods

- Macroinvertebrate community data (netfreshexpcomm.csv):
  - Taxonomic resolution: family level (with morphotaxa for Chironomidae: filterers vs. predators by head capsule morphology).
  - Abundances recorded by taxon per sample.
  - Key columns include Site (Ll3, Ll6, Ll7, Ll8), Treatment (100%, 50%, 10%), Time (Before, During, After), Segment (1–9; 1 = top, 9 = bottom; 1 m segments), and Taxon-specific abundance data.

- Stable isotope data (netfreshexpsi.csv):
  - Isotopes measured: δ13C and δ15N for each taxon per sample.
  - Columns mirror the sampling structure: Site, Treatment, Time, Taxon, and isotope values (d13C, d15N).
  - Samples were prepared by depuration, freeze-drying, homogenization, and weighed into tin capsules; analyzed by EA-IRMS with standard references.

- Data processing and quality controls:
  - Isotope analyses performed at UKCEH (Lancaster) with standards USGS40 and USGS41a; USGS40 used as a reference for both carbon and nitrogen.
  - Long-term QA metrics reported for quality control standards (total C, δ13C, total N, δ15N with specified precision).
  - Data processing conducted with Isodat 2.0.

## Data structure and storage

- File structure:
  - Netfreshexpcomm.csv: Macroinvertebrate community data.
  - Netfreshexpsi.csv: Stable isotope data.
- Data organization:
  - Each row represents an individual replicate; columns encode mesocosm site, treatment, time point, channel segment, and taxon- or isotope-specific measurements.
- Documentation:
  - Table 1 provides column definitions for both datasheets (site codes Ll3, Ll6, Ll7, Ll8; treatment levels; time points; segments; and taxon/isotope data).

## Practical considerations for data stewardship

- Standards and interoperability:
  - Use of delta notation and established taxonomic keys referenced in the document for consistent identification.
  - Clear standard references (USGS materials) and QA procedures to enable cross-study comparability.
- Provenance and traceability:
  - Detailed description of experimental design, mesocosm setup, and sample processing steps to support reproducibility.
- Metadata richness:
  - Comprehensive metadata includes site labeling, flow treatments, sampling times, channel segments, and methods of preservation and isotopic analysis.
- Data governance and lifecycle:
  - Data are organized for easy ingestion into data portals; two complementary datasets (community data and isotope data) are linked via site, time, and taxon identifiers.
  - Documentation supports potential updates, reprocessing, or re-analysis with transparent lineage from field collection to data products.
- Potential limitations to note:
  - Temporal gaps between sampling points (Before, During, After) and the complexity of multiple connected data streams (taxonomy, diet, and isotopes).
  - Some taxa-level data (e.g., Chironomidae morphotaxa) require careful interpretation when combining datasets.

## References and supporting materials

- Taxonomic keys and ecology references used for identifications.
- Methodological references for core aspects of the experiment (BAC I design, mesocosm setup, stable isotope analysis, and data processing).
- Table 1 (described in the dataset) detailing column contents for the two CSV files.