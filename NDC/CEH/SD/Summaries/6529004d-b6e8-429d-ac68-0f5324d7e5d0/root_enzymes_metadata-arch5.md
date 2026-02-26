# Site description

- Location and setting: AFEX project area at the Biological Dynamics of Forest Fragments Project (BDFFP/INPA), ~80 km north of Manaus, Amazonas, Brazil (02° 25' 00'' S; 59° 43' 00' W).
- Climate context: Mean annual temperature ~26 °C; mean annual precipitation ~2,400 mm; relative humidity 75–92% across seasons.

## Experimental setup - AFEX Experiment

- Design: Full factorial nutrient addition experiment with eight treatments: control, N, P, cations (Ca, Mg, K), and combinations N+P, N+cations, N+P+cations.
- Plot and replication: 32 plots total (4 replicates per treatment) arranged in 4 independent blocks with at least 250 m between blocks.
- Plot geometry: Each plot 50 m x 50 m; central 30 m x 30 m area used for main measurements.
- Nutrient application: Dry granules applied three times per year at rates:
  - N: 125 kg ha^-1 year^-1 (as urea)
  - P: 50 kg ha^-1 year^-1 (as triple superphosphate)
  - Ca: 50 kg ha^-1 year^-1
  - Mg: 20 kg ha^-1 year^-1 (as dolomitic limestone)
  - K: 50 kg ha^-1 year^-1
- Sampling framework: Data collection focused on the central plot area (30 m x 30 m) within each plot.

## Root sampling and processing

- Ingrowth cores: In each plot (n=32), five 12 cm-diameter, 30 cm-deep root ingrowth cores (2 cm plastic mesh bags) installed in August 2017.
- Sampling schedule: Ingrowth cores collected every three months; five core replicates homogenised by plot and soil depth (0–10 cm and 10–30 cm; N=64 total).
- Focus period: Only fine roots produced between November 2017 and February 2018 (middle of the wet season) used.
- Processing: Roots washed; cumulative root biomass sampled within each 60-minute collection window used to estimate sampling yield; Michaelis-Menten asymptotic curve applied to extrapolate biomass for 180 minutes (based on Metcalfe et al. 2007).

## Root subsampling and enzyme assays

- Depths for subsampling: 0–10 cm and 10–30 cm (both depths analyzed).
- Enzyme focus: Potential root acid phosphomonoesterase activity (PHOS) measured in root tips (<1 mm diameter).
- Subsample preparation: Triplicate subsamples per plot and depth for PHOS assay within 3 days of root sampling.
- Assay method: Fluorimetric microplate assay using MUF (Methylumbelliferyl-phosphate) as substrate.
  - Sample size: ~10 mg fresh root material per assay
  - Incubation: 30 minutes at ~25 °C with gentle shaking
  - Termination: 50 μL of 1 M NaOH added to stop reaction
  - Measurement: Fluorescence read at 365 nm excitation / 450 nm emission on a fluorometer (Tecan Infinite 200 PRO)
- Data output: PHOS expressed as μmol MUF g^-1 dry mass h^-1 per plot per depth.

## Spreadsheet details and data structure

- Metadata fields:
  - Block: 1–4 (indicating block assignment)
  - Plot: 1–8 (plot designation within a block)
  - TRT: treatment code corresponding to one of the eight nutrient treatments
  - Depth: 0–10 cm or 10–30 cm
- Data constructs: PHOS measurements organized by plot, depth, and time (sampling interval across November 2017–February 2018; central 30x30 m area per plot).

## Data quality, provenance, and governance considerations for Data Stewards

- Provenance and traceability:
  - Clear experimental design (treatment structure, replication, block layout) and sampling timeline.
  - Documented methodological steps for root collection, processing, and PHOS assays.
- Metadata and data dictionary:
  - Essential to include: Block, Plot, TRT, Depth, time point(s), PHOS values, units, and the exact assay conditions (substrate, incubation, instrument model).
- Data standards and interoperability:
  - Use consistent units (PHOS in μmol MUF g^-1 dry mass h^-1; depths as defined 0–10 cm and 10–30 cm).
  - Standardize treatment codes and plot identifiers across datasets to enable integration with other measurements (e.g., biomass, soil nutrients, environmental variables).
- Data quality assurance:
  - Maintain records of sampling dates, storage conditions, and any deviations from protocol.
  - Include blanks, standards, and duplicate measurements from the PHOS assays for QA purposes.
- Data sharing readiness:
  - Provide a complete data dictionary, a methods summary, and references (e.g., Metcalfe et al. 2007; Lugli et al. 2019; Turner & Romero 2010; German et al. 2011) to contextualize procedures.
  - Prepare dataset alongside a governance note describing data ownership, access restrictions (if any), and intended data use.

## References

- Araújo AC. 2002. Comparative measurements of carbon dioxide fluxes from two nearby towers in a central Amazonian rainforest: The Manaus LBA site. Journal of Geophysical Research 107:2156-2202.
- German DP, et al. 2011. Optimization of hydrolytic and oxidative enzyme methods for ecosystem studies. Soil Biology and Biochemistry 43:1387-1397.
- Lugli LF, et al. 2019. Multiple phosphorus acquisition strategies adopted by fine roots in low-fertility soils in Central Amazonia, Plant Soil.
- Metcalfe DB, et al. 2007. A method for extracting plant roots from soil which facilitates rapid sample processing without compromising measurement accuracy: Methods. New Phytologist 174:697-703.
- Turner BL, Romero TE. 2010. Stability of hydrolytic enzyme activity and microbial phosphorus during storage of tropical rain forest soils. Soil Biology and Biochemistry 42:459-465.