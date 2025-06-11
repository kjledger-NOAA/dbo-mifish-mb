# dbo-mifish-mb
12S MiFish metabarcoding analysis of eDNA samples from Arctic DBO stations

## 1. the data 
MiFish metabarcoding reads from eDNA samples collected at DBO stations/moorings in the NBS and Chukchi Sea 
* DY2012 - Sept 2020 (PMEL)
* NO20 - Oct 2020 (PMEL)
* SKQ2021 - Nov 2021 (PMEL)
* SKQ2023 - Sept 2023 (ABL + PMEL)
* SKQ2024 - Aug 2024 (ABL)

## 2. preprocessing 
all demultiplexed fastq files combined into a single folder and processed using Dadasnake (config.DBO.mifish.yaml) 

## 3. taxonomic assignment 
ran blastn.sh on SEDNA and processed taxonomic assignments using "1_taxonoic_assignment_blastn.Rmd"

## 4. post asv curation 
ran "3_lulu.Rmd" to removes ASVs that are likely sequencing errors of more abundant ASVs 

## 5. join taxonomic assignment to asv table 
run "3_taxon_summary.Rmd"