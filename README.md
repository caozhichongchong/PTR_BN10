# BN10 data path on c3ddb
* genomes: /scratch/users/anniz44/genomes/donor_species/selected_species/round1/allfasta/*/fasta/
* metagenomes: /scratch/users/anniz44/Metagenomes/BN10_MG/multiple/
* [trial data](https://drive.google.com/drive/folders/1ocNlSmVHdIVTr8RG-jGTqX5dc4xbZp1_?usp=sharing)
* [species information](https://drive.google.com/file/d/1W0ANLpcewOUrQ5RUaFbOezati-xhnmkW/view?usp=sharing)
# How to work with c3ddb
* To email their admin (c3ddb-admin@techsquare.com ) for more disk space and file quota
for example: 2TB of disk space and 10,000,000 number of files
* To login c3ddb: `ssh -i $your_public_key -l your_c3ddb_name c3ddb-globus.mit.edu`\
usually your_c3ddb_name = your mit email address\
sometimes login requires your password\
`c3ddb-globus.mit.edu` node is used for small tasks, such as python, scp, and rsync (file transfer)\
`c3ddb01.mit.edu` node is used for submitting jobs
* To follow the [instructions to set up c3ddb](https://github.com/caozhichongchong/PTR_BN10/blob/main/c3ddb_introduction.docx)
* To find the genomes and metagenomes on c3ddb
    * genomes: /scratch/users/anniz44/genomes/donor_species/selected_species/round1/allfasta/*/fasta/
    * metagenomes: /scratch/users/anniz44/Metagenomes/BN10_MG/multiple/
# Aligning metagenomes to reference genome
* [Mapper](https://github.com/mathjeff/Mapper)
* [Latest Mapper](https://drive.google.com/file/d/1yz9GkTO7aGjcYPov3XmHOkuB_-UxCQKl/view?usp=sharing)
* To allocate threads and memory: `java -Xms10g -Xmx10g mapper-1.1.0-beta01.jar --num-threads 40`
# PTR analysis
* Interpret vcf: contains a description of allele counts by reference genomic position
* How to tell whether a species exists in that sample?
* How to exclude metagenomic sequences (reads) that don't belong to this species but align to the reference genome?\
Why do they align?  
* How to find the origin (“peak”) and the terminus (“trough”) of replication?\
Considering that the reference genome is not circular, containing multiple sequences\
Can we see the peak -> trough -> peak pattern in read depth?\
What model can we use to evaluate the quality of this pattern? 
* Compute peak to trough ratio
Can we use data of all genomic regions, instead of just the peak and trough?
* What does PTR tell us?\
Growth rate? Proportion of cells in growth?
# PTR in BN10 data