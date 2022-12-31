# ObjectDetection

Knowledge Engineering Final Project by Group ... (2022/12)
---------------------------------------------------------------------------------
---------------------------------------------------------------------------------

For the purpose of this project, we only focus on Dynamic Method, which is the 2nd method proposed by the original paper (Credit at the end of the file)

---------------------------------------------------------------------------------
Kaggle.json key file
---------------------------------------------------------------------------------
Since the number of files in folders of VOC 2012 dataset is very large, mounting this dataset from google drive crashes the google colab sessions. Thus, we download dataset directly from Kaggle website when we run the code. 

To download dataset from kaggle, you need a kaggle.json key. We provided this key file in the code base. If you like to download your own kaggle key from your account, use below instructions:

- Go to the Kaggle website (www.kaggle.com)

- Register for a Kaggle account (log in to the exsiting account if you already have one)

- Go to "My Account"

- Select "Create New API Token" under the API section to download the kaggle.json file

Test/train in google colab
---------------------------------------------------------------------------------

- connect to google colab GPU
- upload model to the left folder bar of google colab in pascal folder
- to manually upload a file in folder, right click on the folder and click upload
- Upload kaggle json file, using code snippet, to download dataset directly
- run code snippets in the order they are placed

In some notebooks, the directory of loading model, in test function, might have been changed to google drive directory. To make it compatible with manual upload of models, simply comment out those lines.

To only test a model, you need to comments out calling train_deep_q() function in main function, and directly run the test.

---------------------------------------------------------------------------------
Note: It is highly recommended to run the code with GPU since the runtime is around 30mins per epoch for the hierarchical model and around 1hour per epoch for the dynamic model.


Test-train split:
---------------------------------------------------------------------------------
 
In training, we use images listed in objectclass_train.txt file in datatset. For testing we use images listed in objectclass_val.txt file in datatset. 


Number of examples for different object categories do not differ significantly. For most classes, there are around 300 images for each class. However, among classes we tested, 'car' class has around 500 images. 

---------------------------------------------------------------------------------
The orginal paper is COMP 767 Final Project by Manoosh Samiei and Ruofeng Li. We're really appreciated for their idea, so that we can come up with our own contribution, which is presented in our Final Project.

## Credit

```
@misc{https://doi.org/10.48550/arxiv.2208.04511,
  doi = {10.48550/ARXIV.2208.04511},
  url = {https://arxiv.org/abs/2208.04511}, 
  author = {Samiei, Manoosh and Li, Ruofeng},
  keywords = {Computer Vision and Pattern Recognition (cs.CV), Artificial Intelligence (cs.AI), FOS: Computer and information sciences, FOS: Computer and information sciences}, 
  title = {Object Detection with Deep Reinforcement Learning},
  publisher = {arXiv}, 
  year = {2022},
  copyright = {Creative Commons Attribution 4.0 International}
}
```
