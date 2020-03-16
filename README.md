# Indoor Localization with Wi-Fi Fingerprinting database


* Ensemble averaging
* Gradient boosting / Random forest (lightbgm and sklearn)
* Scenario-based (time-series) CNN
    1. Sort by user
    2. Sort by time 
    3. Concatenate instances into images by scenario (group by time-series) 
    4. Feed the images to CNN as a video (sliding window)
* (TODO) DCGAN for domain adaptation

## Dataset
UJIIndoorLoc (https://archive.ics.uci.edu/ml/datasets/ujiindoorloc)

## Packages
- python 3.7
- pytorch 1.3
- matplotlib
- mpl_tookits
- numpy
- scipy
- sklearn
- lightgbm

## Outcome
- Building prediction: 
    - Ensemble averaging: 99.91%
    - Random forest: N/A
    - Scenario-based (time-series) CNN: 100%

- Floor prediction: 
    - Ensemble averaging: 84.97%
    - Random forest: 91.53%
    - Scenario-based (time-series) CNN: 87.48%

- Longitude / Latitude prediction:
    1. Mean error (Euclidean distance): 
        - Ensemble averaging: 13.56 m
        - Gradient boosting: 16.14 m
        - Scenario-based (time-series) CNN: N/A
    2. Max error (Euclidean distance): 
        - Ensemble averaging: 92.46 m
        - Gradient boosting: 182.70 m
        - Scenario-based (time-series) CNN: N/A
    3. Min error (Euclidean distance): 
        - Ensemble averaging: 0.03 m
        - Gradient boosting: 0.31 m
        - Scenario-based (time-series) CNN: N/A
    4. Standard deviation (Euclidean distance): 
        - Ensemble averaging: 10.33 m
        - Gradient boosting: 21.44 m
        - Scenario-based (time-series) CNN: N/A
    5. Variance: 
        - Ensemble averaging: 106.72
        - Gradient boosting: 459.56 m
        - Scenario-based (time-series) CNN: N/A
    
## TODO


- CNN improvement

- DCGAN for domain adaptation
    - Scalability
    - Reuse of previously trained CNN layers
    
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
- Choi, Jeongsik, Yang-Seok Choi, and Shilpa Talwar. "Unsupervised Learning Technique to Obtain the Coordinates of Wi-Fi Access Points." 2019 International Conference on Indoor Positioning and Indoor Navigation (IPIN). IEEE, 2019.
- Makhzani, Alireza, et al. "Adversarial autoencoders." arXiv preprint arXiv:1511.05644 (2015).
- Ibrahim, Mai, Marwan Torki, and Mustafa ElNainay. "CNN based indoor localization using RSS time-series." 2018 IEEE Symposium on Computers and Communications (ISCC). IEEE, 2018.
