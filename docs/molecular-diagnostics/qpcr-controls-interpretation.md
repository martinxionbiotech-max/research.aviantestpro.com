---
title: "Controls in Avian qPCR: Types, Functions and Interpretation Rules"
description: "Controls in avian qPCR: positive, negative, internal controls and extraction blanks; their functions, failure interpretation, and mandatory reporting rules for valid results."
---

# Controls in Avian qPCR: Types, Functions and Interpretation Rules

<div class="abstract-box">
<p><strong>Abstract:</strong> Controls are the difference between a qPCR result and a valid qPCR result. This article explains the four control types used in avian diagnostics — positive controls, negative controls, internal controls, and extraction blanks — their scientific functions, how to interpret control failures, and the reporting rules that make results defensible.</p>
</div>

## Why Controls Are Non-Negotiable

Every qPCR run produces data — but only runs with valid controls produce **interpretable** data. Without controls, a negative result could mean "no pathogen" or "failed reaction"; a positive result could mean "infection" or "contamination." Controls disambiguate these possibilities.

| Control | Answers the Question |
|---------|---------------------|
| Positive control | "Did the reaction work?" |
| Negative control | "Is the result clean?" |
| Internal control | "Did this sample contain amplifiable DNA?" |
| Extraction blank | "Was the extraction process clean?" |

## The Four Control Types

### 1. Positive Control

A known target (inactivated virus, plasmid, or synthetic RNA/DNA standard) that must amplify in every run.

| Feature | Requirement |
|---------|-------------|
| Placement | One per plate (ideally one per assay per plate) |
| Material | Inactivated virus or quantified plasmid standard |
| Expected Ct | Within a defined range (e.g., ± 2 Ct of reference) |
| Failure action | Entire run invalid — investigate reagents/cycler |

### 2. Negative Control (No-Template Control)

Water or buffer instead of template — must produce no amplification.

| Feature | Requirement |
|---------|-------------|
| Placement | At least one per plate; more for high-throughput |
| Failure | Any amplification = contamination → run invalid |
| Investigation | Check reagents, tips, work area, amplicon carryover |

### 3. Internal Control (IC)

A co-amplified target (avian β-actin, 18S rRNA, or a synthetic spiked sequence) present in every sample reaction.

| Feature | Requirement |
|---------|-------------|
| Chemistry | Same tube (multiplex) or parallel reaction |
| Function | Proves DNA was present and amplification was not inhibited |
| Failure in a sample | That sample's negative result is INVALID — re-extract or dilute |
| Failure in all samples | Reagent or extraction batch problem |

### 4. Extraction Blank

A tube processed through the entire extraction workflow containing no sample.

| Feature | Requirement |
|---------|-------------|
| Placement | One per extraction batch (e.g., per 96-well plate) |
| Function | Detects cross-contamination during extraction |
| Failure | Batch-level contamination — all samples from that batch suspect |

## Interpretation Rules: The Decision Table

| IC (sample) | NTC | Positive Control | Pathogen Signal | Valid Result? |
|:---:|:---:|:---:|:---:|:---:|
| OK | Negative | OK | Negative | ✅ Valid negative |
| OK | Negative | OK | Positive | ✅ Valid positive |
| Failed | Negative | OK | Negative | ❌ Invalid — re-extract/dilute |
| OK | **Positive** | OK | Any | ❌ Invalid — contamination |
| OK | Negative | **Failed** | Negative | ❌ Invalid — run failure |
| OK | Negative | OK | Borderline (Ct 38–40) | ⚠️ Repeat; report as inconclusive |

**The golden rule:** a result is reportable only when ALL controls behave correctly. Any exception must be documented, and the sample retested.

## Designing a Control Strategy

### Placement Optimization

| Plate Size | Recommended Layout |
|:---:|-------------------|
| 96-well | 2 NTC, 2 positive controls (different targets), 1 extraction blank |
| 384-well | 4 NTC, 4 positive controls, 2 extraction blanks |
| Every sample | IC in each well (multiplex format) |

### The IC Dilution Trap

An IC that is too abundant can outcompete the pathogen target at low copy numbers — masking a weak positive. IC concentration should be titrated so that:

1. IC Ct is stable (e.g., 24–28) across the plate
2. IC amplification does NOT suppress pathogen detection at the assay LOD
3. IC and target Ct separation is at least 5 cycles at target LOD

## Worked Example: A Contaminated Plate

A 96-well plate with 90 clinical samples yields the following controls:

| Control | Result |
|---------|--------|
| NTC well 1 | **Positive (Ct 33)** |
| NTC well 2 | Negative |
| Positive control | Ct 24 (expected 23–25) ✅ |
| Extraction blank | Negative |

Interpretation: one NTC positive indicates sporadic contamination — possibly a pipetting event or a contaminated tip. The run is declared **invalid for interpretation**; all 90 samples are retested. Investigation identifies a splash event during plate setup. Corrective actions: centrifuge tubes before opening, fresh gloves, revised pipetting technique. The retest is clean.

This example shows the correct behavior: **one NTC positive invalidates the entire run** — selective interpretation ("the positive samples are probably real") is scientifically indefensible.

## Reporting Controls in Results

Every report should state control outcomes explicitly:

| Report Field | Example |
|--------------|---------|
| Positive control Ct | "PBFD positive control Ct 24.1 (reference 23–25)" |
| NTC | "Negative — no amplification" |
| IC (per sample) | "β-actin IC Ct 26.3 — within range" |
| Extraction blank | "Negative" |
| Conclusion | "Result valid; sample negative for PBFV DNA" |

Transparent control reporting distinguishes a professional laboratory and is increasingly expected by accreditation bodies and informed clients.

## Control Failure Investigation Protocol

When a control fails, follow a defined investigation path rather than repeating the run blindly:

| Control Failure | Immediate Check | Next Step |
|-----------------|-----------------|-----------|
| NTC positive | Inspect pipetting technique, fresh tips | Decontaminate area; repeat with new reagents |
| Positive control weak/late | Check reagent expiry, storage | Prepare fresh master mix; verify standard |
| IC failure in one sample | Check sample quality, inhibition | Dilute 1:5 or re-extract |
| IC failure in many samples | Check extraction batch, reagents | Re-extract batch; verify lysis buffer |
| Extraction blank positive | Check extraction workflow | Clean hood; new reagents; repeat batch |

### The 10% Rule for Repeat Testing

A pragmatic quality threshold: if more than 10% of samples in a run show any control anomaly (IC failure, borderline Ct, replicate disagreement), treat the entire run as suspect and repeat it. Intermittent single-sample issues are expected; systemic patterns are not.

## Automated Control Monitoring

Modern qPCR software can automate control monitoring:

| Feature | Benefit |
|---------|----------|
| Automatic IC range checking | Flags out-of-range IC per well |
| Plate-wide NTC alarms | Immediate contamination alerts |
| Positive control trending | Early warning of reagent degradation |
| Real-time result gating | Only reports results when controls pass |
| Audit trails | Complete run documentation |

Automation removes operator subjectivity from validity decisions — the software enforces the same rules every time. Combined with LIMS integration, it creates the full traceability that accreditation requires.

## A Realistic Example: Run Acceptance Criteria

Before any results are released, the run must pass acceptance criteria. A typical acceptance checklist:

| Criterion | Pass Condition |
|-----------|----------------|
| Positive controls | Ct within ± 2 of reference for all targets |
| NTCs | No amplification (or Ct > 40 with no curve) |
| Extraction blanks | No amplification |
| IC pass rate | ≥ 95% of samples; failed ones flagged |
| Standard curve (if quantitative) | Efficiency 90–110%, R² > 0.98 |
| Replicate agreement | Ct range ≤ 1.0 (triplicates) |
| Sample IDs | All match submission form |

A run that fails any criterion is either repeated or partially repeated with the affected samples — never released with "acceptable exceptions." This discipline is what separates reliable avian diagnostics from guesswork, and it is exactly the standard that accreditation bodies and informed clients expect.

## Key Takeaways

- Controls answer four questions: did the reaction work, is it clean, was DNA present, was extraction clean?
- A negative without IC amplification is invalid — never report it.
- A positive NTC invalidates the entire run — retest everything.
- IC concentration must not suppress pathogen detection at the LOD.
- Every report should document control outcomes.
- Control discipline is the hallmark of a defensible diagnostic laboratory.

## References

1. Bustin, S. A.; Benes, V. et al. The MIQE guidelines: Minimum information for publication of quantitative real-time PCR experiments. *Clinical Chemistry* 2009;55(4):611-622. DOI: 10.1373/clinchem.2008.112797. PubMed ID: 19246619
2. Borst, A.; Box, A. T.; Fluit, A. C. False-positive results and contamination in nucleic acid amplification assays. *European Journal of Clinical Microbiology & Infectious Diseases* 2004;23(4):289-299. DOI: 10.1007/s10096-004-1107-4
3. Raidal, S. R.; Riddoch, P. A. Detection of beak and feather disease virus by PCR. *Avian Pathology* 1997;26(3):679-682. DOI: 10.1080/03079459708419244

---

Return to [Molecular Diagnostics Overview](index.md) or read [qPCR Technology in Avian Disease Detection](qpcr-avian-disease-detection.md).
