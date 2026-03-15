# Comprehensive Research Documentation
Well,these are my research logs IM lazy I'll reflourish the proper README when it's published...:_) peace.


ALso,the final results and plots such as manhatten plot , PRS distribution acros individuals , QQ plots and Ancestoy clusters aren in the
plots directory along with all the other plots,
 Research Logs – 

 Aim : 
 investigate how Genetic factors contribute to psychiatric diseases, with a focus
 on specific decease schizophrenia, by building a reproducible SNP‑layer pipeline that preserves
 biologically relevant signals that'll further in  and sets the foundation for multimodal integration.
---

Data Sources:  
- 1000 Genomes Phase 3 (hg19 'reference genome build'): Chosen for open sourced accessibility and global diversity.  
- PGC Schizophrenia GWAS summary statistics: using Primary datasets (autosome + chrX) to maximize cohort diversity.  
    - Primary datasets: larger, more inclusive, reflect global variation.  
    - Core datasets: curated, harmonized, narrower scope.  
    - Rationale: inclusivity and diversity prioritized to capture broad genetic variation.

 Methods & QC

1. Genotype Matrix Construction
   - Variants harmonized, strand ambiguity resolved, sex inferred via X heterozygosity.  
   - Multi‑allelic sites excluded for initial model simplicity.  
   - Chromosome X modeled in diploid space for consistency across samples.

2. Variant QC Metrics  
   - Allele frequency (AF), minor allele frequency (MAF).  
   - Dosage mean and variance, derived from Hardy–Weinberg equilibrium assumptions.  
   - Exclusion of ambiguous/discordant alleles.

3. Statistical Validation ,  
   - Manhattan plots (Current state-of-the-art for ancestory data quality.) : –log10(p‑value) vs |β| effect size.  
   - Distribution checks: effect size vs statistical significance.  
   - Dosage variance distributions compared across high‑ vs low‑variance SNPs.

---

Biological Significance
- Polygenicity of Schizophrenia: QC safeguards weak but biologically relevant signals across thousands of SNPs.  

- Pathway Anchoring: Recovery of GWAS hits tied to neurotransmitter pathways (dopamine, glutamate, synaptic signaling) 
                   validates biological relevance.  

- Global Diversity: Using primary datasets captures ancestry variation, critical for psychiatric genetics where 
                    stratification can bias results.  

-Foundation for Novelty: This SNP layer is the scaffold for multimodal integration (genetics + neuroimaging + 
transcriptomics + ML), which is where deeper biological insights will emerge.




---Citations & Next Steps ,
- Current reliance on open‑source data (1000G, PGC primary) limits resolution compared to UK Biobank or high quality individual level
 other strong institutional backed datasets.  
- No multimodal features yet (imaging, transcriptomics).  

- Future work:  
  - Integrate multimodal data with ML. 
  - Neuroimaging (sMRI/fMRI) 
  - Transcriptomics
  - Extend QC to sex‑aware modeling.  
  - Population‑specific fine‑tuning once higher‑quality datasets are accessible.

---

s Accountability Notes
- Hardy–Weinberg assumptions explicitly acknowledged (no selection, mutation, migration; large random‑mating populations).  
- Variance and mean dosage metrics computed and visualized.  
- Ambiguous alleles excluded, allele harmonization added, strand ambiguity handled.  
- Chromosome X modeled consistently, with future plans for sex‑aware refinement.
