# MMS tripolar Hall-field data and software archive

This repository template organizes the data and software supporting the GRL
manuscript **“Single-X-Line Tripolar Hall Electromagnetic Perturbations During
Strong-Guide-Field Reconnection.”** It separates authoritative MMS mission data
from the derived, figure-level products that must be preserved with a DOI.

## Event definition

- Mission: Magnetospheric Multiscale (MMS)
- Spacecraft: MMS1–MMS4; MMS4 is the primary spacecraft
- Event date: 2016-01-22
- Main plotted interval: 07:18:44–07:18:53 UT
- Coordinate-analysis interval: 07:18:36.860–07:19:00.920 UT
- Instruments: FGM, EDP, FPI/DIS, FPI/DES, and MEC
- Coordinates: LMN; vectors and MVA/timing parameters are stored in
  `metadata/event_parameters.yaml`

## Repository architecture

```text
GRL_MMS_tripolar_data_system/
├── README.md
├── DATA_AVAILABILITY.md
├── RELEASE_CHECKLIST.md
├── CITATION.cff
├── LICENSE-CODE
├── LICENSE-DATA
├── environment.yml
├── config/
│   └── mms_products.yaml
├── metadata/
│   ├── event_parameters.yaml
│   ├── raw_data_manifest.csv
│   └── derived_data_manifest.csv
├── data/
│   ├── raw/README.md
│   ├── interim/README.md
│   └── derived/README.md
├── code/
│   └── README.md
├── notebooks/
│   └── README.md
├── figures/
│   └── README.md
└── scripts/
    ├── download_mms_data.py
    └── verify_archive.py
```

## Storage policy

1. **Raw MMS CDF files are authoritative at the MMS Science Data Center.** Do
   not modify them. Freeze their exact filenames, versions, sizes, and SHA-256
   checksums in `metadata/raw_data_manifest.csv`.
2. **Do not upload a second uncontrolled copy of raw MMS data to the DOI
   archive.** The DOI archive should contain the exact manifest and retrieval
   instructions unless the repository terms and MMS data policy support
   redistribution.
3. **Archive every derived value needed to reproduce a manuscript figure.**
   Store time series and multidimensional products as NetCDF and compact
   relations/tables as CSV.
4. **Keep code versioned.** Develop on GitHub if desired, but create an
   immutable release in Zenodo or another trusted repository and cite its DOI.
5. **Never overwrite a released version.** Create a new tagged release and DOI
   version when data, code, or figures change.

## Reproducibility workflow

```bash
conda env create -f environment.yml
conda activate grl-mms-tripolar



