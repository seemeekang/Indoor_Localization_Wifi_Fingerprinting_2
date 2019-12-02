# Indoor Localization with Wi-Fi Fingerprinting database
PCA (Principal Component Analysis) and Semi-supervised AAE (Adversarial Auto-Encoder)

## Dataset
UJIIndoorLoc (https://archive.ics.uci.edu/ml/datasets/ujiindoorloc)

## Packages
- python 3.7
- pytorch 1.3
- matplotlib
- numpy

## Outcome
- Building prediction: 99.91%
- Floor prediction: 84.97%
- Longitude / Latitude prediction:
    1. Mean error (Euclidean distance): 13.56 m
    2. Max error (Euclidean distance): 92.46 m
    3. Min error (Euclidean distance): 0.03 m
    4. Standard deviation (Euclidean distance): 10.33 m
    5. Variance: 106.72
    
## Further Improvements
- Semi-supervised AAE (Adversarial Auto-Encoder) implementation
    - Denoising effect + Dimension reduction effect
    - No need to know the prior distribution of the sample
    - Cheaper cost than labelling

- Frequency domain analysis
    - Digital filters
    
- Towards seamless real-time user experience with optimal performance using low battery consumption
    - Inference request frequency optimization at online phase
    - Battery consumption estimation
    - Device characteristics consideration
    - Shifting from/to GPS system
    
## Reference
- http://giant.uji.es/blog/convnet/convnet.html
- https://github.com/armin-talic/Indoor-Positioning-Via-Wifi-Fingerprinting
- https://rstudio-pubs-static.s3.amazonaws.com/393608_8cf0481dbc8b4c40b56b7b2ca0e543c9.html
- http://evaal.aaloa.org/2015/technical-annex-offsite
- https://towardsdatascience.com/a-wizards-guide-to-adversarial-autoencoders-part-4-classify-mnist-using-1000-labels-2ca08071f95
- https://blog.paperspace.com/adversarial-autoencoders-with-pytorch/
- https://arxiv.org/abs/1907.09514
- https://arxiv.org/abs/1511.05644