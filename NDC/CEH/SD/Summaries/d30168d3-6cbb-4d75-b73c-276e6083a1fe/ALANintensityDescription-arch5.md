# Abstract

- The dataset comes from the NERC project NE/N001672/1, investigating the effects of artificial light at night on multi-trophic population dynamics.
- Data include direct observations of insects and plants from field and laboratory experiments, measuring insect numbers, plant biomass, parasitoid attacks, and parasitoid behavior under varying light intensities.
- Experimental setup combines field mesocosms and controlled-temperature laboratory conditions at the University of Exeter (Penryn Campus, UK). The field experiment began on 29 July 2016 and ran for nine weeks; additional experiments were conducted between summer 2016 and spring 2018.
- Researchers: Dirk Sanders, Kevin J. Gaston, and F.J. Frank van Veen (University of Exeter).

## Experimental design and scope

- Field experiment using a randomized block design (6 blocks) with artificial light at night as the treatment.
- Treatments include a control (no light) plus white LED light at 0.1, 1, 5, 10, 20, 50, and 100 lux (plant-height level).
- 48 mesocosms (cages) each containing experimental plant–insect communities; plant species: broad bean (Vicia faba) and barley (Hordeum vulgare).
- Aphid community: three species (Aphis fabae, Acyrthosiphon pisum, Megoura viciae) with winged and unwinged morphs; parasitoids: Lysiphlebus fabarum, Aphidius ervi, Aphidius megourae.
- Linkages among species via a generalist parasitoid, Praon dorsale, attacking multiple aphid species.
- Data collection: weekly counts of all species on all or half of the plants from week 1 through week 9.
- Plant biomass (dry weight) measured at the end of the field experiment (48 mesocosms) after processing (cutting, washing, drying at 50°C for 48 hours).
- A separate experiment measured plant biomass without aphids across 30 mesocosms (4 two-week-old broad beans per mesocosm) over 3 weeks.
- Parasitoid attack-rate experiments and behavioral tests conducted under various light conditions.

## Datasets and contents

- Eight different files cover: insect population dynamics, plant biomass with and without insects, and parasitoid behavior/attack rates under different lighting.
- Key variables and coding schemes include:
  - ab.factor (sampling intensity per cage when counting organisms)
  - Block, Treat.lux, Light.lux (block and light treatment identifiers)
  - M.v, M.v.w, A.p, A.f, A.f.w, S.a, S.a.w (counts for aphids and their winged forms)
  - L.f, A.e, A.m, P.dor.m, P.dor.a, P.dor.s (counts for parasitoids and their mummy status)
  - Plantbiomass.g (dry plant biomass in grams)
  - Hostdensity, Aphid.mummies, and light-related exposure variables (Light.Dark, First)
  - Parasitioid distribution within cages (Parasitoid.on.plant, Parasitoid.on.side.of.cage, Parasitoid.ceiling)
- Data collection spanned both field and laboratory contexts, detailing experimental setups and measurement timings.

## Data quality, provenance, and governance

- Quality control performed after data entry: variables checked for errors and cross-validated against hard-copy records.
- Documentation includes explicit descriptions of experimental designs, species involved, treatment levels, and measurement methods.
- Data are prepared with explicit metadata: names, units (e.g., lux for light, grams for biomass), and coding for missing/partial counts (e.g., ab.factor).
- Contact to primary investigators for provenance and reuse: Dirk Sanders, University of Exeter (d.sanders@exeter.ac.uk), with co-authors Kevin J. Gaston and F.J. Frank van Veen.

## Data structure and metadata considerations for reuse

- Data are organized into eight files capturing:
  - Insect population dynamics (aphids and parasitoids)
  - Plant biomass data from field and insect-free experiments
  - Parasitoid behavior and attack rates under different light intensities
- Variables are systematically named and documented to enable reproducibility and cross-study comparisons.
- The dataset uses a consistent, structured scheme for mesocosm identity (1-48) and block/treatment mappings, supporting downstream data integration.
- The documentation notes missing plant biomass data due to loss of labels; this is a known limitation for downstream analyses.

## Access, sharing, and data stewardship implications

- The data are described in detail to facilitate reuse, with explicit notes on experimental design, measurement protocols, and data structure.
- Data stewardship best practices evidenced by:
  - Clear data dictionaries and variable mappings
  - Versioned design descriptions (field and lab experiments, multiple light treatments)
  - Plans to upload to relevant data portals and catalogue holdings
- For data stewards, this dataset provides a model for:
  - Publishing-ready data with comprehensive metadata
  - Guidance for data creators on standardizing naming conventions, units, and provenance
  - Documentation of data limitations and missing values to inform future updates or re-collection

## Limitations and data management considerations

- Notable limitation: missing plant biomass data in the field experiment due to loss of labels; users should account for this gap in analyses relying on biomass measurements.
- Some experiments used alternate light-treatment schemas (e.g., treatments mentioned as 0, 0.1, 5, 20, 100 lux in specific tests), so users should verify exact treatment mappings per file.
- The dataset spans multiple interconnected experiments (field and laboratory) with potentially differing sampling schedules; careful alignment of time points is recommended for integrated analyses.

## How this aligns with the Data Steward archetype

- Demonstrates effective data governance: well-documented experimental design, measurement methods, and data structure with clear provenance.
- Provides a usable, publishable dataset suitable for discovery and reuse by others studying multi-trophic interactions under artificial light.
- Highlights practical data stewardship activities: quality control, metadata richness, data curation across multiple formats and contexts, and plans for data sharing and portal deposition.
- Emphasizes user-centric considerations by detailing what was measured, how, and under what conditions, enabling researchers to understand scope, limitations, and applicability.