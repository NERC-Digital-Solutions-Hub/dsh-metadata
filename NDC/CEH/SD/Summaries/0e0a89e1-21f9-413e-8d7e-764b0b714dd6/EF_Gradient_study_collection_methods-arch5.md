# Vegetation work

- Study collects multi-domain ecological data across sites, including vegetation structure, biomass, soil properties, and greenhouse gas flux, with surface and soil measurements designed for integration and reuse.
- Vegetation data collected via four 50 cm x 50 cm quadrats per site, randomly placed; species presence tracked by visual percent cover; species richness and the percent cover of grasses/forbs are summed across quadrats.
- Biomass harvested by clipping at ground level within each quadrat, dried at 80°C for 24 hours, weighed, and summed to produce site-level biomass (g biomass m⁻²).
- Community metrics include Shannon diversity (Shannon & Weaver, 1963) and Community Weighted Mean (CWM) traits, calculated as CWM = sum(w_i × x_i) over S species, where w_i is relative abundance and x_i is trait value; trait values are taken from established trait databases.
- Trait values used include longevity, plant height, specific leaf area, root architecture, rooting depth class, and VAM affinity, sourced from LEDA, PlantATT, and related trait databases (with cited literature).

## Greenhouse gas flux measurements

- Net ecosystem CO₂ exchange, photosynthesis, and respiration assessed using four soil collars and transparent chambers connected to an infrared gas analyser (EGM-4 IRGA).
- CO₂ fluxes measured in light conditions and after covering chambers to obtain dark measurements; concurrent measurements of soil moisture, soil temperature (WET sensor), and photosynthetically active radiation (PAR) recorded in triplicate.
- Calculations convert 27 CO₂ measurements per chamber visit to CO₂ flux in mg m⁻² h⁻¹; explicit equations reference start time, chamber volume, and chamber area.
- Methane (CH₄), CO₂, and nitrous oxide (N₂O) fluxes obtained by collecting gas samples (9 mL) into evacuated vials at 0, 10, 20, and 30 minutes and analyzing with a Gas-Chromatograph.

## Soil sampling and physical properties

- Six soil samples per site collected with a 4 cm auger to a depth of 10 cm; samples sieved to 2 mm and stored at 5°C until processing.
- Bulk density measured from two cores per site by splitting into 0–5 cm and 5–10 cm depths, drying at 80°C for 48 hours, then calculating mass/volume.
- Soil pH determined by mixing 5 g soil with 5 g water (1:1) and measuring with a pH meter.

## Moisture and nutrient analyses

- Volumetric moisture content determined by drying fresh soil aliquots (5 ± 0.001 g) at 80°C for 48 hours; moisture content calculated from post-dry and wet weights.
- Water extractable N and C: 5 g soil shaken with 25 mL Milli-Q water for 1 hour, filtered; undiluted filtrate analyzed for DIN (NH₄⁺, NO₃⁻, total N) and DOC (via autoanalyser and TOC analyzer); DIN/DOC values adjusted to mg kg⁻¹ using soil moisture and dry weight.
- KCl extractable N and potential mineralisation: 5 g soil with 25 mL 1 M KCl shaken for 1 hour; filtrate analyzed for DIN; moisture-adjusted calculations applied; a separate 5 g sample incubated at 25°C for 14 days to assess mineralisation (NO₃⁻ + NH₄⁺), expressed as g m⁻² day⁻¹.
- Mineralisation calculations involve combining extractable N with bulk density and time.

## Microbial biomass

- Microbial biomass assessed via fumigation-extraction: 5 g soil fumigated (with chloroform) and 5 g unfumigated, then extracted with 25 mL 0.5 M K₂SO₄; extracts analyzed for DIN, extractable PO₄ and dissolved carbon (via TOC-L) at appropriate dilutions.
- Correction factors KE and KEN applied (0.35 and 0.54) to adjust for extraction efficiency and provide microbial biomass estimates.

## Trait data and sources

- Trait values drawn from established plant trait databases and literature:
  - Longevity: ordinal scale (annual to perennial) from LEDA traitbase.
  - Plant height: PlantATT.
  - Specific leaf area: LEDA traitbase.
  - Root architecture: categorical trait ranging from fibrous to tap roots (multiple categories).
  - Rooting depth class: ordinal with three levels.
  - VAM affinity: ordinal scale (usually/mycorrhizal to never mycorrhizal).
- Trait references include Diaz et al. (2007), Grime et al. (2007), Hill et al. (2004), Kleyer et al. (2008), and related trait databases (PlantATT, LEDA).

## Data governance and documentation for Data Stewards

- The document provides explicit measurement protocols, instruments, and calculation methods, facilitating data provenance, reproducibility, and standardization across datasets.
- Derived metrics (e.g., CWM, CO₂ flux, mineralisation rates, microbial biomass) are defined with calculation formulas, supporting consistent data processing and quality checks.
- References and trait sources are listed, enabling traceability of inputs and trait values used for analyses.
- The breadth of data (vegetation structure, GHG flux, soil chemistry, microbial biomass, and trait data) implies a need for integrated metadata to maintain compatibility across datasets and long-term reuse.

## Challenges and considerations for Data Stewards

- Integration of diverse data types and formats from vegetation, gas flux, soil chemistry, and microbial analyses.
- Ensuring consistent units, measurement timings, and calibration records across methods (IRGA, GC, autoanalyser, TOC).
- Managing metadata richness to support reuse (methods, instruments, environmental conditions, and trait sources).
- Handling potential data gaps and updates across sampling events and site replications.
- Maintaining alignment with trait databases and literature references to support robust ecological analyses.

## References and trait sources

- Díaz et al. 2007; Fitter & Peat 1994; Grime et al. 2007; Hill et al. 2004; Kleyer et al. 2008; Shannon & Weaver 1963; and related plant trait and ecological literature.