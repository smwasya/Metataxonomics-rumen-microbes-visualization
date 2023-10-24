
# WE use the nf-core Ampliseq pipeline in this project


First we need to do preprocessing and generate ASV count matrix using the script

Run the script as follows; Note this was done on 16S for 18S and ITS refer to [nf-core/ampliseq website](https://nf-co.re/ampliseq/2.7.0)


`bash nf-core-ampliseq.sh version profile "path/to/the/data/" "extension" "/path/metadata/data.tsv" "Forward-primers" "Reverse-primers"  "outdir" "dada-reference-database"`

An example of the code executation

`bash analysis.sh 2.4.0 singularity "/data/GenomicData/MeridRumen/" "/*-B_{1,2}.fastq.gz" "/home/smwasya/tools/Metadata_Merid_Rumen_microbiome.tsv" "CCTACGGGNGGCWGCAG" "GACTACHVGGGTATCTAATCC"  "bacteria-output" "silva"`

For more elaboration about nf-core ampliseq pipeline please refer to [nf-core/ampliseq website](https://nf-co.re/ampliseq/2.7.0)

Use the output in outdir/dada2 to proceed to R create the phyloseq object as illustrated in the [script}(https://github.com/SamuelMwasya/Metataxonomics-rumen-microbes-visualization/blob/main/Scripts/16S-rRNA-Bacteria%20.rmd)
