# ReadMe file for Biomass_N_and_CtoN.csv

## Overview
- Dataset derived from a field trial investigating greenhouse gas emissions from sheep urine patches deposited on semi-improved upland grassland.
- Captures above-ground biomass harvests within greenhouse gas chambers (dimensions: 50 cm x 50 cm).
- Trial location: orthic podzol at Henfaes Research Station, Abergwyngregyn, North Wales (270 m a.s.l.; 53°13'N, 4°0'W).
- Experimental design: four treatments in a randomised block design (Control = no urine, ArtUrine = artificial sheep urine, RealUrine = real sheep urine) applied in spring and autumn 2016.
- Biomass cuts: four times after spring treatments; three times after autumn treatments.
- Biomass samples dried, ground, and chemically analyzed; data visually checked for errors.

## Experimental Design and Sampling
- Treatments (n=4): Control, ArtUrine, RealUrine (within blocks).
- Application timing: treatments applied in spring and autumn 2016.
- Sampling schedule: biomass cuts conducted at multiple time points (four post-spring, three post-autumn).
- Plot details: biomass harvested from chambers corresponding to plot numbers.

## Data Processing and Measurements
- Sample processing: biomass dried in an oven at 80 °C for 24 hours, then ground.
- Analytical method: samples analysed with a TruSpec® Analyzer (Leco) against certified standard reference materials.
- Quality checks: data visually inspected for errors.

## Data Structure and Variables (Headers)
- Sample_date: Date of biomass sampling.
- Plot_no: Chamber/plot identifier from which biomass was sampled.
- Treatment: Treatment category per sample (Control, ArtUrine, RealUrine).
- Season: Season in which treatments were applied (Spring, Autumn).
- Biomass: Above-ground biomass in g dry weight per m².
- Foliar_N: Nitrogen content of dried and ground biomass, in percent.
- Foliar_CtoN: Carbon-to-N ratio of biomass samples.

## Data Quality, Provenance, and Metadata
- Provenance: field trial data with explicit location, soil type, and treatment structure.
- Data quality notes: only visual error checks documented; no detailed automated QC steps described.
- Metadata includes measurement units and sample/treatment identifiers to support trackability and reuse.

## Use, Reuse, and Best Practices
- Authorship note: Authors must be acknowledged if data are reused or reproduced.
- Potential uses: analyses of how urine treatments influence biomass composition (N content and C:N ratio) and biomass yield under different seasonal applications.
- Considerations for researchers: ensure consistent interpretation of headers (e.g., Treatment categories, Season labels) and align dates to standard formats for integration with other datasets.

## Limitations and Scope
- Limited to a single upland grassland site with specific soil type and altitude.
- Temporal coverage limited to 2016 spring and autumn treatment applications.
- Data checks described are visual; users may want to implement additional QC and standardization when integrating with other datasets.