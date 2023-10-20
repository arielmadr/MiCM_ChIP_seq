# MiCM ChIP seq

This page covers the instructions to download the software if you're using Docker. Please only follow up this instructions if you are familiar with Docker and have already installed Docker in your system. 

## Software

* [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)
* [Samtools](http://www.htslib.org/)
* [MACS2](https://pypi.org/project/MACS2/)
* [Bedtools](https://bedtools.readthedocs.io/en/latest/)
* [Deeptools](https://deeptools.readthedocs.io/en/develop/)
* R (>=4.0.0) and Rstudio 

> Open your terminal and copy and paste the following commands inside the text boxes

```{}
docker pull biocontainers/bowtie2:v2.4.1_cv1
docker pull biocontainers/samtools:v1.9-4-deb_cv1
docker pull biocontainers/bedtools:v2.27.1dfsg-4-deb_cv1
docker pull dceoy/macs2
docker pull njaved/deeptools
```

## Check the installation
To check that the program works, you can check if the help message gets printed:
```{}
docker run biocontainers/bowtie2:v2.4.1_cv1 bowtie2 --help
docker run biocontainers/samtools:v1.9-4-deb_cv1 samtools --help
docker run biocontainers/bedtools:v2.27.1dfsg-4-deb_cv1 bedtools --help
docker run dceoy/macs2  --help
docker run njaved/deeptools deeptools --help
```

## R libraries

It is still recommended to install R and Rstudio locally with its dependencies

```{r}
if (!require("BiocManager", quietly = TRUE))
    install.packages("BiocManager")

BiocManager::install("ChIPQC")
BiocManager::install("TxDb.Hsapiens.UCSC.hg38.knownGene")
BiocManager::install("rGREAT")
```
