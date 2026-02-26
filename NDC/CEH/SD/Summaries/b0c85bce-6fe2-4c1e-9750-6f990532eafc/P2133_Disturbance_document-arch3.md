# Plant and soil animal diversity measurements from a disturbance and nitrogen addition experiment in an upland grassland site [NERC Soil Biodiversity Programme] Cole, L., Bardgett, R.D., Buckland, S.M. and Burt-Smith, G.

## Purpose and scope
- Document for a field experiment within the NERC Soil Biodiversity Thematic Programme (1999–) aimed at understanding soil biota biodiversity and functional roles.
- Focuses on plant and soil microarthropod diversity, linked to aboveground productivity and community composition.
- Data describe abundance of soil mites and Collembola, and aboveground plant biomass across a disturbance and nitrogen addition gradient.

## Study site and experimental design
- Location: Sourhope, Cheviot Hills, Southeast Scotland, UK (55°28′30″N, 2°14′W); upland semi-improved grassland, ~350 m altitude.
- Site description: humic brown soil (Sourhope series), average annual rainfall ~1117 mm.
- Experimental layout: five blocks; within each block five replicated experimental areas (3 m × 3 m).
- Treatments: a crossed, continuous gradient of nitrogen addition (0, 60, 120, 180, 240 kg N ha−1) and disturbance (0%, 25%, 50%, 75%, 100% ground cover disturbed), arranged in a 25-subplot matrix per area.
- Implementation: nitrogen applied Feb 2000 and Apr 2001; disturbance simulated by soil disruption using a cross-blade implement to 10 cm depth.

## Treatments and sampling
- Plant sampling: conducted Aug 2000 and Aug 2001 using point quadrats; diversity metrics calculated (Shannon Wiener index H, evenness J, cumulative richness R).
- Functional diversity: indices for predatory vs. non-predatory mites; diversity of microarthropods calculated overall and by group (mites, Collembola).
- Aboveground biomass: plots clipped to 6 cm height; biomass oven-dried at 70°C for 1 week.
- Soil sampling: three cores per 0.5 m^2 plot (0–5 cm depth) for 2000 and 2001; microarthropods extracted via Tullgren funnels (96 h); counts of total mites and Collembola; species-level data where available (2001) with taxonomic references.

## Data and structure
- Datasets (structured as comma-separated values):
  - Dataset 1047: Matrix plant species abundance data, 2000 (P2133_MATRIX_SURVEY2000.csv)
    - Fields include SAMPLING_DATE, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT, etc.
  - Dataset 1048: Matrix plant species abundance data, 2001 (P2133_MATRIX_SURVEY2001.csv)
    - Similar fields with YEAR and updated sampling dates.
  - Dataset 1045: Microarthropod species abundance, 2001 (P2133_MATRIX_MPOD_SPECIES.csv)
    - Fields include YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, SPECIES, COUNT.
  - Dataset 1045: Matrix plant MPOD data (P2133_MATRIX_PLANT_MPOD.csv)
    - Includes above-ground biomass (PLANT_BIOMASS), MITES, COLLEMBOLA counts; fields for YEAR, BLOCK, MAIN_PLOT, MATRIX_POSITION, DISTURBANCE, NITROGEN, and sampling methods.
- Quality and governance:
  - Data validated with numeric range, formatting, and logical integrity checks.
  - QA performed by the data providers; NERC cannot guarantee accuracy or fitness for a particular use; data shared with no liability from NERC.
- Access context:
  - Supporting information available via the SOURHOPE FIELD DATA HANDBOOK (2003); related methodological and contextual references include Usher et al. (2006) and related citations.

## References and notes
- Core background and methodology sources listed, enabling researchers to understand context, sampling design, and taxonomic references (Hopkin 2000; Krantz 1978; Begon et al. 1996; Burke & Grime 1996).
- Data usage notes emphasize data provenance, sampling protocols, and the necessity to consult accompanying handbooks for full metadata and data lineage.