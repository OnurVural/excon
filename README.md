# excon
This paper introduces EXCON, a novel contrastive representation learning framework designed to enhance classification performance amidst such imbalances. EXCON operates through four stages: (1) extracting core features from multivariate time series (MVTS) data; (2) generating distinctive contrastive representations for each class to maximize inter-class separation; (3) training a temporal feature embedding module with a custom contrastive reconstruction loss to capture dynamic patterns; and (4) applying a classifier to the learned embeddings for robust classification.

# Content Details
* <code> DATA\catch22 </code> contains data points, including extracted catch22 feature vectors and the contrastive extremes.

* <code> DATA\Preprocessed-SWANSF-main </code> contains preprocessed SWAN-SF data points, in case of training all components from scratch, the folders to keep data files must be placed under here (names and paths can be specified while running the relevant notebook cells).
* Desired datasets may be placed here for excon-p2.ipynb
  
* <code> src/ </code> The details for each notebook file are as follows:
  - <code>excon-p1.ipynb</code>: This module is a step-by-step guide to our experiments of SWAN-SF a single notebook file.
  - <code>excon-p2.ipynb</code>: This module is a step-by-step guide to our extended edition experiments in a single notebook file.
    
# Execution Details 
* To view our modules, experiments, and results in a single file, each ipynb file is sufficient.
* Since SWAN-SF is a large dataset, we do not include the preprocessed dataset in DATA\Preprocessed-SWANSF-main, if you need to train the components and start the experiments from scratch, don't hesitate to contact us!
* Original SWAN-SF data comes from: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EBCFKM,
we use the preprocessed version as discussed in our paper.
* All experiments are done with python 3.9.13, pytorch 2.1.0, numpy 1.25.2, pycatch22 0.4.2

