# ECEN758
For ECEN 758 Data Mining Final Project

This is a multi-label audio classifying CNN trained on the FSD50k dataset. Given a WAV audio file, it will produce probabilities between 0–1 for each of the 200 FSD50K sound classes.

**Downloading**

It is recommended to download the FSD50K dataset locally using db_download.ipynb and run the CNN classifier in base_classifier.ipynb on your local machine rather than Google Colab as the dataset is over 32GB in size. After all files download, the zip files will need to be extracted and arranged so that the file hirarchy matches the following image:

<img width="292" height="265" alt="image" src="https://github.com/user-attachments/assets/8434b451-46b4-4861-ac3f-b824b43d1178" />


**Running**

Running the entire base_classifier.ipynb will rebuild, retrain, and evaluate the model, and fsd50k_cnn.h5 is the trained CNN classifier. If you don't want to retrain the model and only want to evaluate it, only run the Evaluation Scores and Prediction code blocks at the bottom of base_classifier.ipynb.
