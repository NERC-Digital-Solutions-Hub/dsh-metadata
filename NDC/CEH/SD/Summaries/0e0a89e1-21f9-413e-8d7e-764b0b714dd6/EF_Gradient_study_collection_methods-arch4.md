# Vegetation work

- Focuses on field and lab measurements to characterise vegetation, soil properties, and greenhouse gas flux, with derived metrics for ecological analyses.
- Data used to compute community-level trait statistics (e.g., community weighted mean traits) and to support ecosystem function assessments.

## Vegetation data collection and metrics

- Four random quadrats of 50 cm x 50 cm each are used to assess vegetation.
- Visual estimation of percentage cover for each species within quadrats.
- Species richness and percent cover of grasses and forbs are summed across the four quadrats.
- Biomass is harvested by clipping at ground level from each quadrat, dried at 80°C for 24 hours, and weighed; sums across the site yield total biomass (g m^-2).
- Diversity metric: Shannon's Diversity index calculated (Shannon & Weaver, 1963).
- Functional data: Community weighted mean (CWM) traits calculated using species abundance and trait values (Díaz et al. 2007); trait values are sourced from established databases (e.g., LEDA Traitbase, PlantATT).

## Greenhouse gas flux measurements

- Net ecosystem CO2 exchange, photosynthesis, and respiration are measured using:
  - Four plastic collars (25 cm diameter) embedded in soil.
  - Transparent chambers attached to an infrared gas analyser (EGM-4 IRGA); CO2 influx measured over 2 minutes, followed by a measurement with a reflective cover to obtain dark efflux.
  - Concurrent measurements of soil moisture, soil temperature, and PAR (in triplicate).
- Calculations convert raw CO2 measures to flux (mg CO2 m^-3 over time; final flux reported as mg CO2 m^-2 h^-1) using chamber volume, area, and time-based changes.
- Methane (CH4), CO2, and nitrous oxide (N2O) are sampled with reflective-covered chambers; 9 mL air samples collected at 10, 20, and 30 minutes, analyzed by Gas Chromatograph (GC).
- Final gas concentrations are calculated using the same approach as CO2 for IRGA data.

## Soil sampling and processing

- Six soil samples per site collected with a 4 cm width auger to 10 cm depth (as far as possible).
- Soil passed through a 2 mm sieve to remove stones and roots and stored at 5°C until processing.

## Bulk density and basic soil properties

- Bulk density measured from two cores per site, split into 0–5 cm and 5–10 cm depths; dried at 80°C for 48 hours and weighed.
- pH determined by mixing 5 g soil with 5 ml Milli-Q water (1:1) and measuring with a pH meter.

## Volumetric moisture and nutrient analyses

- Volumetric moisture content: 5 ± 0.001 g of fresh soil dried at 80°C for 48 hours; moisture calculated from pre/post-drying weights.
- Water extractable N and C:
  - 5 g fresh soil shaken with 25 mL Milli-Q water for 1 hour; filtered.
  - Filtrate analysed for DIN (NH4+, NO3-, total N) and DOC using autoanalyser and TOC analyser; values adjusted for soil moisture.
- KCl extractable N and potential mineralisation:
  - 5 g fresh soil with 25 mL 1M KCl, shaken 1 hour; filtrate diluted and analysed for DIN.
  - A second 5 g sample incubated at 25°C for 14 days, then extracted and analysed similarly.
  - Mineralisation calculated as (NO3 + NH4) × bulk density ÷ days.
  
## Microbial biomass assessment

- Fumigation-extraction method:
  - 5 g soil fumigated with chloroform in a desiccator; after 24 hours, nutrients extracted with 25 mL 0.5 M K2SO4.
  - Extracts analysed for DIN, PO4, and dissolved organic carbon (DOC) at appropriate dilutions.
  - Values adjusted for moisture; KE (0.35) and KEN (0.54) quotients used to correct extraction efficiency.

## Trait data and sources

- Trait values used:
  1) Longevity (ordinal; annual to perennial) from LEDA Traitbase.
  2) Plant height (cm) from PlantATT.
  3) Specific leaf area (SLA) from LEDA/PlantATT sources.
  4) Root architecture (categorical; from tap roots to fibrous) per Grime et al. (2007).
  5) Rooting depth class (ordinal; shallow to deep).
  6) Vesicular-arbuscular mycorrhizal (VAM) affinity (ordinal: usually/sometimes/never mycorrhizal).
- Trait sources include Díaz et al. (2007), Hill et al. (2004), Grime et al. (2007), and broader plant trait databases (LEDA, PlantATT).

## Calculations and references

- Calculations for CWMs, CO2 fluxes, mineralisation, and other metrics follow the formulas and methods cited (e.g., Díaz et al. 2007; Shannon & Weaver 1963; Grime et al. 2007; Hill et al. 2004; LEDA/PlantATT databases).
- References provided for trait and methodological context, including ecological trait databases and standard trait compilations (Díaz et al. 2007; Hill et al. 2004; Grime et al. 2007; Kleyer et al. 2008; Shannon & Weaver 1963).

## Data management implications for Data Leaders

- Data types span vegetation surveys, biomass, diversity metrics, GHG flux data, soil chemical and physical properties, and microbial biomass measurements.
- Key data governance needs:
  - Clear unit conventions, measurement protocols, and timing to ensure consistency across sites and years.
  - Detailed metadata capturing methodology, equipment, and calculation steps (especially for flux calculations and CWMs).
  - Sourcing and provenance for trait values; documentation of traitdb references and versioning.
  - Data discoverability and discoverable formats to support broader use within networks and collaborations.
  - Versioning and updates to reflect re-analyses or methodological refinements; alignment with community data standards.
- Potential challenges highlighted by the broader archetype perspective:
  - Fragmented data sources and heterogeneous data types requiring harmonised metadata.
  - Access to comprehensive trait data and ensuring up-to-date references for trait values.

## References

- Díaz, S.; Lavorel, S.; de Bello, F.; Quétier, F.; Grigulis, K.; Robson, M. 2007. Incorporating plant functional diversity effects in ecosystem service assessments. Proceedings of the National Academy of Sciences.
- Fitter, A.H. & Peat, H.J. 1994. The Ecological Flora Database.
- Grime, J.P.; Hodgson, J.C. & Hunt, R. 2007. Comparative Plant Ecology: A functional approach to common British species. 2nd Ed.
- Hill, M.O.; Preston, C.D. & Roy, D.B. 2004. PLANTATT - Attributes of British and Irish Plants.
- Kleyer, M. et al. 2008. The LEDA Traitbase: a database of life-history traits of the Northwest European flora.
- Shannon, C.E. & Weaver, W. 1963. The Mathematical Theory of Communication.