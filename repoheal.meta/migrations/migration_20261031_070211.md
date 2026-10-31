# RepoHeal Migration Document

**Immutable**: this document is an append-only migration record and must not be modified after creation.
**Repository**: ArvindNandigam/Repohealdemo2
**Generated**: 2026-10-31T07:02:04.520970+00:00

---

| Metric | Score |
|--------|------:|
| **Repository Health** | 68/100 |
| **Migration Risk** | 39/100 (LOW) |
| **Average Confidence** | 0.93 |


---

# Migration Assessment

**Repository**: ArvindNandigam/Repohealdemo2
**Generated**: 2026-10-31T07:02:04.520970+00:00
**Overall Health Score**: 68/100
**Migration Risk Score**: 39/100
**Migration Risk Level**: LOW
**Migration Intelligence Status**: SUCCESS

## Executive Summary

- Critical findings: 0
- Deprecated APIs: 1
- Breaking changes: 0

---

## Dependency Inventory

| Dependency | Installed | Latest | Status | Type |
| --- | --- | --- | --- | --- |
| datetime | unknown | 6.0 | missing | detected |
| flask | 3.1.1 | 3.1.3 | declared | third-party |
| pandas | 2.3.3 | 3.1.0 | declared | third-party |
| python-dateutil | unknown | 3.0.0 | missing | detected |
| requests | 2.32.5 | 2.34.2 | declared | third-party |
| typing | unknown | 3.10.0.0 | missing | detected |

---

## Deprecated APIs

### pandas.DataFrame.append
- Library: pandas
- Installed version: 2.3.3
- Latest version: 3.1.0
- Status: deprecated
- Files using: app.py
- Functions using: build_frame
- Deprecated in: 2.0.0

---

## Breaking Changes

### pandas@2.3.3 → 3.1.0
- Library: pandas
- Installed version: 2.3.3
- Latest version: 3.1.0
- Status: at_risk

---

## Migration Paths
- `pandas@2.3.3 → 3.1.0` -> `3.1.0` (major_version_gap, confidence: 0.90)
- `pandas.DataFrame.append` -> `pandas.concat` (deprecated_in_favor_of, confidence: 0.95)

---

## Risk Assessment

### pandas@2.3.3 → 3.1.0
- Risk score: 24/100 (low)
- Affected files: 0 (0.0%)
- Breaking severity: medium
- Replacement confidence: 0.90
- Call chain depth: 0

### pandas.DataFrame.append
- Risk score: 39/100 (low)
- Affected files: 1 (100.0%)
- Breaking severity: low
- Replacement confidence: 0.95
- Call chain depth: 2

---

## Recommended Actions
- [MEDIUM] `pandas.DataFrame.append` (confidence: 0.95): Migrate pandas.DataFrame.append with `pandas.concat` to avoid potential breakage. Impacted files: 1
- [MEDIUM] `pandas@2.3.3 → 3.1.0` (confidence: 0.90): Migrate pandas@2.3.3 → 3.1.0 to avoid potential breakage. Impacted files: 0
