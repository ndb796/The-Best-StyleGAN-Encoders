## The Best StyleGAN Encoders

### Datasets

* All datasets are based on the [CelebAMask-HQ](https://github.com/switchablenorms/CelebAMask-HQ) dataset.
    * The original dataset contains 6,217 identities.
    * The original dataset contains 30,000 face images.

#### Celeb-HQ Facial Identity Recognition Dataset

* This dataset is <b>curated</b> for the facial identity classification task.
* There are <b>307 identities</b> (celebrities).
    * Each identity has <b>15 or more</b> images.
* The dataset contains 5,478 images.
    * There are 4,263 train images.
    * There are 1,215 test images.
* [Dataset download link (527MB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ES-jbCNC6mNHhCyR4Nl1QpYBlxVOJ5YiVerhDpzmoS9ezA)

<pre>
<b>Dataset/</b>
    <b>train/</b>
        identity 1/
        identity 2/
        ...
    <b>test/</b>
        identity 1/
        identity 2/
        ...
</pre>

#### Celeb-HQ Face Gender Recognition Dataset

* This dataset is <b>curated</b> for the face gender classification task.
* The dataset contains 30,000 images.
    * There are 23,999 train images.
    * There are 6,001 test images.
* The whole face images are divided into two classes.
    * There are 11,057 <b>male</b> images.
    * There are 18,943 <b>female</b> images.
* [Dataset download link (2.54GB)](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EZ-LQXHjSztIrv5ayecz_nUBdHRni8ko4p_vCS1zypkhOw)

<pre>
<b>Dataset/</b>
    <b>train/</b>
        male/
        female/
    <b>test/</b>
        male/
        female/
</pre>

### Classification Models

* All classification models are based on [ImageNet pre-trained models](https://pytorch.org/vision/stable/models.html).
    * Transfer learning is used because the dataset size is small.
* The test accuracies are reported as follows:
    * There are 1,215 test images for identity recognition.
    * There are 6,001 test images for gender recognition.

1. The size of input images is <b>224 X 224</b> resolution.

||Identity recognition|Gender recognition|
|:---|---:|---:|
|VGG19|62.88% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_VGG19_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERqtpqjtkIhAs2Q5H28CRR0B5eJzRrxMq_6RaFNvrDW-0A))|97.83% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_VGG19_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EQSvN1P99ANJnL_T_k1Ny_QBZi7sgmzM5cVuhEG97dC9MQ))|
|ResNet34|86.34% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet34_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/Ebp8bPYd9FdClrzYmAptAVIBMqKhjyOT26Ew5nnAHlEPcQ))|98.30% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet34_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERUDrWOiNwRCqfFNykIzjYoBTnShKj3U15sJZs1TacJgLw))|
|ResNet101|86.67% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfZuTpqXwPFAo8jJfzdQWPABkW4qkAne745MfjT1F3gbgQ))|98.40% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EV0cM9vCZexOlBgII7Ky8mMB70jNR7Ds-6YQ0kPNX5lvMA))|

2. The size of input images is <b>256 X 256</b> resolution.

||Identity recognition|Gender recognition|
|:---|---:|---:|
|MNasNet1.0|78.85% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_MNASNet_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EanV-2422p1Onm2Qqsx1XyoBkkgfIpxXz50xq30frin3Og))|98.35% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_MNASNet_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERhbbjsN6aBCuCoSaH1R-LYBsOigeeSbweYu6RBMsvsr9A))|
|DenseNet121|85.51% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_DenseNet121_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EffriJXe9_1GpS99dxGiE8MBhZdi-xxdM0_UDj1UrZhDig))|98.38% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_DenseNet121_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfwYi4E67U5ChAwjAYeWLwwB3nCRxkDnB9X7sv1c1gn9ew))|
|ResNet18|86.34% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet18_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EYGLTNxpuPNIgvA9llxUmykBMbpnKBm7jhwJOmL7-XbgVw))|98.30% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet18_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EagNww3nBL9NmgVg0WDzdVcBUMtgD_gG6zNer1YnAL0jgQ))|
|ResNet101|87.65% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ES48F28hK45EiCLx6RyR3b8BDA9v4qcB0cP9pOxSx4kRuQ))|98.28% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_256.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EeSI1pacl-1DriGGm01I4IkBLU834yp87cuh9s4BX3UT9Q))|

3. The size of input images is <b>256 X 256</b> resolution (normalization 0.5).

||Identity recognition|Gender recognition|
|:---|---:|---:|
|MNasNet1.0|78.35% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_MNASNet_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EWItNQMfZaVNovgdLgousNwBqhVe5gifzy9plKe4dObTpg))|98.38% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_MNASNet_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ETr-45CBFQdBpkPU9FJyYi0B_Knk4zRBq0MZ76hiod3bhg))|
|DenseNet121|86.42% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_DenseNet121_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EYHdbwJ5xTRCl4l5pJq7FFcBuM7QNJ3ZA1z7dgUP969XNw))|98.15% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_DenseNet121_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EYb6xTPoB3hNsQhgCCDxMucBrvGwYW2_5_7gdAoHwsm81w))|
|ResNet18|87.82% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet18_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EX15A0wm8MBLrBsT-9ARA-gBZ6W-RwmSw1IgYZzan4dELg))|98.55% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet18_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfvDuXQT285MtP738FodJnQBa8_qF6sW6K2KyAfRzNbiAw))|
|ResNet101|87.98% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfSWIIet9s1IjzrCztPrcN0BnVSDMPNH0YPc3U6xC7YiYg))|98.05% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_256_Normalize_05.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EYVchyAgv5NHvGsXbApEphIBvzgCSWm_o_pk3DzLwuxIug))|

### Encoding (Inversion) Methods Comparison

* For experiments, the three functions are required.
    * E(???) is an encoding method that maps an image into a latent vector.
    * G(???) is the StyleGAN2 model that generates an image given a latent vector.
    * F(???) is a classification model that returns a predicted label.
* We can compare the performances of various encoding methods given a dataset that contains (image x, label y) pairs.
    * <b>Consistency accuracy</b> denotes the ratio of test images such that F(G(E(x))) = F(x) over all test images.
    * <b>Correctly consistency accuracy</b> denotes the ratio of test images such that F(G(E(x))) = F(x) and F(x) = y over all test images.

* Identity recognition:

||Consistency accuracy|Correctly consistency accuracy|Similarity score|LPIPS loss||
|:---|---:|---:|---:|---:|---:|
|[pixel2style2pixel (pSp)](https://github.com/eladrich/pixel2style2pixel)|70.78%|67.00%|0.6465|0.1504|([code](./inversion_methods/pSp.ipynb) \| [custom dataset](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EQIF7ZqRxDJCjTwWiO1xPe4BqpenC93AEpTnRpSOlrPl5g))|