# Indian-Ocean-Acidification-Future-Projection
# Indian Ocean Surface Climatology Dataset (1980–2100)

## Overview

This repository contains monthly climatological surface ocean variables for the **Indian Ocean**, prepared from **ROMS simulations** for historical and future climate periods.

The dataset is organized into four climatological periods:

* **hist** → 1980–2014
* **nf** → 2015–2040 (Near Future)
* **mf** → 2041–2070 (Mid Future)
* **ff** → 2071–2100 (Far Future)

Each file contains monthly climatology (`month = 1–12`) and a period dimension (`period = hist, nf, mf, ff`).

---

## Available Variables

### Directly extracted from ROMS ensemble

* Sea Surface Temperature (**SST**)
* Sea Surface Salinity (**SSS**)
* Dissolved Inorganic Carbon (**DIC**)
* Total Alkalinity (**ALK**)

### Derived carbonate chemistry variables

The following variables were calculated using **PyCO2SYS** from ROMS-derived SST, SSS, DIC, and ALK:

* Surface pH
* Hydrogen ion concentration (**[H⁺]**)

---

## Carbonate System Calculation

Carbonate chemistry calculations were performed using:

PyCO2SYS

PyCO2SYS solves the marine carbonate system using thermodynamic equilibrium equations based on supplied carbonate parameters and hydrographic variables.

Inputs used:

* SST
* SSS
* DIC
* ALK

Outputs derived:

* pH
* [H⁺]

---

## File Structure

Example file naming convention:

* `SST_monthly_climatology_hist_nf_mf_ff_compressed.nc`
* `SSS_monthly_climatology_hist_nf_mf_ff_compressed.nc`
* `DIC_monthly_climatology_hist_nf_mf_ff_compressed.nc`
* `ALK_monthly_climatology_hist_nf_mf_ff_compressed.nc`
* `pH_monthly_climatology_hist_nf_mf_ff_compressed.nc`

Each NetCDF file includes:

* monthly climatology
* compressed storage
* CF-compliant metadata
* global attributes

---

## NetCDF Dimensions

* `period` → 4 periods
* `month` → 12 months
* `LAT_RHO`
* `LON_RHO`

---

## Institution

Indian National Centre for Ocean Information Services, Ministry of Earth Sciences, "Ocean Valley"
Pragathi Nagar (BO), Nizampet (SO),
Hyderabad-500090, India

---

## Contact

* [kunal.c@incois.gov.in](mailto:kunal.c@incois.gov.in)

---


---

## Citation

If you use these datasets, please cite the corresponding study or repository.

---

## Notes

* SST, SSS, DIC, and ALK are directly obtained from ROMS simulations.
* pH and [H⁺] are derived offline using PyCO2SYS.
* Files are compressed using NetCDF4 lossless compression.
