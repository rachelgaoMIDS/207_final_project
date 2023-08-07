# 207_final_project

## Team name:
BirdSong Sonatas

## Team members:
Rachel Gao

Amina Alavi

Hamsini Sankaran

Andrew Loeber

## Dataset:
https://www.kaggle.com/competitions/birdclef-2023

## Objective:
Bird species classifier using audio recordings and machine learning algorithms.

## Forewords:
The original BirdClef-2023 competition contained more than 260 bird species in the training dataset. Due to limitation in computing power, we selected 10 species for our project during baseline presentation time. For our final model, we further trimmed down our species selection to 3 species due to limitation in computing power. All files saved in this repo only contains the work done for the 3 species models as presented in the final presentation.

The label for the test dataset as provided by the competition is hidden, and since we trimmed down the number of species to 3 species for our models, we split the provided training dataset to train and test for our own model building purpose.

3 species selected: barswa, comsan, eaywag1

NOTE: ALL WORK WAS DONE IN SHARED GOOGLE DRIVE, THE RESULTS FROM THE NOTEBOOKS CAN BE SEEN IN THE NOTEBOOKS BUT THE DIRECTORY PATH NEED TO BE CHANGED IF YOU WANT TO RERUN THE NOTEBOOKS.

## Directories:

### 0.RAW_Data
All data as provided by the Kaggle competition for the 3 species selected:
- train_metadata.csv
- eBird_Taxonomy_v2021.csv
- Original audio files for each species can be downloaded from Kaggle
 
### 1.Train_Test_Split
The training data for the 3 species were split to train (70%) vs test (30%). All EDA and models were built using data from the training set only while the test set is preserved for inference at the end.
- Train_Test Dataset Construction.ipynb
  - Note: The train/test split was originally done for 10 species, but then we further down-selected 3 species out of the 10 species for our final presentation

### 2.Preprocessing
- np_object_extraction: to extract the train and test audio np object from librosa.load() to save downstream processing time
  - Extract_Train_Audio_Object_Librosa.ipynb
  - Extract_Test_Audio_Object_Librosa.ipynb
  - The audio np objects are too large to fit into the repo, the two notebooks can be ran in colab to extract the audio np objects
- metadata: train & test metadata for downstream tasks
- train_preprocessing_&_EDA: preprocess training data and perform EDA
- test_preprocessing_&_EDA: preprocessing test data and perform minimal EDA

### 3.Notebooks
Notebooks from each member of the team

### 4.Inference
Models used for inference & inference results

Inference results presented in final presentation:
- CNN1D model source: 3.Notebooks/RG/5.CNN1D/5b.8sec_4sec_overlap_with_embedding_continents_CNN1D.ipynb
- GRU-RNN model source: 3.Notebooks/HS/RNN/GRU/1.b.RNNGRU.ipynb
- Vision Transformer source: 4.Inference/Vision_Transformer/ViT_8s_stft_inference.ipynb

### 5.Presentation
- Baseline
- Final
