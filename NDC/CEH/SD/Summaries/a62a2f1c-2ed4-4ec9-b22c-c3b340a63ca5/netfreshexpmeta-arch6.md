# Overview A dataset of stable isotope concentrations (  13 C or  15 N) and community abundance data for stream macroinvertebrate taxa measured during a mesocosm drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK.

- Purpose: Understand how aquatic macroinvertebrate communities and their diets respond to habitat and food availability changes during hydrological drought.
- Study system: Mesocosm drought experiment conducted at the Llyn Brianne Experimental Observatory, Wales, UK.

## Experimental design and setup

- Mesocosms and blocks
  - Four mesocosm blocks: Carpenter (Ll6), Davies (Ll7), Hanwell (Ll3), Sidaway (Ll8).
  - Each block contains three cobble-channel mesocosms fed by water from four upland streams; average channel flow ~2 m s-1 with 1 L s-1 baseflow.
  - Streams differ in pH: Ll6 and Ll7 circumneutral (pH 6.8–7.2); Ll3 and Ll8 acidic (pH 5.3–5.8).
- Treatments and design
  - Before-After Control-Impact (BACI) design with random block assignment.
  - Treatments: 100% baseflow (control), 50% baseflow, and 10% baseflow maintained throughout the drought period.
  - 6-month colonisation period prior to treatments (Jan–Jul 2023).
- Sampling timeline
  - Before drought (T0): 20 July 2023
  - During drought (T1): ~30 days after treatment initiation, 24 August 2023
  - After drought recovery (T3): ~40 days after return to 100% baseflow, 9 October 2023
- Sampling design
  - Each channel sampled at three segments (1–9 along the 1 m segments) with nine replicate samples per channel (triplicate samples from each of three segments).
  - Across the study: 216 samples collected.
  
## Sampling and analyses

- Macroinvertebrate sampling
  - Method: Hess samplers (165 cm2, 500 μm mesh); nine replicates per channel per time point (three segments × three replicates per segment).
  - Sample handling: six replicates preserved in absolute ethanol for community, dietary metabarcoding, and macronutrient analyses; three samples kept in channel outflow water for gut depuration (24 h) for stable isotope analyses.
  - Taxonomic resolution: identification to family level; Chironomidae morphotaxa (two groups: filterers and predators) by head capsule morphology.
- Stable isotope analysis
  - Gut depuration followed by freeze-drying of invertebrates; tissues ground and weighed into tin capsules.
  - Isotopes measured at UKCEH (Lancaster) using an elemental analyzer (EA) coupled to an IRMS.
  - Isotopes: δ13C and δ15N; standards: USGS40 and USGS41a (L-glutamic acid) for both isotopes; USGS40 also used as reference for C and N concentrations.
  - Quality control: long-term precision reported for reference material (e.g., δ13C, δ15N, total C, total N); analytical replicates included.
- Data processing
  - Data processed with Isodat 2.0; delta notation used for isotope values.
  
## Data structure and files

- Data files (two CSVs)
  - netfreshexpsi.csv — Stable isotope data
    - Site: Mesocosm block (Ll3, Ll6, Ll7, Ll8) or block name (Hanwell, Carpenter, Davies, Sidaway)
    - Treatment: 100%, 50%, 10% baseflow
    - Time: Before (T0) and During/After drought (T1; only Before and During for isotope data)
    - Taxon: Taxon from which δ13C and δ15N were measured
    - d13C: δ13C value
    - d15N: δ15N value
  - netfreshexpcomm.csv — Macroinvertebrate community data
    - Site: As above
    - Treatment: As above
    - Time: Before, During, After drought
    - Segment: Channel segment (1–9; 1 is the top, 9 is the bottom)
    - Taxon: Macroinvertebrate taxa abundance (abundances for taxa from Chironomidae through Odontoceridae)
- Data organization
  - Each row represents an individual replicate; columns indicate mesocosm, treatment, time, segment, and taxon-specific measurements (abundances or isotope values as appropriate).

## Considerations and references

- Context and prior work
  - References include methodological keys and prior reports on freshwater invertebrates and mesocosm experiments, as cited in the document (e.g., works by Edington & Hildrew, Wallace et al., Dobson et al., Durance et al., Seymour et al., etc.).
- Usability notes for data use
  - Data are arranged to enable self-service analysis of community structure and trophic information across flow treatments and timepoints, with clear mappings for site, treatment, time, and spatial segmentation.
  - The isotopic data allow linking taxa to dietary shifts under drought conditions and can be integrated with abundance data for ecosystem interpretation.