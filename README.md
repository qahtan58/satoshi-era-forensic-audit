# Satoshi-Era Forensic Audit

## Bitcoin Early Block Forensics & Reproducible Research

This repository contains an independent forensic research project focused on historical Bitcoin blockchain data and early-block analysis.

The project is designed around reproducible inspection, documented validation, execution records, and evidence-oriented analysis of early Bitcoin block data.

---

## Scope

The research covers historical Bitcoin blockchain records from the early network period.

The current documented archive covers:

* **Target Scope:** Block heights 1 through 10,000
* **Protocol State:** Frozen v1.4
* **Core Artifact:** `execution_audit_report_ATTEMPT_03.txt` (10,000+ lines of raw verification logs)

---

## F28 — CBigNum Script Matching Analysis

The finalized Version 3 archival report documents the F28 computational reproduction concerning observed coinbase `push[1]` payloads and the historical CBigNum `getvch()` serialization model.

* **F28 Exact Match Count:** **8,713**
* **Tested integer range:** 1 through 199,999 inclusive
* **Observed payload population:** 9,993 unique `push[1]` payloads
* **Match criterion:** exact byte-level equality after CBigNum serialization
* **Report status:** Archived Reference Copy

The result demonstrates a substantial and reproducible byte-level compatibility between the observed `push[1]` payload population and the tested historical CBigNum serialization model.

### Final Report

`Bitcoin_Early_CBigNum_F28_Analysis_Report_v3_Final_260903_172412.pdf`

[View the finalized F28 Technical Research Report](./Bitcoin_Early_CBigNum_F28_Analysis_Report_v3_Final_260903_172412.pdf)

---

## Repository Structure

* `PROJECT_MASTER...`: Master technical specification & scope definition
* `README.md`: Project overview, research scope, and finalized F28 report reference
* `SatoshiVerifierABI.json`: Smart contract ABI for on-chain verification
* `execution_audit_report_ATTEMPT_03.txt`: Raw unaltered audit log output
* `Bitcoin_Early_CBigNum_F28_Analysis_Report_v3_Final_260903_172412.pdf`: Final archival F28 technical research report

---

## Boundaries & Limitations

* The findings represent cryptographic and deterministic block data verification.
* The F28 result is a byte-level computational matching result under the stated serialization model and tested integer range.
* The analysis does not, by the match count alone, establish that every matched `push[1]` payload was historically an ExtraNonce or that CBigNum was the historical source of every matched payload.
* Technical analysis focuses on header validation and serialization patterns without making unverified entity attributions.
