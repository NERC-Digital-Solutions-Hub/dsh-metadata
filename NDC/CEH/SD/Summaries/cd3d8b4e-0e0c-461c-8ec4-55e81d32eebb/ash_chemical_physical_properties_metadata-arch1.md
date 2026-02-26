# Physical and chemical properties of wildfire ash collected from different ecosystems and burn severities across the globe, 2003-2021

## Overview
- Global dataset characterizing wildfire ash chemical and physical properties collected from 2003 to 2021, with analyses conducted through 2022.
- Built to characterize how ash composition varies with ecosystem, burn severity, and sampling site to inform environmental impact and ash behavior analyses.
- Data produced from Swansea University analyses; includes two main data files and a detailed methodology.

## Data files and content
- ash_chemical_properties.csv: Chemical characteristics, including site metadata and concentrations.
- ash_physical_properties.csv: Physical characteristics, including site metadata and physical measurements.
- Key fields common to both: Country, site name, year, burn severity, sample name; sampling and analysis provenance.
- Chemical properties include:
  - Isotopic and elemental composition: δ13C, total C, CO3, N; total concentrations of P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, Cr, Co, Br, Sr; Hg, As, Cd (mass-based units).
  - Welished measurements: pH, electrical conductivity (EC), UV transmittance at 254 nm.
  - Dissolved constituents: DOC, NH4+, NO3-, Cl-, SO4-, F-, P, Ca, Mg, Na, K, Al, Si, Fe, Mn, Ni, Cu, Zn, Pb, B; Hg, As, Cd (dissolved forms).
- Physical properties include:
  - Ground truth and performance indicators: WR_33kPa, WR_1500kPa (water retention at specific pressures), bulk density (g cm-3), WDPT (water drop penetration time) class counts.
  - Sample metadata: country, site name, year, burn severity, sample name.

## Sampling and locations
- Sampling sites include Madre del Agua (Tenerife, Spain), Thompson Reservoir (Victoria, Australia), Higher Swineshaw Reservoir (Manchester, UK), and Mesa Fire (Idaho, USA).
- Chemical analyses conducted at Swansea University (UK).
- The dataset uses a country and site field to indicate specific sampling locations.

## Temporal coverage
- Ash samples collected 2003–2021.
- Laboratory analyses performed 2003–2022.

## Analytical methods and workflow
- Chemical analysis methods:
  - pH and electric conductivity (EC) via pH meter and conductivimeter after leachate preparation.
  - F-, NH4+, UV index, DOC, P & PO4 measured using leachate-extraction protocols; UV index via 254 nm spectrophotometry.
  - Cl-, NO3-, SO4- measured by Liquid Ion Chromatography.
  - %C and %N by elemental combustion analysis (LECO).
  - CO3 by Bernard Calcimeter; isotopic carbon (δ13C) and other elements by appropriate instrumental methods (e.g., AAS for metals, ICP for multi-element analyses).
  - Hg by EPA 7473 thermal decomposition and AAS (DMA-80 system).
- Digestion and leachate procedures:
  - Total element analyses via EPA 3051 digestion (0.25 g sample + acids, microwave digestion).
  - Leachate experiments following established guidelines (4 g sample in 100 mL water; shaking, standing, filtration; sub-samples for various analyses).
  - Carbonates determined with Bernard Calcimeter per ISO 10693:1995.
  - WDPT used to assess water repellency (Doerr, 1998) with a standardized protocol.
- Replication:
  - Chemical analyses: 2 to 20 replicates per site and treatment.
  - Physical analyses: 4 replicates per site and treatment.
- Documentation and references provided for standard methods (e.g., Klute, Blake & Hartge; Doerr; EPA 3051).

## Variables and completeness
- Chemical characteristics: comprehensive suite of major and trace elements, carbon content, carbonate, dissolved constituents, pH, EC, and UV metrics. Some parameters are not analysed for every ash sample.
- Physical characteristics: complete dataset for the specified physical properties; WDPT classes captured.
- Observations:
  - Chemical characteristics: 296 wildfire ash samples.
  - Physical characteristics: 36 wildfire ash samples.
- Completeness note: chemical parameters may be missing for some samples; physical parameters are more consistently represented.

## Data provenance, access, and use
- Data produced by Swansea University with explicit site metadata and methodological detail.
- Documentation includes detailed methodology, replication, and references, enabling reproducibility and cross-study comparisons.
- Data suitable for cross-site comparisons, burn severity analyses, and modeling of ash behavior; potential caveats include gaps in chemical measurements across samples and scaling differences between sites.

## Practical implications and caveats for analysts
- Well-suited for exploring correlations between ash composition, burn severity, and site-specific factors; supports development of predictive models for ash behavior and environmental impact.
- Useful for meta-analyses combining chemical and physical properties with burn severity and ecosystem context.
- Be mindful of gaps in chemical data (not all parameters measured for every sample) and potential scale limitations when comparing across sites.
- Access and usability considerations: data are provided as two CSV files with rich metadata and a detailed methods dossier, but broader data portal integration is not specified.