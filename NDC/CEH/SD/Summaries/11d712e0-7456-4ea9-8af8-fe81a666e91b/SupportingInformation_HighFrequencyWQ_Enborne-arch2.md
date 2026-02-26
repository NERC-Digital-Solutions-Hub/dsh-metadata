# Brief description of the dataset

## Scope and period
- Hourly physical and nutrient monitoring data for the River Enborne near Brimpton (grid SU568648).
- Time period: November 2009 to February 2012.
- Parameters: total reactive phosphorus (TRP), nitrate (NO3), conductivity, temperature, dissolved oxygen (DO), pH, chlorophyll.
- Includes accompanying hourly averaged flow data from Environment Agency (EA) gauging station at the same site.

## Monitoring setup and instrumentation
- Instruments:
  - Micromac C automated nutrient analyser (TRP)
  - YSI 6600 multi-parameter sonde (DO, pH, temperature, conductivity, turbidity, chlorophyll)
  - Nitratax Plus probe (NO3)
- Location and housing: installed in an insulated shed 2 m from the riverbank at Brimpton.
- Sampling approach: water pumped from a river intake 1 m from the bank; intermittent pumping to minimize sediment resuspension; flow cells used for TRP and NO3 analyses.
- TRP method: colorimetry via phosphomolybdenum blue complexation; detection limit 0.025 mg P L⁻¹; daily check standard; fortnightly recalibration when reagents change.
- NO3 method: UV-absorbance (210 nm) with reference at 350 nm; detection limit 0.07 mg N L⁻¹; periodic checks with standard solutions.
- YSI measurements: in situ readings every hour; turbidity is NTU with temperature compensation; chlorophyll via fluorometer (470 nm).

## Measurement specifics and quality controls
- TRP data validated against manual laboratory samples (Seal AA3) using the same colorimetric method; supporting data referenced in Bowes et al. (2015).
- NO3 data validated against weekly laboratory ion chromatography samples; Bowes et al. (2015).
- Temperature control: shed heated to ~20°C to reduce reaction temperature errors and prevent frozen sampling pipes.
- YSI calibration: every 2–3 weeks by Environment Agency staff following SOPs.
- Turbidity corrections applied to chlorophyll measurements to account for optical interference from sediment.

## Flow data and time resolution
- 15-minute flow data provided by EA; hourly average derived for dataset.
- Flow units: cubic metres per second (m³/s).

## Data format and units
- Time format: day/month/year hour:minute.
- TRP: mg P L⁻¹ (unfiltered, total reactive phosphorus).
- Nitrate: mg NO3 L⁻¹.
- Conductivity, temperature, DO, pH: standard units as recorded by equipment.
- Turbidity: NTU (nephelometric turbidity units).
- Chlorophyll: μg L⁻¹ (total chlorophyll a, b, c).
- Flow: m³/s (hourly average of 15-minute values).
- Missing data: NaN.

## Context and references
- Related publications for methodology and high-frequency monitoring context:
  - Bowes et al. (2015) on phosphorus and nitrate inputs to a rural river.
  - Halliday et al. (2014) on water quality observations from high-frequency monitoring.
  - Wade et al. (2012) on hydrochemical processes in lowland rivers.

## Data provenance and usage notes
- Data are derived from multiple instruments with cross-checks to manual laboratory analyses.
- The dataset supports standardized reporting of environmental health indicators and can be integrated with other monitoring data for policy performance assessment.
- Relevant caveats: TRP is operationally defined; TRP sample at 06:00 is omitted due to daily check standard measurement. Chlorophyll readings may be influenced by sediment and corrected using turbidity data.