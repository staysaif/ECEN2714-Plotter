# ECEN 2714 · Lab 6 Frequency Response Plotter

A GitHub Pages-ready website for the four passive RC/RL filters measured in ECEN 2714 Lab 6.

## Live deployment in the existing ECEN2714-Plotter repository

These files are intended for the `lab6/` folder of `staysaif/ECEN2714-Plotter`. The **Lab 5 root site remains unchanged**.

With GitHub Pages set to deploy from `main` / `(root)`, Lab 6 can be accessed at:

`https://staysaif.github.io/ECEN2714-Plotter/lab6/`

**If the URL returns 404:** Go to GitHub repository **Settings → Pages → Build and deployment**, select **Deploy from a branch**, branch **main**, folder **/(root)**, and save. GitHub may need to publish the new commit before the URL works.

## Files

- `index.html` — the student-facing site; CSV import, validation, plots and PNG exports
- `ECEN2714_Lab6_CSV_Template.csv` — direct-download template linked from the site; four labeled circuit tables and 15 required frequencies each
- `Lab6_Example_Data_DO_NOT_SUBMIT.csv` — synthetic demonstration dataset, not actual measurements
- `.nojekyll` — optional static-site compatibility marker

No installation, backend server, CSV upload service, build pipeline, or external JavaScript libraries are needed.

## Using the CSV

The CSV file holds four independent, vertically stacked sections: `RC_LPF`, `RC_HPF`, `RL_LPF`, `RL_HPF`. Each section is a separate table with headings:

`Frequency_Hz,Vin_Vpp,Vout_Vpp,Phase_deg`

Keep every listed frequency row (1 kHz through 3 MHz). Leave a measurement column blank until it is complete, and enter values for all required frequencies before plotting that response. Extra frequencies may be inserted into individual circuit tables.

Magnitude is computed from 20·log10(Vout_Vpp / Vin_Vpp). Phase is output minus input in degrees. Optional complete `Gain_dB` columns and previous Lab 6 wide-layout CSV files remain supported.

Each circuit is plotted separately, with magnitude/phase options. A missing or partially filled measurement column produces a readable error and never causes incomplete data to be plotted. Other complete series can still be plotted.

## Publishing to a separate repository instead

Upload these same files to the **root** of any public GitHub repository with `index.html` at its top level. Then enable Pages in **Settings → Pages → Deploy from a branch**, branch `main`, folder `/(root)`. The CSV link is relative and works from either location.

All student measurement data are processed in the student's browser.
