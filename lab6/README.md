# ECEN 2714 · Lab 6 RC Filter Plotter

Deploy the contents of this folder into `lab6/` within `staysaif/ECEN2714-Plotter`. Do not change the files at the repository root (Lab 5).

Live page once published: https://staysaif.github.io/ECEN2714-Plotter/lab6/

This version supports **RC LPF and RC HPF only**, both with R = 1 kΩ and C = 10 nF (theoretical cutoff ≈ 15.92 kHz). The downloaded template contains the **19 exact frequency rows** from the revised handout: 1, 2, 4, 6, 8, 10, 12, 16, 20, 25, 30, 40, 50, 60, 80, 100, 150, 200, and 400 kHz.

**There is no minimum list of specific frequencies required by the plotter.** Missing rows and blank measurements are allowed. Each filter independently plots any two or more valid magnitude or phase points, without inventing missing values. The original LPF data with only 18 points through 200 kHz will plot.

CSV formats supported:
- Two vertically stacked labeled blocks, `RC_LPF` and `RC_HPF`.
- Individual LPF/HPF CSV exports; include `lpf` or `hpf` in the filename and select both files together.
- Older wide CSVs with circuit-prefixed column headings.

Measurements use `Vin_Vpp`, `Vout_Vpp` and `Phase_deg` (CH2 − CH1). Optional `Gain_dB` can be supplied, but voltage-derived gain takes precedence. Extra frequencies are accepted; the two filters can use different frequency sets.

The synthetic example is intentionally 10 GHz (LPF) and 12 GHz (HPF) to distinguish it from real lab measurements. All processing runs locally; data are not uploaded to any server.
