# Indian-Ocean-Acidification-Future-Projection

# Indian Ocean Surface pH Dataset (1980–2100)

## Overview

This repository contains **monthly interannual surface ocean pH data for the Indian Ocean**, prepared from **ROMS simulations** for historical and future periods.

The dataset is organized into four continuous simulation periods:

* **hist** → 1980–2014
* **nf** → 2015–2040 (Near Future)
* **mf** → 2041–2070 (Mid Future)
* **ff** → 2071–2100 (Far Future)

Each file preserves the full **monthly interannual time series** for the corresponding period.

---

## Available Variable

### Surface carbonate chemistry variable

* **Surface pH**

---

## Carbonate System Calculation

Surface pH was calculated offline using **PyCO2SYS** from ROMS-derived carbonate system variables.

### Inputs used

* Sea Surface Temperature (**SST**)
* Sea Surface Salinity (**SSS**)
* Dissolved Inorganic Carbon (**DIC**)
* Total Alkalinity (**ALK**)

### Output derived

* Surface pH

---

## Carbonate Chemistry Solver

**PyCO2SYS**

PyCO2SYS solves the marine carbonate system using thermodynamic equilibrium equations based on supplied carbonate parameters and hydrographic variables.

---

## File Structure

Files are provided separately for each period:

* `pH_monthly_interannual_hist.nc`
* `pH_monthly_interannual_NF.nc`
* `pH_monthly_interannual_MF.nc`
* `pH_monthly_interannual_FF.nc`

Each NetCDF file includes:

* monthly interannual time series
* compressed storage
* CF-compliant metadata
* global attributes

---

## NetCDF Dimensions

* `time`
* `LAT_RHO`
* `LON_RHO`

---

## Institution

Indian National Centre for Ocean Information Services
Ministry of Earth Sciences
"Ocean Valley", Pragathi Nagar (BO), Nizampet (SO)
Hyderabad-500090, India

---

## Contact

* [kunal.c@incois.gov.in](mailto:kunal.c@incois.gov.in)

---

## Citation

If you use these datasets, please cite the corresponding study or repository.

---

## Notes

* Surface pH is derived offline using PyCO2SYS from ROMS ensemble outputs.
* Files preserve full monthly interannual variability.
* NetCDF files are compressed using lossless NetCDF4 compression.
