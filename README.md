# MiCM ChIP seq

This worskhop will guide you through the basics of ChIP-seq analysis with hands-on exercises. Worskhop participants will learn how to process ChIP-seq data: perform read alignment, peak calling, visualization through the genome browser, motif finding and gene set enrichment analysis. 

## Requirements
We will be using the unix terminal to run our analyses, so be sure you have access to one. 

* Mac OS and any linux distribution will have a terminal already
    * Mac OS: search for terminal in your spotlight search
* Windows users: 
    * Option 1: Download a [unix subsystem (WSL)](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#1-overview) **recommended
    * Option 2: Download [MobaXterm](https://mobaxterm.mobatek.net/)

## Sofware
* [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)
* [Samtools](http://www.htslib.org/)
* [MACS2](https://pypi.org/project/MACS2/)
* [Bedtools](https://bedtools.readthedocs.io/en/latest/)
* [Deeptools](https://deeptools.readthedocs.io/en/develop/)
* Python3 (>=3.6) is required for installing MACS2 and Deeptools
* R (>=4.0.0) and Rstudio

> To install the software, look at the instructions for your operating system. Open your terminal and copy and paste the following commands inside the text boxes

### Linux distribution and Windows with WSL
Most of the software we need is availble through the package manager.

```{}
sudo apt install bowtie2
sudo apt install samtools
sudo apt install bedtools
pip3 install MACS2 # Note: For users of python 3.10 please see below
pip3 install deeptools
```

If you are using python (3.10), please install [MACS3](https://pypi.org/project/MACS3/)
```{}
pip3 install MACS3
```

### Mac OS
First install [Homebrew](https://brew.sh/) or any other package manager.
```{}
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
Then you can use brew to install the packages.
```{}
brew install fastqc
brew install bowtie2
brew install samtools
pip install multiqc
pip install cutadapt
```
### R
In R, type the following command.
```{r}
install.packages()
```

## Check the installation
To check that the program works, you can check if the help message gets printed:
```{}
bowtie2 --help
samtools --help
bedtools --help
macs2 --help # or macs3 --help
deeptools --help
```

If you run into any issues, see [install_issues](/install_issues.md)
