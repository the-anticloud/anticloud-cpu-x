# Independent Insurance — CPU_X

**Project:** CPU_X  
**Category:** LAPTOPS  
**Upstream:** https://github.com/TheTumultuousUnicornOfDarkness/CPU-X  
**Pinned commit:** `bef2c44363f193ff844cfed41ac223a6ea5d57b7`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3`  
**Date:** October 2026

## Why AI-specific cover matters

Deploying AI in a regulated sector creates liability surfaces that ordinary
technology cover does not reach: inference liability, audit-trail liability,
data-breach liability and IP-infringement liability.

## How this project's architecture reduces insurable risk

| Risk | Cloud AI | CPU_X with AIOSS |
|---|---|---|
| Audit-trail loss | high — vendor-controlled logs | low — append-only chain, verifiable offline |
| Data breach in transit | high — data transits external servers | low — no external endpoint |
| Compliance violation | high — cannot satisfy air-gap requirements | low — structural |
| IP liability | moderate | low — pinned provenance chain |

## Evidence package for an insurer

- AIOSS chain verification for head `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3`
- The 16-check register with per-check evidence hashes
- Framework control mapping in `BENCH.json`

## Contact

lois@0-1.gg
