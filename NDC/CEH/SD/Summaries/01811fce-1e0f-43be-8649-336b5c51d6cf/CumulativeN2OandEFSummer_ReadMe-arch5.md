# ReadMe file for CumulativeN2OandEFSummer.csv

## Overview
- The dataset contains cumulative N2O emissions and N2O-N emission factors measured from three treatments: Control (no urine), ArtUrine (artificial sheep urine), and Urine (real sheep urine).
- Site: unimproved grazing land in the Carneddau mountains, Snowdonia National Park, Wales, UK (556 m a.s.l.; 53°22'N, 3°95'W).
- Experimental design: randomised block design.
- N application rates: 920 kg N ha-1 for artificial urine; 930 kg N ha-1 for real sheep urine.
- Emissions calculation: cumulative N2O emissions derived from the area under the curve of replicate chambers using trapezoidal integration; EF corrected for the portion of area not treated due to discrete patch application within the chamber.
- Data quality: visually checked for errors.
- Authors must be acknowledged if data are re-used or reproduced.

## Data structure and headers
- Treatment: one of 'Control', 'ArtUrine', or 'Urine'.
- Chamber: chamber number from which N2O emissions were measured.
- Cum_N2O: cumulative N2O emissions (micrograms N2O-N) for each chamber over 144 days.
- EF: N2O-N emission factor as a percentage of total N applied.

## Calculations and processing
- Cumulative N2O: area under the N2O-N emission curve for each chamber over 144 days (via trapezoidal integration).
- EF: percentage of the applied urine-N that was released as N2O-N, with correction for the area not treated due to patch application within the chamber.

## Experimental design and site details
- Location: Carneddau mountains, Snowdonia National Park, Wales.
- Soil: dystric histosol.
- Design: randomized block.
- Treatments correspond to control, artificial urine, and real urine applications, with discrete patches of urine applications.

## Data quality and provenance
- Authorship acknowledgment required for reused/reproduced data.
- Data visually checked for errors.

## Usage notes
- Be sure to cite the original dataset and acknowledge authors when re-using.
- Understand that EF calculations include adjustments for patch areas not treated within measurement chambers.