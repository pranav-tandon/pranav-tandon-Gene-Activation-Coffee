```markdown
# Coffee × Nicotine: Engineering Alkaloid Biosynthesis in *Coffea arabica*

A bioinformatics-driven project to **discover, annotate, and engineer coffee homologs of the nicotine pathway genes found in tobacco**—with the long-term goal of producing valuable alkaloids in coffee plants.

---

## 1 · Why It Matters  
Nicotine biosynthesis is well understood in *Nicotiana tabacum*. Uncovering—and boosting—the equivalent genes in coffee could open new avenues in plant metabolic engineering, pharmaceutical precursors, and functional-ingredient agriculture.

---

## 2 · Project Roadmap (6 weeks total)

| Phase | Goal | Main Output |
|-------|------|-------------|
| 1 · Gene Identification (2 wk) | BLAST/HMMER search for coffee homologs of **PMT, MPO, QS, AO, QPT, SAMS, ODC, A622, BBL** | Homolog list + motifs |
| 2 · Pathway Annotation (1.5 wk) | Map homologs to nicotine pathway; InterPro + KEGG notes | Annotated pathway PDF |
| 3 · Vector Design (2 wk) | CRISPR-a / OE constructs in **pCAMBIA1300/1301** with double **CaMV 35S** promoters, **NOS** terminators | SnapGene files + primer list |
| 4 · -Omics Validation (1 wk) | Transcriptomic/­proteomic expression analysis; Cytoscape viz | Expression heatmaps |

---

## 3 · Current Progress
* Confirmed coffee homologs for **SAMS, PMT, MPO, QS**.  
* Dual-gene construct (35S::SAMS::NOS + 35S::PMT::NOS) validated _in-silico_.  
* Draft CRISPR-a gRNAs (Benchling) within 200 bp of TSS for each target.  
* Promoter/terminator catalogue: CaMV 35S, α-tubulin, PAL; NOS/OCS.

---

## 4 · Expected Deliverables
1. **Homolog Catalogue** (`data/homologs.tsv` + FASTA)  
2. **Pathway Report** (`reports/pathway.pdf`)  
3. **Cloning Package** (`constructs/*.dna`, primers, gRNA list)  
4. **-Omics Notebooks** (`notebooks/*.ipynb`)  
5. **Final Report** (`reports/final.pdf`)

---

## 5 · Repo Layout
```

├── data/          # FASTA, BLAST dbs, tables
├── src/           # analysis & vector-design scripts
├── notebooks/     # Jupyter/R notebooks for -omics
├── constructs/    # SnapGene / GenBank plasmids
└── reports/       # pathway & final PDFs

````

---

## 6 · Quick Start
```bash
# clone and set up
git clone https://github.com/<org>/coffee-nicotine.git
cd coffee-nicotine
conda env create -f env.yml   # installs BLAST, HMMER, Biopython, R libs
conda activate coffee-nico

# run full pipeline
python src/run_pipeline.py --coffee-genome coffee.2bit --tobacco-genes data/tobacco.fasta
````

---

## 7 · Contributing

Open an issue before large changes. PRs that add datasets, improve workflows (Snakemake/Nextflow), or refine vector/gRNA design are welcome.

---

## 8 · License

Distributed under the **MIT License**. See `LICENSE` for details.


```
```
