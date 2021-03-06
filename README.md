This repository contains following scripts:
 - processing whole-exome sequencing data
 - construction of validation set based on multiple data
 - choise of reference set and running CNV callers
 - analysis of CNV calling tools perfomance
 
 



### Datasets:
**Exome data**: The 1000 Genomes Project Phase 3 ([samples](https://github.com/bioinformatics-IBCH/Comparasion-study-of-germline-CNV-tools/blob/master/samples.csv))
```bash
ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/phase3/data/
ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/technical/reference/exome_pull_down_targets/20130108.exome.targets.bed
```            


**Compared CNV calling tools:**
 - [CANOES](www.columbia.edu/~ys2411/canoes/)  (Backenroth *et al. Nucleic Acids Res*, 2014)
 - [CLAMMS](https://github.com/rgcgithub/clamms)  (Packer *et al. Bioinformatics*, 2015) 
 - [cn.MOPS](http://bioconductor.org/packages/release/bioc/html/cn.mops.html)  (Klambauer* et al, Nucleic Acids Res*, 2012)
 - [CNVkit](https://cnvkit.readthedocs.io/en/stable/)  (Talevich *et al. PLOS Computational Biology*, 2016)
 - [CODEX](https://github.com/yuchaojiang/CODEX) (Jiang *et al. Nucleic Acids Res*, 2015)
 - [CoNIFER](http://conifer.sourceforge.net/index.html) (Krumm *et al. Genome Research*, 2012)
 - [CONTRA](http://contra-cnv.sourceforge.net/) (Li *et al. Bioinformatics*, 2012)
 - [DeAnnCNV](https://mcg.ustc.edu.cn/bsc/cnv/) (Zhang *et al. Nucleic Acids Res*, 2015)
 - [EXCAVATOR2](https://sourceforge.net/projects/excavator2tool/) (D'Aurizio *et al. Nucleic Acids Res*, 2016)
 - [exomeCopy](https://bioconductor.org/packages/release/bioc/html/exomeCopy.html) (Samarakoon *et al  BMC Genomics*, 2014)
 - [ExomeDepth](https://cran.r-project.org/web/packages/ExomeDepth/index.html) (Plagnol *et al. Bioinformatics*, 2012)
 - [ExonDel](https://github.com/slzhao/ExonDel) (Guo *et al. BMC Bioinformatics*, 2014)
 - [FishingCNNV](https://sourceforge.net/projects/fishingcnv/) (Shi *et al. Bioinformatics*, 2013)
 - [HMZDelFinder](https://github.com/BCM-Lupskilab/HMZDelFinder) (Gambin *et al. Bioinformatics*, 2017)
 - [PatternCNV](https://github.com/svsgvarma/patternCNV) (Wang *et al. Bioinformatics*, 2014)
 - [XHMM](https://statgen.bitbucket.io/xhmm/index.html) (Fromer *et al. Am J Hum Genet*, 2012)
 
 **CNV sets used to construct internal standard  for NA12878 at exon level**
 
- *mccarroll2006* (McCarroll *et al. Nature Genetics*, 2006) 
```bash
ftp://ftp.ebi.ac.uk/pub/databases/dgva/nstd20_McCarroll_et_al_2006/gvf/nstd20_McCarroll_et_al_2006.2015-11-02.GRCh37.Remapped.gvf
```
 - *conrad2006* (Conrad *et al. Nature Genetics*, 2006)
```bash
ftp://ftp.ebi.ac.uk/pub/databases/dgva/nstd17_Conrad_et_al_2006/gvf/nstd17_Conrad_et_al_2006.2015-11-02.GRCh37.Remapped.gvf
 ```
- *wang* (Wang *et al. Genome Research*, 2007)
```bash
ftp://ftp.ebi.ac.uk/pub/databases/dgva/nstd64_Wang_et_al_2007/gvf/nstd64_Wang_et_al_2007.2017-10-03.GRCh37.Remapped.gvf 
```
- *pinto* (Pinto *et al. Human Molecular Genetics*, 2007)
```bash
ftp://ftp.ebi.ac.uk/pub/databases/dgva/estd55_Pinto_et_al_2007/gvf/estd55_Pinto_et_al_2007.2014-04-02.GRCh37.Remapped.gvf
```
- *cooper* (Cooper *et al. Nature Genetics*, 2008)
```bash
ftp://ftp.ebi.ac.uk/pub/databases/dgva/nstd14_Cooper_et_al_2008/gvf/nstd14_Cooper_et_al_2008.2015-11-02.GRCh37.Remapped.gvf
```
- *mccarroll2008* ( McCarroll *et al. Nature Genetics*, 2008)
```bash
https://static-content.springer.com/esm/art%3A10.1038%2Fng.238/MediaObjects/41588_2008_BFng238_MOESM24_ESM.xls
https://static-content.springer.com/esm/art%3A10.1038%2Fng.238/MediaObjects/41588_2008_BFng238_MOESM25_ESM.xls
``` 
- *hapmap* (International HapMap 3 Consortium, *et al. Nature*, 2010)
```bash
ftp://ftp.ncbi.nlm.nih.gov/hapmap/cnv_data/hm3_cnv_submission.txt
```
- *conrad2010* (Conrad *et al. Nature*, 2010)
```bash
https://static-content.springer.com/esm/art%3A10.1038%2Fnature08516/MediaObjects/41586_2010_BFnature08516_MOESM10_ESM.xls
```
- *pilot* (The 1000 Genomes Project Consortium Nature, 2010 Mills *et al. Nature*, 2011)
```bash
ftp://ftp-trace.ncbi.nih.gov/1000genomes/ftp/pilot_data/paper_data_sets/companion_papers/mapping_structural_variation/MasterValidation.Pilot2.all.leftmost.061510.txt 
```
- *phase1* (The 1000 Genomes Project Consortium *Nature*, 2012)
```bash
ftp://ftp.ebi.ac.uk/pub/databases/dgva/estd199_1000_Genomes_Consortium_Phase_1/gvf/estd199_1000_Genomes_Consortium_Phase_1.2013-06-27.GRCh37.Submitted.gvf
```
- *lumpy* (Layer *et al. Genome Biology*, 2014)
```bash
https://static-content.springer.com/esm/art%3A10.1186%2Fgb-2014-15-6-r84/MediaObjects/13059_2013_3363_MOESM4_ESM.zip
```
- *phase3*  (Sudmant *et al. Nature*, 2015)
```bash
ftp://ftp.1000genomes.ebi.ac.uk/vol1/ftp/phase3/integrated_sv_map/ALL.wgs.mergedSV.v8.20130502.svs.genotypes.vcf.gz
```
- *pacbio* (Pendleton *et al. Nature Methods*, 2015)
```bash
ftp://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/data/NA12878/NA12878_PacBio_MtSinai/NA12878.sorted.vcf.gz
```
- *metasv* (Parikh *et al. BMC Genomics*, 2016)
```bash
ftp://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/technical/svclassify_Manuscript/Supplementary_Information/metasv_trio_validation/NA12878_svs.vcf.gz
```
- *svclassify* (Parikh *et al. BMC Genomics*, 2016)
```bash
ftp://ftp-trace.ncbi.nlm.nih.gov/giab/ftp/technical/svclassify_Manuscript/Supplementary_Information/Personalis_1000_Genomes_deduplicated_deletions.bed 
```
 - Stringent CNV map of human genome (Zarrei *et al. Nat Rev Genet*, 2015)
 ```bash
 https://static-content.springer.com/esm/art%3A10.1038%2Fnrg3871/MediaObjects/41576_2015_BFnrg3871_MOESM27_ESM.xls
 ```
