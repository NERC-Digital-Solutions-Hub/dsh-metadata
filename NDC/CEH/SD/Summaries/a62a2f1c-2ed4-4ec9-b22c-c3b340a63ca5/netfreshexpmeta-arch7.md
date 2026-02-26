# Overview A dataset of stable isotope concentrations (  13 C or  15 N) and community abundance data for stream macroinvertebrate taxa measured during a mesocosm drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK.

## Purpose and scope
- Provides δ13C and δ15N stable isotope data and macroinvertebrate abundance for stream invertebrates.
- Collected to understand how communities and their diets respond to changes in habitat and food availability during a hydrological drought.
- Data are organized to support GIS-based analysis of spatial (across mesocosm blocks) and temporal (Before, During, After) patterns.

## Spatial context and sampling framework
- Location: Llyn Brianne Experimental Observatory, Wales, UK (coordinates provided in text).
- Four mesocosm blocks: Carpenter (Ll6), Davies (Ll7), Hanwell (Ll3), Sidaway (Ll8).
- Each block comprises three cobble-channel mesocosms fed by four upland streams; two fed streams are circumneutral, two acidic.
- Each mesocosm block sampling includes three spatial segments per channel (1–9 total segments across channels in a sampling plan), enabling fine-scale spatial mapping along channels.

## Experimental design
- BACI design: Before-After Control-Impact with 6-month colonisation (Jan–Jul 2023) followed by drought treatments.
- Treatments: 100% baseflow (control), 50% baseflow, 10% baseflow (random block design).
- Sampling timepoints: Before (T0, 20 Jul 2023), During (T1, ~30 days of treatment, 24 Aug 2023), After (T3, ~40 days post-recovery, 9 Oct 2023).
- Replication: 9 samples per channel per timepoint (total 216 samples across the study).

## Sampling and processing protocol
- Macroinvertebrate collection: Hess samplers (165 cm2, 500 μm mesh); nine replicates per timepoint per block/channel, with six preserved in ethanol for taxonomy/dietary analyses and three kept in channel outflow water for gut depuration (24 h) prior to stable isotope work.
- Post-collection handling: live samples stored at ~4–5°C during depuration; samples prepared for taxonomy (family level) and stable isotope analyses.
- Taxonomic identification: families; Chironomidae split into two morphotaxa (filterers and predators) by head morphology.
- Isotope sample processing: depurated individuals freeze-dried, homogenized, weighed into tin capsules, and analyzed via EA-IRMS for δ13C and δ15N.

## Stable isotope analysis and quality control
- Instrumentation: Elemental Analyzer (EA) coupled to IRMS (Conflo III with Delta Plus XP).
- Standards: USGS40 (for both δ13C and δ15N) and USGS41a; USGS40 also used as reference for carbon and nitrogen concentrations.
- Expressed as delta values (δ13C, δ15N) relative to standards.
- Quality control: long-term precision reported for a control standard (e.g., δ13C, δ15N, and total C/N with stated variability); duplicate analyses and outlier checks based on standard deviations.

## Data structure and contents
- Two associated CSV datasheets:
  - netfreshexpsi.csv: Stable isotope data (Site, Treatment, Time, Taxon, δ13C, δ15N, etc.).
  - netfreshexpcomm.csv: Macroinvertebrate community data (Site, Treatment, Time, Segment, Taxon abundances).
- Site coding: mesocosm blocks identified by stream codes (Ll3, Ll6, Ll7, Ll8) with corresponding block names Hanwell, Carpenter, Davies, Sidaway.
- Time categories: Before, During, After (dietary isotopes measured during Before and During periods; community data available for all 3 periods).
- Segment indexing: 1 to 9 along a channel, with Segment 1 at the channel top and Segment 9 at the bottom; each segment is 1 m in length.
- Data organization: rows are individual replicates; columns include mesocosm block, treatment level, timepoint, segment, and taxa-specific measurements.

## Potential GIS applications
- Map spatial variation in macroinvertebrate communities and stable isotope signatures across mesocosm blocks and along channel segments.
- Link hydrological treatment data (flow reductions) with ecological responses for spatially explicit analyses.
- Integrate with environmental layers (pH, baseflow differences, channel geometry) to explore drivers of assemblage structure and trophic dynamics.
- Prepare GIS-ready datasets for visualization of Before/During/After dynamics by block and segment.

## Limitations and considerations for GIS use
- Data are specific to controlled mesocosm environments; extrapolation to natural streams should be performed cautiously.
- Temporal resolution is limited to three key timepoints per block; finer temporal GIS analyses would require additional data.
- Data require careful handling of taxon-level updates (family-level identifications and Chironomidae morphotaxa) when harmonizing with external taxonomic databases.

## References (selected)
- Foundational keys and methodologies for aquatic invertebrates and isotope analysis referenced in the dataset documentation (e.g., Edington & Hildrew; Wallace et al.; Dobson et al.; Durance et al.; Seymour et al.; Oxford/UK references for stable isotope standards).