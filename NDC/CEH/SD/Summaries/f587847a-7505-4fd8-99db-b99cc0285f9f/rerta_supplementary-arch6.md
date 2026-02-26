# Nitrous oxide and methane fluxes from different riparian restoration treatments in Oil Palm plantations in Riau, Indonesia 2019-2021

## Aim and context
- Assesses greenhouse gas fluxes (N2O, CH4, CO2) across four riparian treatments to inform management and policy for oil palm plantations.
- Context: riparian buffers are regulated and valued for water quality and biodiversity; little known about their effect on GHG emissions; study aims to guide growers and policymakers.

## Experimental design
- BEFTA/BEFTA-linked RERTA project conducted at two estates (Kandista and Ujung Tanjung); greenhouse gas study focused at the Ujung Tanjung site.
- Four treatments in 50 x 400 m river-side zones:
  1) Immature oil palm – no restoration, replanting to river margin
  2) Mature oil palm – no restoration, 50 m buffer maintained
  3) Native trees – enrichment planting of forest trees in a 50 m buffer, mature palms removed
  4) Mature oil palm with native trees – enrichment planting with forest trees and maintenance of mature palms
- 40 static chambers installed (six replicates per treatment, plus 16 in surrounding plantation) across two sides of the river.
- Sampling occurred monthly from January 2019 to September 2021, with breaks for felling/replanting (Apr–Oct 2019) and Covid-19 restrictions (Jan–Jun 2021).

## Data collection and field methods
- Static chambers (40 cm diameter) installed ground-tight to ~7 cm; chambers closed with lids and sampling ports; four samples per chamber over 45 minutes (0, 15, 30, 45 minutes).
- Gas samples transferred to 20 mL vials for laboratory analysis.
- Volumetric soil moisture measured near each chamber.
- Permits governing the international fieldwork obtained (two RISTEK permits listed).

## Laboratory analysis and calibration
- Gas chromatography (GC) with μECD for N2O and FID for CH4 and CO2 at UKCEH Edinburgh.
- Concentrations determined by comparison to four-point calibration standards.
- Fluxes calculated from concentration changes using the RCFlux R package, fitting six models and selecting the best fit; results expressed as micromoles per square meter per second with 95% confidence intervals.

## Data processing and quality control
- RCFlux outputs provide regression-based flux estimates per chamber and sampling event for each gas; includes multiple model fluxes, best-fit flux, and confidence intervals.
- Quality control included visual inspection of regression plots; data flagged as valid/invalid to account for sampling issues or field anomalies.
- Data structure includes time, chamber, position, treatment zone, and environmental context (soil moisture, chamber dimensions, location coordinates).

## Data files and structure
- rerta_ghg_rcflux.csv
  - Contains flux estimates for each chamber, each sampling occasion (monthly, Jan 2019–Sep 2021) with multiple modeling approaches and a best-fit selection.
  - Includes 95% confidence intervals, model quality metrics (e.g., adj R2), date, chamber ID, location context (plot, treatment_zone, treatment), soil moisture, and physical/demographic details.
- rerta_chambers.csv
  - Details of the 40 static chambers: chamber IDs, location (east/west of river), plot location (plantation vs. riparian buffer), treatment and date_installed/date_planted, latitude/longitude, elevation, and chamber dimensions.

## Data usage and potential applications
- Enables comparative analyses of GHG fluxes across riparian restoration treatments over time.
- Suitable for integration with environmental variables (soil moisture, land-use context) to model drivers of CH4 and N2O flux in tropical agroecosystems.
- Supports dashboards or data products for policymakers and growers to evaluate environmental performance of riparian management options.
- Provides a transparent, reproducible data workflow (field collection, GC analysis, RCFlux processing) with clearly documented data structures.

## Permits and references
- Field work supported under Indonesian research permits (two listed RISTEK numbers).
- References provide methodological and contextual background for GHG flux measurements in tropical plantation landscapes.