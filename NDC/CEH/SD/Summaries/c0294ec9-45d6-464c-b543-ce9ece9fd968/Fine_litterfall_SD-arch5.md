# AFEX Experiment

## Location and Climate
- Conducted at the AFEX (Amazon fertilization Experiment) area within the BDFFP/INPA, ~80 km north of Manaus, Brazil (02°25' S, 59°43' W).
- Area features plateau topography (80–160 m a.s.l.), steep slopes, and valleys.
- Climate: mean ~26.7°C; annual rainfall 1900–3500 mm with a peak in April (>300 mm/month) and a dry period June–October (<100 mm/month); relative humidity 75–92%.

## Experimental Design
- Full factorial nutrient addition experiment (AFEX) with eight treatments: untreated control; N; P; cations (K, Mg, Ca); and combinations N+P, N+Cations, P+Cations, N+P+Cations.
- 4 replicates per treatment across 4 independent blocks (≥250 m apart).
- Total: 32 plots, each 50 m × 50 m; central study area per plot 30 m × 30 m to maximize litter from within-plot trees.
- Nutrient application: dry granules three times/year with rates of N 125 kg ha⁻¹ yr⁻¹ (urea), P 50 kg ha⁻¹ yr⁻¹ (triple superphosphate), Ca 50 kg ha⁻¹ yr⁻¹, Mg 20 kg ha⁻¹ yr⁻¹ (dolomitic limestone), K 50 kg ha⁻¹ yr⁻¹ (potassium chloride).

## Litterfall Sampling and Nutrient Analysis
- Litter production measured with five traps per plot (50 cm × 50 cm) located 1 m above ground; total trap area per plot 1.25 m².
- Use 1 mm mesh polyethylene screens to capture senesced leaves.
- Litter collected biweekly for two years, dried at 65°C, and weighed (precision 0.01 g) to determine dry biomass (g per plot).
- Post-collection sorting into fractions: leaves; woody material (<2 cm diameter); reproductive material (flowers, fruits, seeds); insect frass and other residues.
- Leaves not identified to species; data presented as plot-level means.

## Data Structure and Variables (Data to be Managed)
- Experimental identifiers: plot ID, treatment, block, replicate.
- Temporal coverage: biweekly collections over two years; collection dates recorded per sample.
- Measurements: total litter biomass per trap/plot (g), biomass per fraction (leaves, woody material, reproductive material, other), potentially aggregated to g m⁻².
- Nutrient input records: dates and amounts of N, P, K, Ca, Mg applications per plot.
- Spatial metadata: plot coordinates within the study area.

## Data Governance and Stewardship Considerations
- Ensure standardized metadata: units (grams, kilograms, m²), date formats, measurement methods (drying temperature, balance precision), and fraction definitions.
- Data quality assurance: verify consistent trap placement, complete biweekly collections, and alignment of biomass with corresponding nutrient treatments.
- Documentation of data processing steps (e.g., how fractions are combined, any corrections applied) and data dictionaries.
- Data storage and sharing: prepare datasets for portal/upload with clear accession IDs, versioning, and traceability to field notes and lab measurements.

## Challenges and Considerations for Data Stewards
- Aligning diverse data streams (biomass, fractions, nutrient inputs) across 32 plots and 4 blocks over two years.
- Ensuring completeness and timeliness of data collection (biweekly cadence) and accurate linking of samples to treatments and plots.
- Handling non-identification of leaf species and potential need for species-level data in future analyses.
- Managing potential interoperability issues across systems or formats if integrating with other ecological datasets.
- Supporting data consumers with clear context on experimental design, measurement methods, and seasonal influences on litter production.

## Temporal and Spatial Coverage
- Temporal: biweekly litter collections over a two-year period starting July 2017.
- Spatial: 32 plots (4 blocks, 8 treatments) within a defined 50 m × 50 m plot layout with a central 30 m × 30 m measurement area.

## References
- Araújo, A. C., et al. 2002. Comparative measurements of carbon dioxide fluxes in central Amazon rainforest (Manaus LBA site).
- Laurance, W. F., et al. 2018. An Amazonian rainforest and its fragments as a laboratory of global change.
- Luizão, R.C., Luizão, F.J. 1991. Serrapilheira e biomassa microbiana do solo na Amazônia central.
- Metcalfe, D.B. 2014. Herbivory and ecosystem carbon and nutrient cycling in tropical forests.
- Pauletto, D. 2006. Nutrient stocks and fluxes in litter under selective logging in the northwest Mato Grosso.