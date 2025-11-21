# ECEN758
For ECEN 758 Data Mining Final Project

This is a multi-label audio classifying CNN trained on the FSD50k dataset. Given a WAV audio file, it will produce probabilities between 0–1 for each of the 200 FSD50K sound classes.

**Downloading**

It is recommended to download the FSD50K dataset locally using db_download.ipynb and run the CNN classifier in base_classifier.ipynb on your local machine rather than Google Colab as the dataset is over 32GB in size. After all files download, the zip files will need to be extracted and arranged so that the file hirarchy matches the following image:

<img width="292" height="265" alt="image" src="https://github.com/user-attachments/assets/8434b451-46b4-4861-ac3f-b824b43d1178" />

**Running**

Running the entire base_classifier.ipynb will rebuild, retrain, and evaluate the model. The file fsd50k_cnn.h5 is the trained CNN classifier, as it is included in this repository you may download and evaluate it directly if you wish to avoid spending a signigicant amount of time training the model.

**Important Notes About Running base_classifier.ipynb**

Most of the code blocks in base_classifier.ipynb must be executed at least once per session to load essential variables, preprocessing functions, datasets, and the model architecture into memory.

Only the block directly under the “Training Model” markdown performs the actual time-consuming model training and may be skipped.
All earlier blocks define:

- dataset paths
- label encodings
- preprocessing functions
- TensorFlow datasets
- model architecture
- custom metrics
- cached mel-spectrogram loading logic

These components must be initialized in the current Python session before you can load or evaluate the model.

**If you want to rebuild and retrain the model**

Simply run all cells in order, including the “Training Model” section.

**If you want to skip retraining and only evaluate the model**

Do the following:

Run every code block except the one under “Training Model”.
These blocks restore all session variables and load cached mel-spectrograms.

Then run the Evaluation Scores and Prediction sections at the end of the notebook. The prediction sections may be rerun with different WAV file paths if you wish to classify other samples.
