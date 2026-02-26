# Materials and Methods for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data.

## Study design and materials
- Soil: Woburn sandy loam; amended with sewage sludge spiked with ENMs (ZnO 30 nm uncoated, Ag 50 nm PVP-coated) and TiO2 (27±7.5 nm), or with ionic/bulk forms (ZnSO4, AgNO3, micron-sized TiO2); control with no metals.
- Target loadings: Zn in sludge 2800 mg Zn/kg dry mass; Ag ~100 mg/kg; Ti ~2400 mg/kg (dry mass).
- Sludge production: 40 kg dry sludge per plant (160 kg wet sludge at 25% solids); air-dried and mixed with soil to achieve 0.58:0.42 soil:sludge and ~1400 mg Zn/kg dry soil for ionic-metal treatment.
- Aging: soil-sludge mixtures aged in outdoor lysimeters for six months.
- Experimental units: four replicates per aged soil-sludge treatment; included fully replicated soil control without sludge.
- Earthworms: Eisenia fetida; groups of ten per replicate; maintained at 20 ± 1°C, 12:12 h light:dark.

## Experimental treatments and endpoints
- Aged soil-sludge treatments (five total): 
  1) control soil-sludge (no metal),
  2) high-metal ENM soil-sludge,
  3) high-metal ionic metal soil-sludge,
  4) low-metal ENM soil-sludge (1:1 mix with control),
  5) low-metal ionic metal soil-sludge (1:1 mix with control).
- Additional control: soil only (no sludge) fully replicated.
- Exposure setup: four replicates per treatment with 300 g (dry weight) soil-sludge; eight soil controls with 550 g dry weight.
- Feeding: soil-only controls received 10 g dry horse manure; sludge treatments provided no added food (sludge serves as a food source).
- Endpoints and timing:
  - Survival measured at 14 and 28 days.
  - Batch weight of surviving earthworms recorded after 28 days.
  - After 28 days, three surviving adults per replicate depurated and prepared for tissue analysis.
  - Reproduction: 56 days total; juveniles counted after cocoons hatch.
- Densities and conditions kept constant; temperature and light cycles as above.

## Single-compound exposures for comparison
- Separate exposures to as-synthesised ZnO ENM (30 nm) and PVP-coated Ag ENM, and to Zn(NO3)2 and AgNO3 salts.
- Protocol identical to soil-sludge exposures; endpoints: 28-day survival and 56-day reproduction.
- Spiking levels varied by compound to enable comparison across ENMs vs. ions.

## Soil porewater extraction
- Rationale: porewater reflects uptake route for ionic metals.
- Procedure: after 56 days, two 20 g samples per replicate (dry weight equivalents) saturated to 140% WHC; porewater extracted by centrifugation.
- Analysis: ICP-OES for Zn and Ag; pH measured in soil; filtration steps to minimize adsorption losses (Ag samples filtered through glass wool and pre-treated filters).

## Chemical analysis and tissue preparation
- Digestion:
  - Soil and soil-sludge: ~0.75 g; earthworms: ~0.5 g; digested with HCl/HNO3 (3:1) at 140°C for 2.5 h.
  - Porewater: 1 ml digested with HCl/HNO3 in closed vessels; final volume 50 ml with 1% HCl.
- Instrumentation: ICP-MS (Perkin Elmer Nexion 300D) for Ag and Zn; ICP-OES used for porewater measurements; pH readings with calibrated meter.
- Quality checks: digestion efficiency and instrument calibration documented in Supporting Information.
- Tissue processing: total metal concentrations in earthworms corrected for residual gut soil contamination using Al as a conservative tracer.

## Data correction for gut contamination
- Rationale: soil residues in gut can bias tissue metal measurements.
- Correction method:
  - M_worm,sum,cor = M_worm,sum − m × Al_worm,sum
  - M_worm,sum and Al_worm,sum are measured tissue concentrations; m is the slope from linear regression of metal vs. Al in each exposure type.
- Outcome: separate regressions for each exposure type; significant relationships (p < 0.05) used to adjust Ag and Zn tissue concentrations.

## References and context
- Methods align with OECD Earthworm Reproduction Test (No. 222) and prior sludge-to-earthworm toxicity studies.
- Data generation tied to previous work on nanomaterial fate in biosolids, soil bioavailability, and metal uptake, providing context for interpreting tissue burdens, porewater speciation, and reproductive outcomes.

## Data scope and intended use
- Captures multiple treatment contrasts (ENM vs. ionic metals; high vs. low metal load; sludge-amended vs. sludge-free) and endpoints (survival, growth, reproduction, and tissue metal burden).
- Includes porewater measurements to link exposure chemistry with biological uptake.
- Provides data correction steps to improve accuracy of tissue metal concentrations, enabling robust comparisons across treatments.