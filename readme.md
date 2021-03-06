# scsHi-C analysis

This repository contains notebooks for the analysis of scsHi-C data.

## Preprocessing

Preprocessing of scsHi-C experiments was done as follows: First, the [scshic_pipeline](https://github.com/gerlichlab/scshic_pipeline) was applied to raw sequencing data. The resulting cooler files were then balanced as follows:

- All-contact coolers were zoomified and balanced conventionally (see the following [script](https://github.com/Mittmich/scsHiCanalysis/blob/master/preprocessing/Zoomify_and_balance_all_wOldG2_exp4812_ignore_diag_1_fc_1_2_3_4.sh) for an example for G2 WT data)
- Cis-sister and trans-sister contacts were pooled (see the following [script](https://github.com/Mittmich/scsHiCanalysis/blob/master/preprocessing/Merge_coolers_cis_trans_forBalance_w_oldG2_fc_1_2_3_4.sh) for an example for G2 WT data)
- Then, the pooled cis-and-trans sister contacts were zoomified and balanced (see the following [script](https://github.com/Mittmich/scsHiCanalysis/blob/master/preprocessing/Zoomify_and_balance_cis_and_trans_wOldG2_exp4812_ignore_diag_1_fc_1_2_3_4.sh) for an example for G2 WT data)
- Then, cis-sister and trans-sister coolers were seperately zoomified (see the following [script](https://github.com/Mittmich/scsHiCanalysis/blob/master/preprocessing/Zoomify_cis_trans_wOldG2_exp4812_fc_1_2_3_4.sh) for an example for G2 WT data) and the obtained weights from the cis-and-trans sister coolers transferred to the cis-sister and trans-sister file respectively (see the following [script](https://github.com/Mittmich/scsHiCanalysis/blob/master/preprocessing/Transfer_weights_from_cis_and_trans_wOldG2_fc_1_2_3_4.py) for an example for G2 WT data).


## Fig. 1

### (d)

The analysis of relative mutation rates between a sample grown for 5 days in 4sT and a control sample before and after OsO4-mediated conversion can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Calculate_relative_mutation_rate.ipynb).


## Fig. 2

### (a)

The visualization of the example region on chr.1 for the pooled G2 WT samples can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb).

### (b)

The visualization of the example region on chr.1 for the pooled Prometaphase samples can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Prometaphase_pooled_examples.ipynb).

### (c) and (d)

The calculation of genomie scaling curves of the pooled G2 WT sample and the pooled prometaphase sample can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Scaling_Plots_G2_WT_Prometaphase.ipynb)

### (e)

The visualization of the example region on chr.8 for the pooled G2 WT samples can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb).

### (f), (g) and (h)

The quantification visualization of LOLA-enrichment scores, the quantification of H3K27me3 intensity at highly paired and highly unpaired domains and the stack-up of line-profiles at highly paired and highly-unpaired regions can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Visualize_enrichment_results_2.ipynb).

## Fig. 3

### (a)

The visualization of the example region on chr.2 for the pooled G2 WT samples as well as the calculation of cis-sister and trans-sister contact density can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb).

### (b), (e) and (f)

The pileup of cis-sister and trans-sister contacts at TAD-centers as well as the stak-up of line profiles along TADs and the quantification of enrichment of trans-sister contacts at TAD-boundaries can be found in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_analysis_WT_2.ipynb).

## Fig. 4

### (a)

The visualization of the example region on chr. 1 for the G2 WT sample can be found in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb). The visualization of the example region on chr. 1 for the Nipbl-degraded sample can be found in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Examples_Nipbl-AID.ipynb). The visualiztion of the example region on chr. 1 for the Sororin-degrade sample can be found in the folloiwing [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Examples_Sororin-AID.ipynb).

### (b)

The calculation of genomic scaling plots for the WT sample, the Sorroin-degraded sample and the Nipbl-degraded sample can be found in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Scaling_Sororin_Nipbl_Wt.ipynb).

### (c)

The pileup of TAD-centers for Nipbl-degraded sample can be found in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_boundary_analysis_Nipbl_v2.ipynb). A similar analysis for the Sororin sample can be found [here](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_boundary_analysis_Sororin_v2.ipynb).

### (d)

The obs/expected stack-up calculations can be found in the following notebooks: [WT](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_analysis_WT_2.ipynb), [Nipbl](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_boundary_analysis_Nipbl_v2.ipynb), [Sororin](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_boundary_analysis_Sororin_v2.ipynb).

### (e)

The quantification of contact amount at TAD-boundaries for G2 WT samples, G2 Nipbl-degraded samples and G2 Sororin-degraded samples as done in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Quantify_ICCF_Sororin_WT_Nipbl.ipynb).

## Extended Data Fig. 1

### (d)

The quantification of percentage of cells that is alive upon treatment with different concentrations of 4sT and etoposide for 24h was done in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Plot_apoptotic_index_timelapse_specific_timepoints.ipynb)

### (f)

The quantifiction of normalized (to control) p-gamma-H2A.X signal upon treatment with 4sT and etoposide for 24h was done in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Plot_phospho_gamma_H2A_exp4750_and_exp4611.ipynb)


### (i)

The quantification of doubly labelled reads in scsHi-C samples released into S-Phase for different amounts of time can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Count_percentage_doubly_labeled_S-Phase-Release.ipynb).

### (j)

The quantification of trans-sister contacts in scsHi-C samples generated n G2, prometaphase in the following G1 phase can be found in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Count_cis_trans_G2_Prometaphase_G1.ipynb).

## Extended Data Fig. 2

## (a)

Mass spec based quantification of 4sT in DNA from cells grown for 5 days in 4sT was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Plot_exp4572_exp4557.ipynb)

## (b)

Quantification of sequencing based incorporation of 4sT was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/Calculate_relative_mutation_rate.ipynb)


## Extended Data Fig. 3

### (a)

Histograms of signature mutations per read were calculated in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Histogram_label_amount.ipynb).

### (b)

The false-positive rate of doubly labelled read detection was calculated in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/FPR_doubly_labelled_reads.ipynb).

### (d)

The percentage of doubly labelled reads at different numbers of signature mutations was calculated in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/FPR_determination_trans_assignment.ipynb).

### (e)

The amount of wrongly assigned trans-sister contacts was calculated in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/FPR_determination_trans_assignment.ipynb).

## Extended Data Figure 4

### (a)

Example regions for two of the G2 WT replicates was visualized in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_ind_examples.ipynb).

### (b)

HiCrep was run for the different G2 WT replicates in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/HiCRep_WT_v1.ipynb).

### (c)

Example regions for the two Prometaphase replicates were visualized in this [notebook] (https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Prometaphase_ind_examples.ipynb).

### (d)

HiCrep was run for the different prometaphase replicates in this [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/HiCRep_Prom_v1.ipynb).

## Extneded Data Figure 5

### (a)

Example of G2 WT data on chromosome 3 was visualized in  the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb).

### (b)

Correlation of scsHi-C data with FISH loci-splitting frequency was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Correlation_with_FISH.ipynb)

### (c)

Correlation of scsHi-C data with dCas9 loci splitting frequency was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Correlation_with_newData_exp4812.ipynb)

### (d)

Histogram of average trans-sister contact per TAd was calculated in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Visualize_enrichment_results_2.ipynb).

### (e)

Scaling plots of cis-sister and trans-sister contacts in highly paired and highly unpaired domains was calculated in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Scaling_Plots_G2_WT_pairingDoms.ipynb)

### (f)

Average H3K27me3 signal at high-pairing domains was calculated in the folloiwng [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Visualize_enrichment_results_2.ipynb).


## Extended Data Figure 6

### (a), (b), (c)

Example regions in this figure were plotted in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb).

### (d)

Hi-C stack-ups at CTCF sites were calculated in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/CTCF_pileup_WT.ipynb).

### (e)

Quantification of Hi-C signal at CTCF sites was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/CTCF_analysis_WT.ipynb).

## Extended Data Figure 7

### (c)

Scaling plots for WT G2 and Nipbl-degraded samples constructed from all reads can be found in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Scaling_G2_Nipbl_all_reads.ipynb).

### (e)

Example regions were plotted in the following notebook: [WT](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/G2_pooled_examples_v2.ipynb), [Sororin-degraded](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Examples_Sororin-AID.ipynb), [NIPBL-degraded](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Examples_Nipbl-AID.ipynb).

### (f)

HiC-rep analysis of all NIPBL-degraded samples was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/HiCRep_Nipbl_v1.ipynb).
HiC-rep analysis of Sororin-degraded samples was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/HiCRep_Sororin_v1.ipynb).

## Extended Data Figure 8

## (a)

ICCF stack up analysis of NIPBL-degraded cells was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_center_analysis_Nipbl.ipynb).

## (b)

Obs/exp stack up at TADs of WT and NIPBL-degraded cells was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/TAD_center_analysis_Nipbl.ipynb).

## (c)

ICCF stack up analysis at highly paired and highly unpaired domains was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Pairing_domain_analysis_NIPBL_WT.ipynb).

## (d)

Pairing score stack up analysis at highly paired and highly unpaired domains was done in the following [notebook](https://github.com/Mittmich/scsHiCanalysis/blob/master/notebooks/Pairing_domain_analysis_NIPBL_WT.ipynb).

