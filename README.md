## Technical Update (13 May 2025)
### V Predoi and the TLT (Technical Lead Team)

- [Workshop Agenda](https://github.com/ESMValGroup/Community/discussions/215)

### So far...(since the last workshop)

- New ESMValTool releases since the last workshop:
  - [many thanks Emma for v2.11](https://docs.esmvaltool.org/projects/ESMValCore/en/latest/changelog.html#v2-11-0):
    - a decent amount of optimization via making preprocessors lazy and allowing for caching
    - also, optimal data loading (ie once!) for ESMPy regridding
    - support for Python 3.12 and Numpy 2+
  - [many thanks Saskia for v2.12](https://docs.esmvaltool.org/projects/ESMValCore/en/latest/changelog.html#v2-12-0):
    - overhauling configuration, make it more accessible and modular
    - multiple Dask configuration improvements
    - support for Python 3.13
- Main focus so far was making preprocessors lazy and determine optimal Dask settings to run
  heavy computations: many thanks to all who worked on that, especially Bouwe and Manuel!
  Have a look at the paper on it [Manuel et al](https://gmd.copernicus.org/preprints/gmd-2024-236/)
- Particularily involved maintenance with Python 3.13 and Numpy 2.0 being fairly fussy
- lots of new contributions in data fixing and OBS handling/cmorization,
  new ins in Intake (thanks to Romain and his troop)
- Recipe Test Workflow (RTW) is deployed, and was actually used for v2.12 (Emma and her troop)
- Other serious technical improvements:
  - moved to Ruff + Pre-commit - we are still working on including more ruff rules
  - we now have a `codacy-ruff` app

### To be done in the foreseeable future

- have a look at the [discussion point](https://github.com/ESMValGroup/Community/discussions/187)
- CMIP7 + new ESGF infrastructure (STAC) [EGU2025 abstract](https://meetingorganizer.copernicus.org/EGU25/EGU25-19453.html)
- fixes be taken out and made a package of its own (with `xarray` or `cf-python`)
- optimal handling of our complex ESMValTool environment (split/Pixi/ask grandma etc)
  - finally have a sustainable strategy for supporting new releases of major dependencies
- support for new file formats and architectures (Zarr, object storage etc)
