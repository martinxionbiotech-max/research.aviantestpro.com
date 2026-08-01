---
title: "CHD Gene Database: Avian Sex Determination Reference"
description: "CHD gene database for avian sex determination: gene name, chromosome location, function, testing application, related species, and references."
---

# CHD Gene Database: Avian Sex Determination Reference

<div class="abstract-box">
<p><strong>Abstract:</strong> This database entry provides structured reference data on the CHD (Chromo-Helicase-DNA binding) gene, the standard molecular marker for avian sex determination — including gene name, chromosomal location, molecular function, testing applications, and species coverage.</p>
</div>

## Gene Record

| Field | Value |
|-------|-------|
| Gene Name | CHD1 (Chromo-Helicase-DNA binding protein 1) |
| Aliases | CHD-Z (Z-linked), CHD-W (W-linked) |
| Chromosome | Z chromosome (CHD-Z); W chromosome (CHD-W) |
| Gene Type | Protein-coding |
| Protein Function | Chromatin remodeling; transcriptional regulation |
| Molecular Weight (protein) | ~240 kDa |
| Diagnostic Utility | Sex determination in birds |

## Chromosomal Context

| Copy | Location | Present In | Diagnostic Product |
|------|----------|------------|-------------------|
| CHD-Z | Z chromosome | Males (ZZ) and females (ZW) | Larger intron amplicon |
| CHD-W | W chromosome | Females only (ZW) | Smaller intron amplicon |

The intron length difference between CHD-Z and CHD-W is the basis of PCR-based sex testing: one band = male, two bands = female. See [CHD Gene in Avian Sex Determination](../avian-genetics/chd-gene-sex-determination.md) for the full protocol.

## Testing Application

| Parameter | Detail |
|-----------|--------|
| Assay type | PCR (end-point) or qPCR with melt analysis |
| Amplicon size | 400–700 bp (species-dependent) |
| Sample | Feather calamus, blood, buccal swab |
| Interpretation | 1 band = ZZ (male); 2 bands = ZW (female) |
| Controls required | Male/female reference DNA, NTC, internal control |

## Related Species

The CHD-based test has been validated in a broad range of avian species:

| Species Group | Examples |
|---------------|----------|
| Columbiformes | Domestic pigeon, dove species |
| Psittaciformes | Parrots, cockatoos, budgerigars |
| Falconiformes | Falcons, hawks, eagles |
| Passeriformes | Songbirds, finches |
| Galliformes | Chickens, pheasants |
| Strigiformes | Owls |

## Detailed Gene Annotation

The CHD1 gene (also annotated CHD1L in some avian genome assemblies) spans approximately 85 kb of genomic DNA sequence and comprises multiple exons. Its protein product contains conserved functional domains:

| Domain | Function |
|--------|----------|
| Chromodomain (2×) | Binds methylated histones — chromatin targeting |
| Helicase domain (SNF2-like) | ATP-dependent chromatin remodeling |
| DNA-binding domain | Binds DNA during remodeling |
| BRK domain | Protein-protein interaction |

Mutations in CHD genes are associated with developmental phenotypes, including intellectual disability syndromes in mammals and growth abnormalities in birds, across vertebrates. In birds, the gene's primary diagnostic value is sex determination, but its functional conservation across birds also makes it a useful phylogenetic marker for reconstructing deep avian relationships.

## Expression and Regulation

| Property | Detail |
|----------|--------|
| Expression pattern | Ubiquitous; highest in actively dividing tissues |
| Regulation | Cell-cycle dependent; chromatin state influences expression |
| Alternative splicing | Multiple isoforms reported in avian transcriptomes |
| Copy number | Single CHD-Z copy on Z; CHD-W copy on W (in most species) |

Expression analysis of CHD is rarely used diagnostically in routine practice, but understanding the gene's regulation helps interpret edge cases — for example, why the W copy may be transcriptionally silenced in some tissues, and why primer design must target genomic DNA (introns) rather than mRNA for sexing assays.

## Assay Design Details for the CHD Test

| Design Parameter | Recommended Value |
|------------------|-------------------|
| Primer location | Exon-flanking (amplify across intron) |
| Intron target | CHD intron 10 (variable length) or equivalent |
| Amplicon size (Z) | 600–700 bp (species-dependent) |
| Amplicon size (W) | 350–500 bp (species-dependent) |
| Annealing temperature | 50–58 °C (gradient-optimized per species) |
| Gel type | 2–3% agarose or capillary electrophoresis |

For multiplexing sexing with other assays in a single reaction, the CHD amplicons' size separation from other targets must be verified experimentally — overlapping size ranges cause misreading of results.

## Species Coverage and Validation Data

The CHD-based sexing assay has been validated across major avian orders. Representative validation data from published studies:

| Species Group | Species Tested | Concordance | Notes |
|---------------|:---:|:---:|--------|
| Columbiformes | Pigeons, doves | 100% | Standard panel works well |
| Psittaciformes | Parrots, cockatoos | 99–100% | Band sizes vary; per-species calibration |
| Falconiformes | Falcons, hawks, eagles | 100% | Clean two-band patterns |
| Passeriformes | Songbirds, finches | 97–100% | Some species require modified primers |
| Galliformes | Chickens, pheasants | 100% | Large size difference between bands |
| Strigiformes | Owls | 98–100% | Occasional band-size overlap |
| Anseriformes | Ducks, geese | 100% | Well-characterized |
| Ratites | Ostrich, emu | **Not reliable** | CHD-W absent/undetectable — use HINTW |

### Known Problem Species

| Species | Issue | Alternative |
|---------|-------|-------------|
| Ostrich, emu, rhea | No CHD-W amplification | HINTW-based assay |
| Some penguin species | Band-size overlap | Capillary electrophoresis or qPCR melt |
| Woodpeckers (some) | Multiple CHD-like copies | Careful primer design; sequence verification |
| New World vultures | Unusual band patterns reported | Species-specific validation required before use |

This coverage table is precisely why laboratories must maintain a **validated species menu** — offering CHD sexing for "all birds" without per-species validation of primers and band sizes is scientifically indefensible and risks confident but wrong results.

## Quality Control in CHD Testing: Detailed Protocol

### Per-Batch Control Requirements

| Control | Preparation | Acceptance |
|---------|-------------|------------|
| Male reference | Known ZZ DNA (e.g., rooster) | Single band at expected size |
| Female reference | Known ZW DNA (e.g., hen) | Two bands at expected sizes |
| No-template control | Water in PCR mix | No amplification |
| Internal control | β-actin or GAPDH primers | Amplification in all samples |
| Size ladder | 100 bp ladder | Correct band sizing |

### Troubleshooting Common CHD Assay Failures

| Symptom | Cause | Fix |
|---------|-------|-----|
| No bands (all samples) | Extraction failure or reagent issue | Check DNA, fresh reagents |
| No bands (one species) | Primer mismatch | Species-specific primer redesign |
| Single band in known female | Degraded DNA or band overlap | Re-extract; capillary electrophoresis |
| Extra bands | Non-specific amplification | Increase annealing temperature |
| Smear | Too much template | Dilute 1:5–1:10 |
| Contamination (NTC positive) | Amplicon carryover | Decontaminate; separate areas |

## Interpretation Edge Cases and Their Resolution

| Edge Case | Band Pattern | Correct Interpretation |
|-----------|--------------|------------------------|
| Single band, unexpected size | 1 band ≠ reference Z size | Not male by default — verify against species controls |
| Two bands, one faint | 2 bands, unequal intensity | Female (ZW); faint band may reflect degradation |
| Three bands | 3 bands | Possible extra CHD copy or contamination — investigate |
| No bands, IC failed | 0 bands, no IC | Invalid — re-extract |
| No bands, IC OK | 0 bands, IC amplified | Sample lacks CHD (rare) or primer mismatch — species check |
| Male pattern on known female | 1 band | Assay failure or degradation — repeat with fresh sample |

### The Two-Independent-Assay Rule

For high-value birds (racing champions, elite breeding stock), confirm sex with **two independent assays**:

1. End-point PCR + gel (standard CHD)
2. qPCR melt-curve or a second primer pair targeting a different region

Agreement between two independent assays performed on the same DNA extract virtually eliminates analytical error in routine sex determination. Any disagreement triggers full investigation — never guess the answer.

## Database Update and Maintenance Policy

| Activity | Frequency | Purpose |
|----------|-----------|---------|
| Band-size re-verification | Annually | Detect primer/species drift |
| New species validation | On demand | Expand validated menu |
| Reference sequence update | As genome assemblies improve | Align primers to current references |
| Literature monitoring | Quarterly | Incorporate new validation studies |
| Error review | Per incident | Document and correct interpretation issues |

Maintaining the CHD database is an ongoing scientific commitment — the reference values that laboratories rely upon must continuously reflect the current body of published evidence.

## References

1. Griffiths, R.; Double, M. C.; Orr, K.; Dawson, R. J. G. A DNA test to sex most birds. *Molecular Ecology* 1998;7(8):1071-1075. DOI: 10.1046/j.1365-294x.1998.00389.x. PubMed ID: 9711866
2. Fridolfsson, A. K.; Ellegren, H. A simple and universal method for molecular sexing of non-ratite birds. *Journal of Avian Biology* 1999;30(1):116-121. DOI: 10.2307/3677252
3. Morinha, F.; Cabral, J. A.; Bastos, E. Molecular sexing of birds: A comparative review of PCR-based methods. *Theriogenology* 2012;78(4):703-714. DOI: 10.1016/j.theriogenology.2012.04.015

---

Return to [Research Database Overview](index.md) or read [STR Marker Database](str-markers.md).
