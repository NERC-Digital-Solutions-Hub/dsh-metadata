# Site description

- Location: AFEX project area at BDFFP/INPA, ~80 km north of Manaus, Amazonas, Brazil (coordinates provided). Climate: mean air temperature ~26°C, mean annual precipitation ~2,400 mm; relative humidity 75–92% seasonally.
- Study goal: a full factorial nutrient addition experiment to examine impacts on soil microbial/enzymatic activity and nutrient cycling.

## Experimental setup — AFEX Experiment

- Start date: May 2017.
- Design: full factorial nutrient addition with eight treatments and four replicates per treatment.
- Treatments included: control; N; P; cations (Ca, Mg, K); N+P; N+cations; N+P+cations.
- Plot layout: 32 plots total across four independent blocks (≥250 m apart).
- Plot size and sampling area: each plot 50 m × 50 m; central measurement area 30 m × 30 m.

## Nutrient application

- Application method: manual dry granules to the soil surface; three applications per year.
- Rates (yr⁻¹): N = 125 kg ha⁻¹ (as urea); P = 50 kg ha⁻¹ (as triple superphosphate); Ca = 50 kg ha⁻¹; Mg = 20 kg ha⁻¹ (as dolomitic limestone); K = 50 kg ha⁻¹ (as KCl).

## Soil sampling and processing

- Sampling time: after seven months of nutrient addition (January 2018).
- Procedure: three soil cores per plot (5 cm diameter) from the central 30 m × 30 m area; samples composited by depth (0–5 cm and 5–10 cm) with roots removed.
- Subsampling: fresh soils allocated for enzyme activity assays.

## Hydrolytic enzyme assays

- Target enzymes (soil carbon, nitrogen, phosphorus cycling): BG (β-glucosidase), NAG (N-acetyl-β-D-glucosaminidase), PHOS (phosphomonoesterase).
- Assay method: microplate fluorimetry based on Kaiser et al. (2010).
  - Procedure: 1 g soil in 100 mM sodium acetate buffer (pH 5.5); ultrasonicated; 200 μL soil suspension added to 96-well plates with 50 μL of MUF-labeled substrates for BG, NAG, and PHOS (in triplicate).
  - Incubation: 1 hour at ~25°C.
  - Detection: fluorescence reading at 365 nm excitation / 450 nm emission (fluorometer).
  - Output: enzyme activities expressed as nmol MUF g soil dry weight⁻¹ h⁻¹.
- Quality controls: standard curves and blanks prepared for each substrate and depth.

## Data management and structure

- Data organization (examples of fields used):
  - Block: block identifier (1–4).
  - Plot: plot identifier within block.
  - TRT: treatment code (eight treatments as described).
  - Depth: soil depth category (0–5 cm; 5–10 cm).
  - Enzyme codes: BG, NAG, PHOS with descriptive notes.
- Descriptions linked to each field (e.g., what each code represents, depth definition, and enzyme function).

## References

- Araújo AC. 2002. Comparative measurements of CO2 fluxes at Manaus LBA site.
- Kaiser et al. 2010. Belowground carbon allocation and enzyme activities in soil.