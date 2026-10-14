# Ethics — CPU_X

**Project:** CPU_X  
**Category:** LAPTOPS  
**Upstream:** https://github.com/TheTumultuousUnicornOfDarkness/CPU-X  
**Pinned commit:** `bef2c44363f193ff844cfed41ac223a6ea5d57b7`  
**Assurance:** 16/16 checks passing  
**Ledger head:** `c4401e7eb00bf2b681bf125ffbf33f28226db8036bf3a30f7e8355d140e253f3`  
**Date:** October 2026

## Position

CPU_X is packaged for offline deployment with a verifiable audit trail. The
ethical questions this raises are answered by making the system's behaviour
checkable rather than by policy statements.

## The four commitments

1. **No hidden egress.** The deployment has no external API dependency; this is
   testable by running it with the network disconnected.
2. **Attributable output.** Every artifact is recorded in a hash chain, so what
   the system produced can be reconstructed.
3. **Operator control.** The institution owns the hardware and the keys.
4. **Refusal to overclaim.** Where a certification is not held, the project says
   so rather than implying it.

## Dual use

This project is packaged for civilian and public-sector deployment. Where an
upstream has dual-use characteristics, the licence gate and the reference-only
marking in `BENCH.json` record that.
