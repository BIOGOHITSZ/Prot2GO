# Readme

**This repository contains implementation of Prot2GO in jupyter notebook**

You should download datasets mentioned in our paper, and use the scripts to train the model.

Model details:

sequence data: mapping to matrix using ProVec ,i.e. each trigram is represented by a 100d dense vector, so each protein sequnce is mapped to a 1500*100 matrix.
    feature extraction of sequence data: recurrent CNNS followed by attention.

PPI data: 
   utilize network representation learning to get embeddings of each protein node, concat this vector with sequence feature to predict labels.

**Important:**
i write the codes in different machines, so the datapathes in the scripts may be incorrect,please update the path with respect to the true path.
what is more, hyper-parameters in our model is not the best, which means you can change them to get better results.

# Abstract
Protein is the main material basis of living organisms and plays crucial role in life activities. Understanding the function of protein is of great significance for new drug discovery, disease treatment and vaccine development. In recent years, with the widespread application of deep learning in bioinformatics, researchers have proposed many deep learning models to predict protein functions. However, the existing deep learning methods usually only consider protein sequences, and thus cannot effectively integrate multi-source data to annotate protein functions. In this article, we propose the Prot2GO model, which can integrate protein sequence and PPI network data to predict protein functions. We utilize an improved biased random walk algorithm to extract the features of PPI network. For sequence data, we use a convolutional neural network to obtain the local features of the sequence and a recurrent neural network to capture the long-range associations between amino acid residues in protein sequence. Moreover, Prot2GO adopts the attention mechanism to identify protein motifs and structural domains. Experiments show that Prot2GO model achieves the state-of-the-art performance on multiple metrics.

