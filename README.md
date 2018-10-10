Unified variant pipeline (UVP) BioCompute Object
===============================================

GitHub repository for Unified variant pipeline (UVP):
https://github.com/CPTR-ReSeqTB/UVP

GitHub repository for BioCompute Objects:
https://github.com/biocompute-objects/

----------------------------------------------------
The UVP BCO was made to standardize how we communicate the process for imputing drug resistance profiles using sequence-based technologies. 
The UVP incorporates a suite of the most current bioinformatics analysis tools, written in python scripting language.
In broad outline, there are four major steps implemented in the pipeline:
1. Input data validation & QC
2. Sequence reads mapping & refinement
3. Variant calling
4. Functional annotation & lineage analysis

## Software dependencies and Example files:

All of the files referenced in the [UVP BCO](/UVP_BCO.json) are available at [Unified Variant Pipeline BioCompute Object](http://bco.reseqtb.org/UVP-BCO/) site. 

The following are the tools used in UVP:

[BEDtools Version 2.17.0](https://github.com/arq5x/bedtools/releases/tag/v2.17.0),
[Bcftools Version 1.2](https://github.com/samtools/bcftools/releases/download/1.2/bcftools-1.2.tar.bz2),
[BWA Version 0.7.12](https://sourceforge.net/projects/bio-bwa/files/bwa-0.7.12.tar.bz2/download),
[FastQC Version 0.11.5](https://www.bioinformatics.babraham.ac.uk/projects/fastq_screen/fastq_screen_v0.13.0.tar.gz),
[Fastqvalidator Version 1.0.5](https://www.bioinformatics.babraham.ac.uk/projects/fastq_screen/fastq_screen_v0.13.0.tar.gz),
[GATK Version 3.4.0](https://github.com/broadgsa/gatk-protected/releases/tag/3.4),
[Kraken Version 0.10.5](https://ccb.jhu.edu/software/kraken/dl/kraken-0.10.5-beta.tgz),
[Picard Version 1.134](https://github.com/broadinstitute/picard/releases/tag/1.134),
[Prinseq-lite.pl Version 0.20.4](https://sourceforge.net/projects/prinseq/files/standalone/prinseq-lite-0.20.4.tar.gz/download),
[Pigz Version 2.3.3](http://springdale.math.ias.edu/data/puias/unsupported/7/SRPMS/pigz-2.3.3-1.sdl7.src.rpm),
[Qualimap Version 2.1.1](https://bitbucket.org/kokonech/qualimap/downloads/qualimap_v2.1.1.zip),
[Samtools Version 1.2](https://github.com/samtools/samtools/archive/1.2.zip),
[SnpEff Version 4.1](https://sourceforge.net/projects/snpeff/files/snpEff_v4_1l_core.zip/download),
[Vcftools Version 0.1.126](https://sourceforge.net/projects/vcftools/files/vcftools_0.1.12.tar.gz/download)

## Installation

The UVP requires at least 100GB RAM and up to 100GB storage space to run locally. Insatlling the UVP on your local machine is straight forward. Clone the entire repository, and download the specific version of each of the third party tool listed above into the 'Local Directory Path'/uvp/bin folder . You will need to edit the config.yml file in the 'Local Directory Path'/uvp/bin folder to point to the correct directory and file paths of all the scripts and tools listed there in.

You will run the UVP using command line prompts, by invoking the UVP module in the 'Local Directory Path'/uvp/scripts directory:

'Local Directory Path'/uvp/scripts/UVP -q 'input fastq' -r 'path to H37Rv reference genome fasta file' -n 'sample name' -q2 'paired fastq file' -a -v 
