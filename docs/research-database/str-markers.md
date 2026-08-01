---
title: "STR Marker Database: Microsatellite Markers for Pigeon Identification"
description: "STR marker database for pigeon DNA fingerprinting: microsatellite marker properties, polymorphism, exclusion probability, and applications in parentage verification."
---

# STR Marker Database: Microsatellite Markers for Pigeon Identification

<div class="abstract-box">
<p><strong>Abstract:</strong> This database entry documents short tandem repeat (STR) microsatellite markers used for DNA fingerprinting in pigeons — marker properties, polymorphism levels, combined exclusion probability, and applications in individual identification and parentage verification.</p>
</div>

## STR Marker Overview

| Field | Value |
|-------|-------|
| Marker Type | Short tandem repeat (microsatellite) |
| Repeat Unit | Di-, tri-, tetra-nucleotide motifs |
| Genome Location | Nuclear genome, distributed across chromosomes |
| Inheritance | Co-dominant, Mendelian |
| Mutation Rate | 10⁻³–10⁻⁴ per locus per generation |
| Diagnostic Utility | Individual identification, parentage verification |

## Marker Panel Design

| Parameter | Recommended |
|-----------|-------------|
| Loci per panel | 12–20 |
| Allele number per locus | ≥ 5 (ideally ≥ 8) |
| Observed heterozygosity | ≥ 0.6 |
| Null allele frequency | < 0.05 |
| Combined exclusion probability | > 99.99% |

$$\text{Combined } P_E = 1 - \prod_{i=1}^{n} (1 - P_{E,i})$$

## Applications

| Application | Marker Requirement | Output |
|-------------|--------------------|--------|
| Parentage verification | 12–20 loci, high polymorphism | Exclusion/confirmation + LR |
| Individual identification | 12–20 loci | Unique profile (match probability) |
| Population genetics | 15–30 loci, population-validated | Heterozygosity, FST |
| Inbreeding monitoring | Genome-wide or dense panel | ROH, inbreeding coefficients |

See [DNA Fingerprinting in Racing Pigeons](../racing-pigeon-genetics/dna-fingerprinting-racing-pigeons.md) for the full methodology.

## Match Probability

For an individual profile, the random match probability is:

$$P(\text{match}) = \prod_{i=1}^{n} \left( 2 p_i p_j \text{ or } p_i^2 \right)$$

Where $p_i$, $p_j$ are allele frequencies. With 15 loci, match probabilities typically fall below 10⁻¹⁵ — far below the world pigeon population.

## Marker Validation Requirements

| Validation Step | Purpose |
|-----------------|---------|
| Hardy-Weinberg equilibrium test | Population validity |
| Linkage disequilibrium check | Independence of loci |
| Null allele assessment | Avoid false exclusions |
| Species specificity | Confirm amplification in Columba livia |
| Reproducibility study | Allele calling consistency |

## STR Marker Biology and Mutation

Microsatellites arise from **replication slippage** — during DNA replication, the polymerase can slip on repetitive motifs, adding or deleting repeat units. This mechanism explains their key properties:

| Property | Value | Implication |
|----------|-------|-------------|
| Mutation rate | 10⁻³–10⁻⁴ per locus per generation | Higher than SNPs (10⁻⁸) |
| Mutation model | Stepwise (add/delete one repeat) | Allele size-based analysis valid |
| Mutation bias | Slight expansion bias in birds | Rare size shifts across generations |
| Allele range | Typically 80–400 bp (after primer design) | Compatible with capillary electrophoresis |

The stepwise mutation model has an important practical consequence: alleles differing by one repeat unit are more closely related than alleles differing by many units. This affects genetic distance calculations and the interpretation of allele-sharing in parentage analysis — closely related individuals share alleles by descent, not just by chance.

## Marker Discovery and Development Process

Developing a validated pigeon STR panel follows a structured pipeline:

| Step | Description | Output |
|------|-------------|--------|
| 1. Library construction | Shotgun or enriched genomic library | Sequence reads with repeats |
| 2. Repeat identification | Bioinformatics scan for microsatellite motifs | Candidate loci (hundreds) |
| 3. Primer design | Flanking primers for each candidate | Primer pairs |
| 4. Pilot screening | Test on small panel of individuals | Polymorphic markers |
| 5. Population validation | Genotype larger population | Allele frequencies, HWE |
| 6. Panel assembly | Select loci meeting criteria | Final validated panel |
| 7. Reproducibility study | Repeat genotyping | Allele-calling consistency |

Cross-species transfer of pigeon markers to other Columbidae species (doves) is often possible but requires re-validation — primer binding sites may differ.

## Population Genetic Statistics in Detail

### Hardy-Weinberg Equilibrium (HWE)

For a locus with alleles $p_i$, expected heterozygosity under HWE:

$$H_e = 1 - \sum p_i^2$$

Deviation from HWE signals:

| Deviation | Possible Cause | Action |
|-----------|----------------|--------|
| Heterozygote deficit | Inbreeding, null alleles, population structure | Investigate null alleles; check sampling |
| Heterozygote excess | Outbreeding, recent admixture | Verify sampling design |
| Significant HWE departure | Locus problems | Consider excluding the locus |

### Polymorphism Information Content (PIC)

PIC measures a marker's informativeness:

$$PIC = 1 - \sum p_i^2 - \sum_{i<j} 2 p_i^2 p_j^2$$

| PIC Value | Informativeness |
|:---:|----------------|
| > 0.7 | Highly informative |
| 0.5–0.7 | Moderately informative |
| < 0.5 | Poorly informative — consider replacement |

A validated pigeon panel should consist predominantly of highly informative loci (PIC > 0.7) to maximize exclusion power per marker.

### Null Alleles

Null alleles fail to amplify due to primer-binding site mutations, causing apparent homozygosity:

| Null Allele Frequency | Severity | Action |
|:---:|-----------|--------|
| < 0.05 | Acceptable | Monitor |
| 0.05–0.10 | Caution | Consider redesign of primers |
| > 0.10 | Problematic | Redesign primers or drop locus |

Null alleles in parentage analysis create false exclusions — a parent that appears to share no allele with a chick may actually carry a null allele. Software (e.g., CERVUS, ML-Relate) estimates null allele frequencies and accounts for them.

## Worked Example: Computing Combined Exclusion Probability

Consider a panel of 15 loci with single-parent exclusion probabilities as follows (typical values for pigeon microsatellites):

| Locus | Alleles | PE (single parent) |
|:---:|:---:|:---:|
| 1 | 9 | 0.58 |
| 2 | 10 | 0.61 |
| 3 | 8 | 0.55 |
| 4 | 11 | 0.63 |
| 5 | 7 | 0.52 |
| 6 | 9 | 0.58 |
| 7 | 12 | 0.65 |
| 8 | 8 | 0.55 |
| 9 | 10 | 0.61 |
| 10 | 9 | 0.58 |
| 11 | 6 | 0.47 |
| 12 | 8 | 0.55 |
| 13 | 10 | 0.61 |
| 14 | 7 | 0.52 |
| 15 | 9 | 0.58 |

Combined single-parent exclusion probability:

$$P_E = 1 - \prod (1 - P_{E,i}) \approx 1 - (0.42 \times 0.39 \times ...) \approx 0.99996$$

With both parents tested, the combined exclusion probability exceeds 0.999999 — effectively certain exclusion of falsely assigned parents.

## Genotyping Workflow and Quality

| Step | Method | Quality Check |
|------|--------|---------------|
| DNA extraction | Spin-column | Yield, purity |
| Multiplex PCR | 5–6 loci per dye channel | Positive/negative controls |
| Fragment analysis | Capillary electrophoresis | Size standard in every injection |
| Allele calling | Software (e.g., GeneMapper, Geneious) | Bin editing, stutter filtering |
| Data export | LIMS integration | Sample-locus cross-check |

### Stutter Peaks and Their Management

PCR of STR loci produces **stutter artifacts** — peaks one repeat unit shorter than the true allele (from slippage during early PCR cycles). Stutter complicates calling:

| Stutter Ratio | Handling |
|:---:|-----------|
| < 15% of main peak | Ignore (typical) |
| 15–30% | Caution; use validated bins |
| > 30% | Consider alternate locus or redesign |

Software-based genotyping with validated bin sets manages stutter reliably; manual calling should be double-reviewed.

## Database Applications in Practice

### Parentage Verification Cases

| Case Type | Panel Requirement | Typical Outcome |
|-----------|-------------------|-----------------|
| Sire exclusion | 12–20 loci | Exclusion at ≥ 2 loci → excluded |
| Full parentage (sire + dam) | 15–20 loci | Combined PE > 99.99% |
| Half-sib verification | 20+ loci | Higher power needed for sibship |
| Identity match | 15+ loci | Random match < 10⁻¹² |

### Individual Identification Statistics

The random match probability for a 15-locus profile (all heterozygous, allele frequencies ~0.1):

$$P(\text{match}) = \prod 2 p_i p_j = (2 \times 0.1 \times 0.1)^{15} \approx 2 \times 10^{-15}$$

Far below the global pigeon population (~5 × 10⁸) — profiles are effectively unique.

### Inbreeding Monitoring

| Metric | Calculation | Use |
|--------|-------------|-----|
| FIS (within-population inbreeding) | 1 - Ho/He | Loft-level inbreeding |
| Pairwise relatedness | Queller-Goodnight or Lynch-Ritland | Mate selection |
| ROH (with SNP data) | Genomic runs of homozygosity | Genome-wide inbreeding |

Pairwise relatedness values guide mate selection: avoiding matings with relatedness > 0.125 (first cousins or closer) preserves diversity.

## References

1. Jamieson, A.; Taylor, S. S. Comparisons of three probability formulae for parentage exclusion. *Animal Genetics* 1997;28(6):397-400. DOI: 10.1111/j.1365-2052.1997.00186.x
2. Presti, F. T.; Wasko, A. P. A review of microsatellite markers and their applications in birds. *Genetics and Molecular Research* 2014;13(1):2152-2164. DOI: 10.4238/2014.March.31.2
3. Trachtulec, Z.; Vyleťal, P. et al. Genetic variation of the domestic pigeon (Columba livia). *Folia Zoologica* 2010;59(1):11-17

---

Return to [Research Database Overview](index.md) or read [CHD Gene Database](chd-gene.md).
