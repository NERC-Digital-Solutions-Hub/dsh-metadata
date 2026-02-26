# Experimental design/Sampling regime

## Overview
- 15-minute river stage height measurements at 6 river monitoring stations in the Conwy catchment, North Wales.
- Time period: 2013–2016. Cwm Llanerch site also collected water temperature data.
- Data collected by CEH staff for the NERC project NE/J011991/1.
- Data gaps occurred due to equipment, battery, or system failures.

## Study sites and parameters
- Cwm Llanerch: parameters = Water level (mm), Water temperature (°C); coordinates 53.106627, -3.7916149.
- Glasgwm: parameters = Water level (mm); coordinates 53.027723, -3.8462502.
- Nant y Brwyn: parameters = Water level (mm); coordinates 52.990162, -3.8018288.
- Nant y Coed: parameters = Water level (mm); coordinates 53.049063, -3.7183329.
- Hiraethlyn: parameters = Water level (mm); coordinates 53.204355, -3.7827381.
- Dyffryn Mymbyr: parameters = Water level (mm); coordinates 53.089587, -3.9718091.

## Data collection methods
- Water level: measured every 10 seconds with pressure transducers; mean value recorded every 15 minutes onto data loggers.
- Cwm Llanerch temperature: measured and recorded in the same manner as water level.
- Data routinely downloaded to field laptop and uploaded to an Access database.

## Instruments and calibration
- General site instruments (excluding Cwm Llanerch): Druck PDCR 1830 pressure transducer; Campbell Scientific CR10 data logger.
- Cwm Llanerch site: CS451 pressure transducer; Campbell CR1000 data logger.
- Transducers located in still wells at the edge of the channel.
- Rationale for variation: initial CR10x/PDCR kit discontinued; CS451 and CR1000 adopted for Cwm Llanerch.
- Calibration: Druck PDCR 1830 calibrated prior to deployment (DPI 510, 2013) at CEH Wallingford; CS451 was brand new and factory calibrated prior to deployment.

## Data management and quality control
- Data quality: routine site visits and data downloading; data screened for obvious issues.
- Common issues: periods with no data due to power failure resolved by field visits to replace batteries.

## Data structure and file formats
- Data organized into separate CSV files per site.
- Filenames indicate site and time span (e.g., 2013–2016).
- Five-site files (Dyffryn Mymbyr, Glasgwm, Hiraethlyn, Nant y Coed, Nant y Brwyn): columns = ID, Date (dd/mm/yyyy), Time (hh:mm:ss), Stage_ht_mm, Battery_volt.
- Cwm Llanerch file adds Temp_degC column to the above set.

## Site timelines (start and end dates)
- Cwm Llanerch: start around 12/03/2013; end 03/02/2016.
- Glasgwm: start around 18/04/2013; end 01/03/2016.
- Nant y Brwyn: start around 11/03/2013; end 01/03/2016.
- Nant y Coed: start around 21/03/2013; end 01/01/2016.
- Hiraethlyn: start around 05/11/2013; end 01/01/2016.
- Dyffryn Mymbyr: start around 14/03/2013; end 04/02/2016.