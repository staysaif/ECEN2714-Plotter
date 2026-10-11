# ECEN 2714 Frequency Response Plotter

Static browser-side plotting tool for ECEN 2714 Lab 5 TL072 frequency-response measurements.

## Files
- `index.html` — complete application; no server-side code required.
- `template.csv` — recommended full CSV header.
- `dummy_lab5_data.csv` — complete demo/test dataset.

## CSV behavior
`Frequency_Hz` is the only mandatory column because every plot needs a frequency axis. The remaining expected columns are optional:

- `Vin_Vpp`
- `Vout_Inv_Vpp`
- `Phase_Inv_deg`
- `Vout_NonInv_Vpp`
- `Phase_NonInv_deg`

The page detects what can actually be plotted. Missing or insufficient columns do **not** reject the entire file. Instead, unavailable response/circuit choices are greyed out and the page displays a CSV-format warning. Magnitude requires `Vin_Vpp` plus the corresponding output-Vpp column. Phase requires only the corresponding phase column.

If `Frequency_Hz` is missing, the file cannot be plotted and the page reports an error.

## Plot options
Students can choose:
- Magnitude only, phase only, or both.
- Inverting only, non-inverting only, or both circuits.
- Overlay circuits or separate panels when both circuits are available.

When all four series are available, selecting both response types, both circuits, and separate panels creates a 2×2 response window.

## Publishing
Upload these files to the root of a GitHub repository and enable GitHub Pages from the `main` branch `/ (root)`. The resulting HTTPS URL can be added to Canvas as an External URL or embedded where institutional Canvas settings permit.

All CSV processing occurs locally in the student's browser.
