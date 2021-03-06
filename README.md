# BetaVAEImputation

As missing values are frequently present in genomic data, practical methods to handle missing data are necessary for downstream analyses that require complete datasets. In this work, we describe the use of a deep learning framework based on the variational autoencoder (VAE) to impute missing values in transcriptome and methylome data analysis.

The scripts contained in this repository can be used to carry out the analysis in “Genomic data imputation with variational autoencoders”. 

#######Imputation

#VAE imputation  
python train_beta_VAE.py --config example_config_VAE.json  
python test_beta_VAE.py --config example_config_VAE.json  
#KNN imputation  
python test_KNN.py --config example_config_KNN.json  
#SVD imputation  
python test_SVD.py --config example_config_SVD.json

#######Compare clinical correlations

#Spearman correlation to histologic grade  
python cindex_spearman_cor.py

#Cox regression coefficient to survival  
Rscript find_cox_coeff.R  
python cindex_cox_coeff.py

