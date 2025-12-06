# MosquitoVerbalization

The goal of this project it to train a machine learning model to be able to look at an image of a mosquito a verbalize the features of that mosquito that are relavent to determining the species of the mosquito in the image. We trained multiple models and compared them against each other to determine which one would be best to use for this task.

# Use Directions
Download all of the files included in the github and leave them in their current structure. Do not move any of the files around or remove any of the script from the folder which they are in. Download all of the packages in the requirements.txt file. Run either of the .ipynb in your software of choice.

git clone [repo_url]  
conda create -n my_env python=3.10  
conda activate my_env  
pip install -r requirements.txt  
**Make sure to run code in newly created environment above.**

# Included files
**requirements.txt** - A list of the required python packages needed to run the scripts in this github.

**Mosquito_Verbalization_Training&Comparison.ipynb** - Training and testing script for comparing the 5 different models tested and saves the final state of each of the models. Inculdes evalutions like ROC curve, accuracy, and precision.

**Mosquito_Data (folder)** - Contains all of the data for both the train and test script as well as the sample testing script. it contains the following files:

 &emsp; **images_manifest_species.csv** - Raw feature data for each image for training models.  
 &emsp; **manifest_clean.csv** - Clean feature data for each image from training models.  
 &emsp; **glossary.csv** - Glossary of text for a 1 or 0 for each feature as a lookup table for verbalization.  
 &emsp; **Mosquito_Images (folder)** - Folder of mosquito images separated by species and within species by a unique mosquio ID for training.  
 &emsp; **Sample_Images (folder)** - Same as the moquito images folder but smaller, not used in training, used for inference in sample testing file.    

**Sample_Testing.ipynb** - Script to choose one of the trained model and run a sample inference on the sample images data that was not trained on to show an example output and explore different models.

**model_convnext_tiny.pth, model_efficientnet_b2.pth, model_mobilenet_v3.pth, model_resnet50.pth, model_vit_b_16.pth** - Files for the trained sata of each model used in the saple testing file to switch between models and run inference on new data using them.
