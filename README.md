# MMS Tripolar Hall-Field Event: 22 January 2016

Data products, analysis materials, and figure outputs supporting a study of a
tripolar Hall electromagnetic structure observed by the Magnetospheric
Multiscale (MMS) mission during strong-guide-field reconnection at Earth's
dayside magnetopause.

The repository accompanies the GRL manuscript provisionally titled
**â€œSingle-X-Line Tripolar Hall Electromagnetic Perturbations During
Strong-Guide-Field Reconnection.â€**

## Event summary

- **Date:** 22 January 2016
- **Principal interval:** 07:18:44â€“07:18:53 UT
- **Coordinate-analysis interval:** 07:18:36.860â€“07:19:00.920 UT
- **Spacecraft:** MMS1â€“MMS4
- **Primary spacecraft:** MMS4
- **Instruments:** FGM, EDP, FPI/DIS, FPI/DES, and MEC
- **Coordinate system:** LMN transformed from GSE
- **Representative guide field:** approximately 35 nT
- **Hall perturbation:** \(B'_M=B_M-B_g\)

The event contains a positiveâ€“negativeâ€“positive sequence in \(B'_M\), together
with structured normal electric fields and multilayer Hall currents across an
ion-scale reconnection exhaust.

## Repository contents

```text
MMS-Tripolar-Hall-Field-20160122/
â”œâ”€â”€ README.md
â”œâ”€â”€ DATA_AVAILABILITY.md
â”œâ”€â”€ RELEASE_CHECKLIST.md
â”œâ”€â”€ LICENSE-CODE
â”œâ”€â”€ LICENSE-DATA
â”œâ”€â”€ environment.yml
â”œâ”€â”€ config/
â”‚   â””â”€â”€ mms_products.yaml
â”œâ”€â”€ data/
â”‚   â””â”€â”€ derived/
â”‚       â”œâ”€â”€ 20160122071714_all_mms_plot_data.xlsx
â”‚       â”œâ”€â”€ 20160122071714_event_times.csv
â”‚       â”œâ”€â”€ lmn_values.csv
â”‚       â”œâ”€â”€ mms4_LMN.xlsx
â”‚       â””â”€â”€ ohms_terms_mms4.xlsx
â”œâ”€â”€ figures/
â”‚   â””â”€â”€ manuscript and supporting PDF figures
â”œâ”€â”€ metadata/
â”‚   â”œâ”€â”€ MMS_source_files.csv
â”‚   â”œâ”€â”€ MMS_source_files.md
â”‚   â”œâ”€â”€ derived_data_manifest.csv
â”‚   â”œâ”€â”€ event_parameters.yaml
â”‚   â””â”€â”€ raw_data_manifest.csv
â””â”€â”€ notebooks/
    â””â”€â”€ 20160122071714.ipynb
```

## Source MMS data

The original Level-2 MMS CDF files were obtained from the
[NASA Space Physics Data Facility (SPDF)](https://spdf.gsfc.nasa.gov/pub/data/mms/).
They are not intended to be duplicated in this repository. Exact filenames,
versions, product directories, and direct SPDF download links for MMS1â€“MMS4
are provided in:

- [`metadata/MMS_source_files.md`](metadata/MMS_source_files.md): clickable,
  human-readable file list.
- [`metadata/MMS_source_files.csv`](metadata/MMS_source_files.csv):
  machine-readable source manifest.

The event date is 22 January 2016; therefore, the relevant SPDF directories use
`2016/01/`, not `2017/01/`.

## Derived data and figures

The `data/derived/` directory contains compact products used in the analysis,
including LMN-transformed quantities, event boundaries, Ohm's-law terms, and
figure-level data. The `figures/` directory contains the corresponding
manuscript and supporting figure outputs.

Publication figures alone are not considered numerical source data. Before the
archival release, each manuscript figure should have a corresponding CSV,
NetCDF, or documented spreadsheet from which the plotted values can be
recovered.

## Coordinate and timing parameters

The adopted coordinate and timing results are recorded in
[`metadata/event_parameters.yaml`](metadata/event_parameters.yaml). The main
parameters include:

- MVA eigenvalues: 1281.045, 106.188, and 4.960 nTÂ²
- Eigenvalue ratios: 12.064 and 21.410
- Mean interspacecraft separation: 18.8 km
- Tetrahedron quality factor: 0.80
- Timing normal speed: âˆ’46.8 km sâ»Â¹
- Angle between timing and MVA normals: 4.8Â°

The sign of the timing speed must be interpreted consistently with the adopted
LMN convention when converting temporal derivatives to spatial gradients.

## Reproducing the analysis

Create the software environment:

```bash
conda env create -f environment.yml
conda activate grl-mms-tripolar
```

Then open:

```text
notebooks/20160122071714.ipynb
```

The notebook should be run only after the source CDF files have been downloaded
from the links in `metadata/MMS_source_files.md`. Local raw-data paths should
be configured through `config/mms_products.yaml` rather than embedded as
machine-specific absolute paths.

## Data-storage policy

- Original MMS CDF files remain available from NASA SPDF.
- GitHub stores analysis code, metadata, compact derived products, and figures.
- The versioned release and complete derived-data package will be preserved in
  Zenodo.
- Raw `*.cdf` files should be excluded from Git tracking through `.gitignore`.
- Released files must not be overwritten; substantive updates should receive a
  new version.

## Citation

Until the Zenodo release is published, cite the GitHub repository as:

> Budhathoki, D., & Qiu, S. (2026). *MMS Tripolar Hall-Field Event: 22 January
> 2016* (Version 1.0.0) [Data set and software]. GitHub.
> https://github.com/dipsbc/MMS-Tripolar-Hall-Field-20160122

After publication of the Zenodo record, replace the GitHub-only citation with
the formal DOI-bearing citation generated by Zenodo.

## Licenses

- Analysis code: see [`LICENSE-CODE`](LICENSE-CODE) (MIT License).
- Derived data and documentation: see [`LICENSE-DATA`](LICENSE-DATA)
  (CC BY 4.0).

## Repository status

This repository is under preparation for its first archival release. Verify
all source-file versions, remove unintended raw CDF copies, complete the
derived-data manifest, and replace any remaining DOI placeholders before
creating release `v1.0.0`.
