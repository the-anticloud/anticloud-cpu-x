# Students — CPU_X

**Project:** CPU_X  
**Category:** LAPTOPS  
**Upstream:** https://github.com/TheTumultuousUnicornOfDarkness/CPU-X  
**Pinned commit:** `bef2c44363f193ff844cfed41ac223a6ea5d57b7`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3`  
**Date:** October 2026

## What this project gives you

A complete worked example of offline-first packaging with a cryptographic audit
chain: source pinned at `bef2c44363f193ff844cfed41ac223a6ea5d57b7`, a 16-check assurance suite, an evidence register
with per-check hashes, and an AIOSS ledger chain ending at `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3`.

## Learn by verifying

```
python tools/run_bench.py --out BENCH.json
```

Then take any row from `ISOLATED_LAB_RESULTS/03_Result_Register.md`, recompute
the SHA3-256 of its evidence file, and confirm it matches. If it does not match,
the record has been altered — that is the whole point of the chain.

## Licence

Apache 2.0 terms apply to study and teaching use.
