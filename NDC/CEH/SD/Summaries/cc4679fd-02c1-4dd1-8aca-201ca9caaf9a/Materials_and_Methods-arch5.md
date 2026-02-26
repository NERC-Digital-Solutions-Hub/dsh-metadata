# Materials and Methods for 'Bioavailability and toxicity of nanomaterials in sewage sludge to earthworms' data.

## Overview
- Document describes experimental design, exposure procedures, and analytical methods used to assess bioavailability and toxicity of nanomaterials and metals in sewage sludge to earthworms (Eisenia fetida/andrei).
- Endpoints include earthworm survival, growth, and reproduction (juveniles), tissue concentrations of silver and zinc, and porewater metal concentrations.
- Methods align with OECD guideline 222 for earthworm reproduction tests and include both sludge-associated exposures and as-synthesised ENM/salt exposures.

## Experimental design and treatments
- Substrates and metals
  - Sandy loam soil amended with sewage sludge derived from spiked WWTP influent with either:
    - ENMs: ZnO (30 nm, uncoated), Ag (50 nm, PVP-stabilised), TiO2 (27±7.5 nm)
    - Ionic metals: ZnSO4, AgNO3
    - Control: no metals
- Target loadings
  - Zn in sludge: 2800 mg Zn/kg dry mass; Ag: 100 mg/kg; Ti: 2400 mg/kg
  - Target soil Zn concentration in ionic metal treatment: 1400 mg Zn/kg dry soil (via 0.58:0.42 soil:sludge, aged 6 months)
- Soil-sludge mixtures
  - Four replicate containers per treatment with 300 g dry weight of soil-sludge mix
  - Eight soil controls with 550 g dry weight
  - Aging: six months in freely-draining outdoor lysimeters
- Exposure treatments (earthworms)
  - Five aged soil-sludge treatments:
    1) control soil-sludge (no metal)
    2) high-metal ENM soil-sludge
    3) high-metal ionic metal soil-sludge
    4) low-metal ENM soil-sludge
    5) low-metal ionic metal soil-sludge
  - Additional fully replicated soil control without sludge
- Replication and conditions
  - Four replicates per soil-sludge treatment; appropriate replication for controls
  - Moisture: soils wet to 50% water holding capacity
  - Temperature: 20 ± 1 °C; 12:12 h light:dark
  - Gut clearance: 28-day exposure before tissue analysis, with a 24-hour purge on clean filter paper

## Earthworm exposure and end points
- Earthworms
  - Ten fully clitellated Eisenia fetida/andrei per replicate
  - Food: horse manure added to soil-only controls; no additional food for sludge treatments (sludge as food source)
- Time points and endpoints
  - Survival and batch weight measured at 14 and 28 days
  - Reproduction: after 28 days, adults removed; cocoons allowed to hatch for 28 more days; juveniles counted (total duration 56 days)
- Tissue and contaminant measurements
  - Surviving adults (three per replicate) prepared for tissue Zn and Ag analysis
  - Two separate exposure sets with single-compound treatments (ZnO ENM, Ag ENM, ZnSO4, AgNO3) using the same protocol for comparison

## Sample collection and porewater analysis
- Soil porewater extraction
  - End of exposure (56 days) before juvenile counts
  - Two 20 g (dry weight) soil samples per replicate for Zn and Ag analysis; saturated to 140% WHC and equilibrated overnight
  - Porewater extraction by centrifugation
  - Filtration and ultra-filtration to minimize adsorption (Ag samples filtered with CuSO4-treated filters; 5 mL porewater analyzed)
  - pH measured
  - Analyzed by ICP-OES for Zn and Ag

## Chemical analysis and data processing
- Digestion and analysis
  - Digestion: ~0.75 g soil or soil-sludge, or ~0.5 g earthworm tissue; 3:1 HCl:HNO3; 140 °C for 2.5 h
  - Post-digestion: filtered; digests made up to 50 mL with 0.5% v/v HNO3
  - Porewater digested with 3:1 acids in closed vessels; digests brought to 50 mL with 1% HCl
  - Analyzed by ICP-MS (Ag and Zn)
- Quality control and corrections
  - Determine efficiency of digestions, calibrations, and instrument performance per supporting information
  - Correct total metal concentrations in earthworms for gut residues using aluminum (Al) as a conservative, naturally occurring proxy
  - Correction method: M_worm,sum,corr = M_worm,sum − m × Al_worm,sum, where m is slope from linear regression of worm metal vs. worm Al for each exposure
  - Separate regressions for each exposure group; corrections applied when regression significant (p < 0.05)

## Metadata, standards, and data governance
- Data alignment with OECD 222 for earthworm reproduction
- Datasets likely to include: treatment identifiers, replicate ID, exposure duration, endpoints (survival, weight, juvenile count), tissue concentrations (Zn, Ag), porewater concentrations, pH, soil/sludge metal concentrations, digestion and instrument parameters
- Documentation and provenance to support data discovery, reuse, and interoperability
- Emphasis on transparent reporting of methodologies, units, detection limits, and QA procedures to ensure usability by data stewards and downstream users

## References and contextual notes
- References cover prior sludge fate studies, biosolids risk guidelines, toxicogenomics, nanoparticle uptake, and related earthworm toxicity methodologies
- Key guidelines: OECD 222 Earthworm Reproduction Test; biosolids risk assessment guidelines CFR 40 Part 503
- Additional methodological references detail porewater analyses, soil metal partitioning, and uptake dynamics relevant to interpretation and reuse of data