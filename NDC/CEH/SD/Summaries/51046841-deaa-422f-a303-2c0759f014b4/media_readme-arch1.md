# Data Description for Experiments CompEvo and HostAvail

- The document describes data from two separate experiments, CompEvo and HostAvail, each with distinct treatments and associated data files.
- Data are organized into two main data frames/files:
  - Experimental setup data (including treatments and conditions)
  - Flow cytometry data (flow_data.txt) and derived fractions (fraction_data.txt)

## Experiments and Treatments

- CompEvo (two runs with distinct treatments)
  - A: SBW25.GmR; SBW25.GmR pQBR57d59.GmR.GFP; SBW25d4242.GmR.dTomato pQBR57
  - B: SBW25.GmR pQBR103; SBW25.GmR pQBR57d59.GmR.GFP; SBW25d4242.GmR.dTomato pQBR57 + Mercury
  - C: SBW25.GmR; SBW25.GmR pQBR57d59.GmR.tdTomato; SBW25d4242.GmR.YFP pQBR57
  - D: SBW25.GmR pQBR103; SBW25.GmR pQBR57d59.GmR.tdTomato; SBW25d4242.GmR.YFP pQBR57 + Mercury
  - F1: SBW25.GmR pQBR57d59.GmR.GFP
  - F2: SBW25d4242.GmR.dTomato pQBR57
  - F3: SBW25.GmR pQBR57d59.GmR.tdTomato
  - F4: SBW25d4242.GmR.YFP pQBR57

- HostAvail (four sub-treatments A–D; plus a KT2440.KmR example in D)
  - A: SBW25.GmR : ( SBW25.GmR pWBR57d0059.GFP : SBW25d4242.dTomato pQBR57)
  - B: SBW25.GmR : ( SBW25.GmR pWBR57d0059.GFP : SBW25d4242 pQBR57.tdTomato)
  - C: SBW25.GmR : ( SBW25.GmR pWBR57d0059.GFP : SBW25.GmR pQBR57.tdTomato)
  - D: KT2440.KmR : (SBW25.GmR pWBR57d0059.GFP : SBW25d4242.dTomato pQBR57)

## Experimental Metrics

- Ratio: Proportion of Available vs Occupied hosts at the start point.
- Replicate: Biological replicate of a given treatment.
- Transfer: Timepoint (in days) in the evolution experiment when bacteria are transferred to fresh media (every 24 hours).

## Flow cytometry data (flow_data.txt)

- Machine: Be​ckman Coulter Cytoflex.
- Signals and thresholds (used to identify bacterial events and fluorescence markers):
  - FSC.H: Forward Scatter height, threshold 1e3.
  - SSC.H: Side Scatter height, threshold 1e3.
  - PB450.H: PB450 signal height, threshold 1e3.5; used to detect Hoechst-stained bacteria.
  - FITC: FITC signal height, threshold 1e3.5; detects GFP and YFP.
  - ECD: ECD signal height, used to confirm PE filtering; threshold 1e3.5; detects dTomato and tdTomato.
  - PE: PE signal height, threshold 1e3.4; detects dTomato and tdTomato.

## Fraction data (fraction_data.txt)

- Total.Count: total number of events per sample that pass basic thresholds (size and cytometry gates) and are considered bacteria vs background.
- Fraction_Red: proportion of total counts classified as red (surpassing PE threshold but not surpassing FITC threshold).
- Fraction_Yellow: proportion of total counts classified as yellow (surpassing FITC threshold but not surpassing PE threshold).
- Fraction_Orange: proportion of total counts classified as orange (surpassing both PE and FITC thresholds).
- Fraction_Blue: proportion of total counts classified as blue (surpassing neither threshold).