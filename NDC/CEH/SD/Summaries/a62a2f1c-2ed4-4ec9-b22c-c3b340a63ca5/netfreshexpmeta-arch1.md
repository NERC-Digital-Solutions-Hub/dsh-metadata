# A dataset of stable isotope concentrations (δ13C or δ15N) and community abundance data for stream macroinvertebrate taxa measured during a mesocosm drought experiment at the Llyn Brianne Experimental Observatory, Wales, UK.

## Aim
- To understand how macroinvertebrate communities and their diets respond to habitat and food availability changes during a hydrological drought.
- To identify patterns in community composition and trophic structure using stable isotope data (δ13C and δ15N) alongside abundance data.

## Setting and experimental design
- Location: Llyn Brianne Stream Observatory, Wales, UK.
- Four mesocosm blocks (Carpenter, Davies, Hanwell, Sidaway) fed by water from four upland streams; blocks differ in pH (two circumneutral, two acidic).
- Mesocosm design: 3 stationary channels per block (20 m × 0.2 m × 0.2 m) with cobble substrate; average channel flow ~2 m/s, baseflow ~1 L/s.
- Experimental design: Before-After Control-Impact (BACI) with 6-month colonisation (Jan–Jul 2023) prior to treatments.
- Treatments: random block design with three flow levels applied to mesocosms — 100% baseflow (control), 50%, and 10% of baseflow.
- Timeline: Sampling before treatments (T0, 20 July 2023), during drought (T1, ~30 days after treatments began, 24 Aug 2023), and after drought (T3, ~40 days after recovery to 100% baseflow, 9 Oct 2023).

## Mesocosm and sampling details
- Mesocosm identification: Carpenter (Ll6), Davies (Ll7), Hanwell (Ll3), Sidaway (Ll8).
- Sampling method: Hess sampler (165 cm², 500 μm mesh) collected nine replicate samples per channel per time point (3 segments per channel; 3 replicates per segment; total nine per channel).
- Sample handling:
  - Six replicates preserved in absolute ethanol for community identification, metabarcoding, and macronutrient analyses.
  - Three replicates stored in channel outflow water to depurate gut contents for 24 hours for stable isotope analyses.
  - Total samples collected across the study: 216.

## Taxonomic and dietary analyses
- Community analysis: Samples preserved in ethanol identified to family level using standard keys; Chironomidae divided into two morphospecies (filterers and predators) by head capsule morphology.
- Stable isotope analysis: Gut-depurated individuals identified to taxa, then frozen, freeze-dried, and homogenized for isotopic measurement.
- Isotope measurements: δ13C and δ15N determined using an elemental analyzer coupled to an isotope ratio mass spectrometer (EA-IRMS). Standards used: USGS40 and USGS41a (L-glutamic acid) with USGS40 as reference for both carbon and nitrogen concentrations.
- Quality control: Long-term precision reported for standard controls (e.g., δ13C ~ -27.78‰, δ15N ~ 5.03‰ with small SDs).

## Data structure and availability
- Data organization: Replicates as rows with columns for mesocosm (Site), Treatment (flow level), Time (Before, During, After), and Segment (1–9). Two associated CSV datasets:
  - netfreshexpcomm.csv: Macroinvertebrate community data (abundances by taxon; includes Site, Treatment, Time, Segment, and taxon abundance columns).
  - netfreshexpsi.csv: Stable isotope data (δ13C, δ15N) by Site, Treatment, Time, and Taxon.
- Metadata notes: Tables describe column contents (e.g., site/mesocosm mapping Ll3, Ll6, Ll7, Ll8; treatments corresponding to 100%, 50%, 10% baseflow; time points and channel segments). Data structure enables linking community composition with isotopic signatures to infer trophic shifts under drought conditions.

## Data processing and references
- Processing: Isodat 2.0 used for isotope data processing; isotope values expressed in delta notation relative to international standards.
- Context: Data are part of the NETFRESH project (WP2 data collection) focusing on the ecological effects of drought on stream communities and their diets.
- References included for methodology and taxonomic keys (e.g., works on freshwater invertebrates, taxa keys for Ephemeroptera, Plecoptera, and Trichoptera, and prior drought/microbial DNA considerations).