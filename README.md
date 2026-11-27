# ThAigis-2P: Two-Party Aigis-sig Threshold Signature

This repository contains the reference implementation and experimental data
for the paper "ThAigis-2P: Two-Party Threshold Signatures from Aigis-sig".

## Contents

- `ThAigis-2P.zip` — full source code and raw results. Unzip it to obtain:
  - `pqm/aigis/` — Aigis-sig core (poly, NTT, packing, rounding), adapted from PQMagic
  - `pqm/hash/keccak/` — FIPS202 SHAKE (byte-verified against Python hashlib)
  - `thaigis/` — two-party threshold signing: ShareGen, HSample, LocalRej,
    challenge/combine, and N/R/C codec
  - `scripts/` — parameter selection, success-rate model, core-SVP estimation
  - `results/` — 29 raw JSON/TXT files underlying Tables 2-9 in the paper

## Build and Run

    unzip ThAigis-2P.zip
    cd ThAigis-2P-impl
    make
    ./bin/bench1 2000 8 1
    python3 scripts/final_params.py

Requires GCC and Linux (getrandom). Python scripts need numpy, scipy, mpmath.

## Data and Code Availability

All data and code supporting this paper are available in this repository and
archived at Zenodo with DOI: <TO-BE-FILLED-AFTER-ZENODO>.

## License

The PQMagic-derived Aigis-sig sources remain under their original license;
all newly written ThAigis-2P code and scripts are released for academic use.
