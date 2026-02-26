# Plant biomass, nutrition, ecosystem carbon fluxes and soil nutrients in common alder growing on home and away soil from Aberdeenshire, Scotland. 2018

## Aim and hypotheses
- Investigates how soil origin (home alder soil, birch family soil, Douglas fir away soil) and associated symbionts (ECT fungi and Frankia) influence alder seedling performance (growth, nutrition) and carbon allocation.
- Uses a 13C pulse-labelling approach to relate seedling nutritional status (leaf N and P) to belowground carbon allocation to fine roots and symbionts.
- Hypotheses include: home soils yield superior seedling performance due to specialist symbionts (positive plant–soil feedback); leaf N linked to Frankia nodulation and belowground C allocation; home soils enhance P content via ECM-mediated P acquisition.

## Experimental design
- Mesocosm setup using intact soil cores collected from three stands (alder, birch, Douglas fir) at Crathes Estate, Aberdeenshire (N=30 cores; 10 per stand).
- For each mesocosm: root-excluding cores included to measure in-growth of fungal mycelium; transplantation of one non-mycorrhizal alder seedling per mesocosm.
- Growth period: 6 months with monthly measurements; climate chamber at 20°C, 14 h light.
- Randomized spatial design within each stand; cores fixed and managed to allow drainage and root exclusion where needed.

## 13CO2 pulse labelling and flux measurements
- Two days before harvest: pulse-labelling with 99 at% 13C-CO2 for 6 hours in a controlled chamber.
- Sampling: leaf tissue collected before labelling and at multiple timepoints after labelling (immediately, then every 12 h up to 48 h) to track 13C incorporation and respiratory losses.
- Soil and root cores used to capture 13C in root-associated respiration via NaOH traps; whole-system CO2 flux measured with LI-COR under light and dark conditions to assess carbon accumulation (negative values = accumulation).
- Leaf tissue used to quantify 13C and 15N; 13C allocation belowground partitioned into fine roots and Frankia nodules.

## Plant and tissue measurements
- Growth metrics: seedling height and leaf number recorded at planting and monthly.
- Biomass: shoots, coarse roots, lateral roots, and fine roots separated and dried (80°C, 48 h) for weighing.
- Functional traits: specific leaf area (SLA) measured; leaf N, C, P analyzed.
- Symbioses: ECM colonization assessed by morphotyping and microscopy; nodulation quantified for Frankia.
- Isotope data: 13C in leaves, fine roots, Frankia nodules; 15N natural abundance in a subset.

## Soil and nutrient analyses
- Nutrient pools measured: total and exchangeable K, Ca, Mg, P, NO3-, NH4+.
- In situ ion exchange membranes used to estimate nutrient supply rates.
- At harvest, soil total C, N, and P measured; pH recorded.
- Data reported per soil origin (Ag = Alnus glutinosa, Bp = Betula pendula, Pm = Pseudotsuga menziesii).

## Molecular and microbial analyses
- ECM fungal community characterized by sequencing ITS1–ITS4 from representative extraradical tips.
- PCR products purified and sequenced; reads processed and compared to UNITE database; representative ECM taxa submitted to GenBank (accessions MT499907–MT499914).

## Data structure and units
- Data organized with rows as replicate cores; columns represent variables.
- Soil origin codes: Ag (Alnus glutinosa), Bp (Betula pendula), Pm (Pseudotsuga menziesii).
- Example variables and units:
  - Biomass, AboveG, BelowG, Coarse_roots, Lateral_roots, Fine_roots: mg dwt
  - C_flux_Bio, C_flux: mg CO2 m-2 h-1 (net CO2 flux)
  - ECM: percent colonization
  - 13C_fixed, d13C_leaves_t1, d13C_fineroots_t4, d13C_Frankia_t4: mg or per mil
  - d13C_NaOH_t1: per mil
  - leafN, leafC, leafP: percent
  - g_core, soilN, soilC, soilP: (units as specified in dataset)
  - 21 days -1 measurements for various minerals (e.g., NO3-, NH4+, Ca, Mg, K, P, Fe, Mn, Zn, S, Pb)
- Additional notes: 21-day timepoint data per core; multiple measurement modalities (CF-IRMS, CRDS, LI-COR) with cross-referencing to calibration standards.

## Data provenance and accessibility
- Isotope and elemental analyses conducted with standardized, calibrated instruments; data linked to landing metrics (biomass, C/N/P, isotope incorporation).
- ECM fungal data and accession details provided; sequences aligned to UNITE with GenBank submissions.
- Data structure supports integrative analyses across plant performance, nutrient status, carbon allocation, and microbial symbiont dynamics, enabling reuse and cross-study comparisons.

## Relevance for data governance and stewardship
- Rich, multi-modal dataset requiring thorough metadata (soil origin, stand location, core replication, measurement methods, instrument settings, sampling times).
- Clear coding for soil origin and standardized units facilitate interoperability and data sharing.
- Documentation of methods and sequencing data enhances reproducibility and provenance; deposition of sequence data in GenBank and reference to UNITE supports long-term accessibility.
- Potential data management needs: versioning of dataset, data quality checks across disparate measurement types, and consistency in unit conventions for reuse across studies.