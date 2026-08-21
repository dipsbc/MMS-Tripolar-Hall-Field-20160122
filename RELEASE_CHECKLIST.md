# GRL data-release checklist

## Data completeness

- [ ] Exact MMS CDF filenames and versions are recorded.
- [ ] SHA-256 checksum and byte size are recorded for each downloaded CDF.
- [ ] Only data actually used by the analysis are marked `used=yes`.
- [ ] Figure 1 source time series and VDF products are exported.
- [ ] Figure 2 relation/bubble-plot source data are exported.
- [ ] Figures S1–S4 source data are exported.
- [ ] MVA eigenvalues, eigenvectors, interval, timing normal, and speed are saved.
- [ ] Units, coordinates, fill values, cadence, and processing history are documented.

## Software completeness

- [ ] Analysis and plotting scripts are included.
- [ ] Executed notebooks have outputs cleared or intentionally retained.
- [ ] `environment.yml` reproduces the environment.
- [ ] Random seeds are recorded wherever stochastic methods are used.
- [ ] A tagged software version is assigned.
- [ ] Code license is included.

## AGU/GRL readiness

- [ ] Data/software are preserved in a trusted DOI repository.
- [ ] Reviewers have working access at submission.
- [ ] Final DOI, version, license, and development URL replace all `TBD` fields.
- [ ] The Open Research statement is inserted in the manuscript.
- [ ] The DOI archive is cited in the References.
- [ ] Every hyperlink and DOI resolves without author-only credentials.
- [ ] Supporting Information contains figures/method detail, not the only copy
      of research data.

## Scientific consistency

- [ ] `B_M_prime = B_M - B_g` is applied only to the M component.
- [ ] The signed normal speed used for time-to-space conversion is documented.
- [ ] LMN handedness and transformation convention are documented.
- [ ] `J_L = -mu0^-1 dB_M/dN` and `J_M = +mu0^-1 dB_L/dN` sign conventions match
      the adopted LMN system.
- [ ] Figure legends use “central B_M′ region,” not “island,” unless topology is
      independently established.

