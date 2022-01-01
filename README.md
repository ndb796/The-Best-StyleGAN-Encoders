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
    * All input images are resized to the 224 X 224 resolution.
* The test accuracies are as follows:
    * There are 1,215 test images for identity recognition.
    * There are 6,001 test images for gender recognition.

||Identity recognition|Gender recognition|
|:---|---:|---:|
|VGG19|62.88% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_VGG19_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERqtpqjtkIhAs2Q5H28CRR0B5eJzRrxMq_6RaFNvrDW-0A))|97.83% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_VGG19_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EQSvN1P99ANJnL_T_k1Ny_QBZi7sgmzM5cVuhEG97dC9MQ))|
|ResNet34|86.34% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet34_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/Ebp8bPYd9FdClrzYmAptAVIBMqKhjyOT26Ew5nnAHlEPcQ))|98.30% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet34_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/ERUDrWOiNwRCqfFNykIzjYoBTnShKj3U15sJZs1TacJgLw))|
|ResNet101|86.67% ([code](./classification_models/Facial_Identity_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EfZuTpqXwPFAo8jJfzdQWPABkW4qkAne745MfjT1F3gbgQ))|98.40% ([code](./classification_models/Face_Gender_Classification_Using_Transfer_Learning_with_ResNet101_Resolution_224.ipynb) \| [download](https://postechackr-my.sharepoint.com/:u:/g/personal/dongbinna_postech_ac_kr/EV0cM9vCZexOlBgII7Ky8mMB70jNR7Ds-6YQ0kPNX5lvMA))|

### Encoding (Inversion) Methods

* <b>Inversion accuracy</b> denotes the ratio of test images such that F(G(E(x))) = F(x).
    * E(ꞏ) is an encoding method that maps an image into a latent vector.
    * G(ꞏ) is the StyleGAN2 that generates an image given a latent vector.
    * F(ꞏ) is a classification model that returns a predicted label.

||Identity recognition|Gender recognition|
|:---|---:|---:|
|[pixel2style2pixel (pSp)](https://github.com/eladrich/pixel2style2pixel)| (code)| (code)|
