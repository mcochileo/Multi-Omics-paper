# Multi-Omics-paper
The code for all the analyses for the paper is in this folder.

1_RNAseq_alignment - code necessary to align RNAseq data for each replicate to the transcriptome using kallisto

	- code to be run in command line in txt format (multiAlignments_code_in_txt.txt)
	- code to be run in command line in bash format (multiAlignments.sh)
	- replicate names and corresponding SRR ids, in tab separated txt file (targets_	4.txt)



2_PCA_and_DEGs - code necessary for analyzing RNAseq data

	- Alignments_cluster
		- control_rep1 - alignment result for control1
		- control_rep2 - alignment result for control2
		- control_rep3 - alignment result for control3
		- STAG2kd_rep1 - alignment result for STAG2kd1
		- STAG2kd_rep2 - alignment result for STAG2kd2
		- STAG2kd_rep3 - alignment result for STAG2kd3
		- DEGs in excel format (DEGs.xlxs)
		- DEGs formated for GSEA (DEGs_GSEA.rnk and DEGs_GSEA.tsv)
		- DEGs formated for ORA (DEGs_ORA.txt)
		- background genes formated for ORA (background_genes_ORA.txt)
		- dowregulated DEGs (downReg.txt)
		- upregulated DEGs (upReg.txt)
		- reads for genes (readCounts_gene.RDATA)
	- R code for PCA and Differential Expression Analysis (DEG_analysis.R)
	- reference human genome used (gencode.v38_geneInfo)



3_ChIPseq - code for ChIPseq analysis and integration of RNAseq and ChIPseq data 

	- code to be run in command line to align, call peaks and filter out blacklisted 	regions using raw ChIPseq data (ChIPseq_command_line.txt)
	- ChIPseq_peaks_annotation
		- STAG2_filtered.txt - file produced using the code in 					ChIPseq_command_line.txt
 		with the final ChIPseq peaks
		- code to annotate STAG2 ChIPseq peaks (Annotation_ChIPseq.R) using the 		STAG2_filtered
		- STAG2_annotated_peaks.txt - file with annotated ChIPseq peaks
	- Compare_DEGS_ChIPseq - code for integrating DEGs and ChIPseq peaks
		- DEGs
		- upReg
		- downReg
		- STAG2_annotated_peaks
		- Overlap_between_DEGs_and_ChIPseq.R 
