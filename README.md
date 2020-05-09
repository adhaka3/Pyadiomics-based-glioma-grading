# Pyadiomics-based-glioma-grading
This project uses the BRATS(Brain Tumor Segmentation Challenge) 2018 dataset to grade different types of brain tumors  (HGG and LGG) by extracting features by fusing the different MRI modalities present in the dataset.

The dataset contains 5 types of image: T1-weighted, T2-weighted, T1-contrast enhanced, FLair images and the segmented image. The segmented image(image which has only the tumor part) has 3 Region of Interest labeled as 1,2,4. I have made 3 segemneted images from the dataset as follows:
1. Using only the region labelled '1'.
2. Using region labelled '1' and '2'.
3. Using region labelled '1', '2' and '4'.

Now, the other 4 images (t1,t2,t1c and flair) are fused using DWT(discrete wavelet transform). 
The fused image and the 3 segmented images are used to extract features by Pyradiomics and different models are applied to get the results.

If you find any problem with the repository, please report an issue or if you have to give any feedback, please mail me at: ayushdhaka3@gmail.com

References:
[1] B. H. Menze, A. Jakab, S. Bauer, J. Kalpathy-Cramer, K. Farahani, J. Kirby, et al. "The Multimodal Brain Tumor Image Segmentation Benchmark (BRATS)", IEEE Transactions on Medical Imaging 34(10), 1993-2024 (2015) DOI: 10.1109/TMI.2014.2377694
[2] S. Bakas, H. Akbari, A. Sotiras, M. Bilello, M. Rozycki, J.S. Kirby, et al., "Advancing The Cancer Genome Atlas glioma MRI collections with expert segmentation labels and radiomic features", Nature Scientific Data, 4:170117 (2017) DOI: 10.1038/sdata.2017.117
[3] S. Bakas, M. Reyes, A. Jakab, S. Bauer, M. Rempfler, A. Crimi, et al., "Identifying the Best Machine Learning Algorithms for Brain Tumor Segmentation, Progression Assessment, and Overall Survival Prediction in the BRATS Challenge", arXiv preprint arXiv:1811.02629 (2018)
[4] van Griethuysen, J. J. M., Fedorov, A., Parmar, C., Hosny, A., Aucoin, N., Narayan, V., Beets-Tan, R. G. H., Fillon-Robin, J. C., Pieper, S., Aerts, H. J. W. L. (2017). Computational Radiomics System to Decode the Radiographic Phenotype. Cancer Research, 77(21), e104–e107. `https://doi.org/10.1158/0008-5472.CAN-17-0339 <https://doi.org/10.1158/0008-5472.CAN-17-0339>`_
