# Educators — CPU_X

**Project:** CPU_X  
**Category:** LAPTOPS  
**Upstream:** https://github.com/TheTumultuousUnicornOfDarkness/CPU-X  
**Pinned commit:** `bef2c44363f193ff844cfed41ac223a6ea5d57b7`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3`  
**Date:** October 2026

## Teaching with CPU_X

The project is usable as a worked example of offline-first packaging with a
cryptographic audit chain. It ships with the assurance suite, the evidence
register and the ledger, so students can verify claims rather than take them on
faith.

## Suggested exercises

1. Run `python tools/run_bench.py --out BENCH.json` and read the 16 results.
2. Recompute the SHA3-256 of a row's evidence file and compare to the register.
3. Walk the AIOSS chain from genesis to head `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3` and confirm every link.
4. Break one artifact and observe the chain fail to verify.

## Licence for teaching

Apache 2.0 terms apply to academic and teaching use. See `24_ANTICOMMONS_LICENSE`.
