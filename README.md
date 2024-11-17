# excon
In heliophysics research, predicting solar flares is crucial due to their potential to substantially impact both space-based systems and Earth’s infrastructure. Magnetic field data from solar active regions, recorded by solar imaging observatories, are transformed into multivariate time series to enable solar flare prediction using temporal window-based analysis. In the realm of multivariate time series-driven solar flare prediction, addressing severe class imbalance with effective strategies for multivariate time series representation learning is key to developing robust predictive models. Traditional methods often struggle with overfitting to the majority class in prediction tasks where major solar flares are infrequent. This work presents EXCON, a contrastive representation learning framework designed to enhance classification performance amidst such imbalances. EXCON operates through four stages: (1) obtaining core features from multivariate time series data; (2) selecting distinctive contrastive representations for each class to maximize inter-class separation; (3) training a temporal feature embedding module with a custom extreme reconstruction loss to minimize intra-class variation; and (4) applying a classifier to the learned embeddings for robust classification. The proposed method leverages contrastive learning principles to map similar instances closer in the feature space while distancing dissimilar ones, a strategy not extensively explored in solar flare prediction tasks. This approach not only addresses class imbalance but also offers a versatile solution applicable to both univariate and multivariate time series across binary and multiclass classification problems. Experimental results, including evaluations on the benchmark solar flare dataset and multiple time series archive datasets with binary and multiclass labels, demonstrate EXCON's efficacy in enhancing classification performance and reducing overfitting.

![EXCON_fig](https://github.com/user-attachments/assets/5079fa75-098a-4bb5-af40-1c4cab72acd0)

# Content Details
* <code> DATA\ </code> Desired datasets may be placed here for excon-p2.ipynb
* <code> DATA\catch22 </code> Directory for data points, including extracted catch22 feature vectors and the contrastive extremes.
* <code> DATA\Preprocessed-SWANSF-main </code> Directory for preprocessed SWAN-SF data points, in case of training all components from scratch, the folders to keep data files must be placed under here (names and paths can be specified while running the relevant notebook cells).

  
* <code> src/ </code> The details for each notebook file are as follows:
  - <code>excon-main.ipynb</code>: Experiments with the EXCON framework based on its classification performance on both the SWAN-SF dataset and multiple time series archive datasets
  - This module is a step-by-step guide to our extended edition experiments in a single notebook file.
    
# Execution Details 
* To view our modules, experiments, and results in a single file, each ipynb file is sufficient.
* Since SWAN-SF is a large dataset, we do not include the preprocessed dataset in DATA\Preprocessed-SWANSF-main, if you need to train the components and start the experiments from scratch, don't hesitate to contact us!
* Original SWAN-SF data comes from: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EBCFKM,
we use the preprocessed version as discussed in our paper.
* All experiments are done with python 3.9.13, pytorch 2.1.0, numpy 1.25.2, pycatch22 0.4.2

