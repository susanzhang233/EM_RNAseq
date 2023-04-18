# EM-RNAseq
Given some RNA-seq alignments in BAM format and a isoform annotation table, find the relevant equivalence classes, then estimate relative abundance of the isoforms by crafting an expectaion-maximization model.

The model involves first findng equivalent class counts for each gene transcript, with the kallisto[1](https://www.nature.com/articles/nbt.3519) method, then from there iteratively update the expectation-maximization model to approach maximum likelihood, ultimating generating a the transcript abundance table.

## Model structure
An illustration of the model from EM paper[2](https://arxiv.org/pdf/1104.3889.pdf) is also attached here:
![EM](https://user-images.githubusercontent.com/67823308/220251190-7a7dfe5b-0d03-4a54-9632-74bc57f7b04c.png)




## Repository Explanation
- [RNA-seq Expectation Maximization implementation.ipynb](https://github.com/susanzhang233/EM-RNAseq/blob/main/RNA-seq%20Expectation%20Maximization%20implementation.ipynb): main model structure and a brief demonstration
- [chr11_transcriptome.fasta](https://github.com/susanzhang233/EM-RNAseq/blob/main/chr11_transcriptome.fasta): RNAseq raw data chromosome 11 used in demonstration
- [supplementary materials(maybe).pdf](https://github.com/susanzhang233/EM-RNAseq/blob/main/supplementary%20materials(maybe).pdf): pdf version of the demonstration


## Sources
- https://arxiv.org/pdf/1104.3889.pdf
- https://www.nature.com/articles/nbt.3519
