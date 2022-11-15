# MiCM_ChIP_seq


## Requirements
We will be using the unix terminal to run our analyses. so be sure you have access to one. 

* Mac OS and any linux distribution will have a terminal already
    * Mac OS: search for terminal in your spotlight search
* Windows users: 
    * Option 1: Download a [unix subsystem (WSL)](https://ubuntu.com/tutorials/install-ubuntu-on-wsl2-on-windows-10#1-overview) **recommended
    * Option 2: Download [MobaXterm](https://mobaxterm.mobatek.net/)

## Sofware
* Python3 is required 


During the workshop we will be using some known bioinformatics software to process our dataset:
* [FastQC](https://www.bioinformatics.babraham.ac.uk/projects/fastqc/)
* [MultiQC](https://multiqc.info/)
* [CutAdapt](https://cutadapt.readthedocs.io/en/stable/installation.html) - can be installed with pip or with conda
* [Bowtie2](http://bowtie-bio.sourceforge.net/bowtie2/index.shtml)
* [Samtools](http://www.htslib.org/)
* [IGV](https://software.broadinstitute.org/software/igv/download) - Optional, if you want to visualize. Please install by following the website instructions.

> To install the software please open your terminal and copy and paste the following commands inside the text boxes.

### Linux distribution and Windows with WSL
Most of the software we need is availble through the package manager.
```{}
sudo apt install fastqc
sudo apt install bowtie2
sudo apt install samtools
pip install multiqc
pip install cutadapt
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

### Check the installation
To check that the program works, you can check if the help message gets printed:
```{}
fastqc --help
bowtie2 --help
samtools --help
multiqc --help
cutadapt --help
```

> Some problems may arise while installing software. Be patient and read the error message, it could be due to some dependecies missing. Googling the error message is a good first attempt to solve it.
