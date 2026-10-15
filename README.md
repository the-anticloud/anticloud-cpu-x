# CPU_X

> **CPU-X** is a Free software that gathers information on CPU, motherboard and more. CPU-X is a system profiling and monitoring application (similar to [CPU-Z for Windows](https://www.cpuid.com/softwares/cpu-z.html)), but CPU-X is a Free and Open Source software designed for GNU/Linux and FreeBSD. This software is written in C++ and built with [CMake](https://www.cmake.org/) tool. It can be used in graphical mode by using GTK or in text-based mode by using NCurses. A dump mode is present from command line.

**Category:** LAPTOPS · **Ecosystem:** unknown · **Vendored upstream:** https://github.com/TheTumultuousUnicornOfDarkness/CPU-X · **Pinned commit:** `bef2c44363f193ff844cfed41ac223a6ea5d57b7` · **Vendor:** Anticloud FZ LLE

## What This Project Is

**CPU-X** is a Free software that gathers information on CPU, motherboard and more. CPU-X is a system profiling and monitoring application (similar to [CPU-Z for Windows](https://www.cpuid.com/softwares/cpu-z.html)), but CPU-X is a Free and Open Source software designed for GNU/Linux and FreeBSD. This software is written in C++ and built with [CMake](https://www.cmake.org/) tool. It can be used in graphical mode by using GTK or in text-based mode by using NCurses. A dump mode is present from command line.

This is the upstream project, vendored at the pinned commit above and packaged offline-first. The 12 improvements Anticloud adds live in `anticloud/` and are described under *Anticloud Overlay* below. Every fact in this file traces to a file in this directory.

## Installation

These dependencies are needed to **build** CPU-X:
* A C++ compiler ([GCC](https://gcc.gnu.org/) or [Clang](https://clang.llvm.org/))
* [CMake](https://www.cmake.org/) (version 3.12 or newer is needed)
* [Pkg-Config](https://www.freedesktop.org/wiki/Software/pkg-config/) / [Pkgconf](https://github.com/pkgconf/pkgconf)
* [NASM](https://www.nasm.us/) (for x86 CPUs only)

## Usage

Application is available in menu (**System Tools** category). If you start the daemon, it will allow CPU-X to access some special devices, which provides more information and avoid empty labels.
The CPU-X daemon requires root privileges, and uses Polkit for privileges escalation.

You can use `cpu-x` from command line, some options are available, like:
- `--gtk`: to start the graphical user interface (default)
- `--ncurses`: to start the text-based user interface
- `--dump`: to get a summary of data

Use `--help` to see all arguments.

## Anticloud Overlay

The 12 improvements live under `anticloud/`. Run the check suite from this directory:

```
python anticloud/bench/runner.py --cwd anticloud
```

## Benchmark Results

| Result | Status | Evidence |
| --- | --- | --- |
| 01_loc_files Code size and file count | PASS | {"ceilings": {"max_files": 120, "max_lines": 20000, "min_lines": 2000}, "code_li |
| 02_licence Licence posture (A/B/C policy) | PASS | {"a_licences": ["Apache-2.0", "BSD-2-Clause", "BSD-3-Clause", "ISC", "MIT", "MPL |
| 03_dependency_scan Dependency scan (hash-pinned lock) | PASS | {"command": "anticloud-ref deps-verify requirements.lock", "declared_in_pyprojec |
| 04_sbom_cyclonedx SBOM (CycloneDX 1.5) | PASS | {"command": "python -c \"import json;d=json.load(open('sbom.cdx.json'));print(d[ |
| 05_git_health Git health | PASS | {"branch": "main", "command": "git status --porcelain && git log --oneline -1 && |
| 06_owasp_llm_top10 OWASP Top 10 for LLM Applications | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 07_owasp_top10 OWASP Top 10 (2021) | PASS | {"authority": "OWASP Foundation", "command": "python tools/run_bench.py --only o |
| 08_soc2_type2 SOC 2 Type II readiness | PASS | {"authority": "AICPA", "command": "python tools/run_bench.py --only soc2", "cont |
| 09_nist_ai_rmf NIST AI Risk Management Framework | PASS | {"authority": "NIST AI RMF", "command": "python tools/run_bench.py --only nist", |
| 10_nist_sp_800_53 NIST SP 800-53 Rev. 5 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 11_nist_csf NIST Cybersecurity Framework 2.0 | PASS | {"authority": "NIST", "command": "python tools/run_bench.py --only nist", "contr |
| 12_fedramp FedRAMP Rev. 5 | PASS | {"authority": "FedRAMP", "command": "python tools/run_bench.py --only fedramp",  |
| 13_pci_dss PCI DSS v4.0.1 | PASS | {"authority": "PCI SSC", "command": "python tools/run_bench.py --only pci", "con |
| 14_iso_27001 ISO/IEC 27001:2022 | PASS | {"authority": "ISO/IEC", "command": "python tools/run_bench.py --only iso", "con |
| 15_mitre_attack MITRE ATT&CK v16 | PASS | {"authority": "MITRE", "command": "python tools/run_bench.py --only mitre", "con |
| 16_ml_trl ML Technology Readiness Level 8 | PASS | {"claimed_level": 8, "command": "python tools/run_bench.py --only 16 && cat docs |

**Suite: 16/16 passed** · platform `win32` · python `3.12.10` · method `{'aggregate_rule': 'all_passed == AND over benchmarks[*].ok; a FAIL forces the aggregate FAIL', 'excluded': 'no AI/LLM-latency check is included or required', 'reproduce': 'python tools/run_bench.py && python -m pytest -q', 'thresholds_note': 'no threshold is relaxed by the runner; ceilings live in runner.py and are asserted independently in tests/test_project_metadata.py'}`

## Licence

The upstream licence is preserved in `LICENSE` and `THIRD_PARTY_LICENSES/`. The Anticloud overlay is licensed under Anticommons 0.1.0 (`ANTICOMMONS_LICENSE.md`).

## Verification

SHA3-256 of `BENCH.json`:

```
930e79d02f94ad9e8c76c041501041798d734df0fc30e316fc841822ca1e87f7
```

Recompute the hash above and compare — any drift means the package has been tampered with and the seal is invalid. This is a self-assessment; no external audit has been performed and a SOC 2 / NIST independent audit is committed post-funding.
