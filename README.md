# MosquitoVerbalization

The goal of this project is to train a machine learning model to be able to look at an image of a mosquito and verbalize the features of that mosquito that are relevant to determining the species of the mosquito in the image. We trained multiple models and compared them against each other to determine which one would be best to use for this task.

# Use Directions

Download all of the files included in the GitHub and leave them in their current structure. Do not move any of the files around or remove any of the scripts from the folder that they are in. Download all of the packages in the requirements.txt file. Run either of the .ipynb files in your software of choice.

git clone https://github.com/Joeywroberts/MosquitoVerbalization.git  

conda create -n mosqverb python=3.10  

conda activate mosqverb  

pip install -r requirements.txt  

Make sure to run code in the newly created environment above.

# Included files

**requirements.txt** - A list of the required Python packages needed to run the scripts in this GitHub.

**Mosquito_Verbalization_Training&Comparison.ipynb** - Training and testing script for comparing the 5 different models tested and saves the final state of each of the models. Includes evaluations like ROC curve, accuracy, and precision.

**Mosquito_Data (folder)** - Contains all of the data for both the train and test scripts as well as the sample testing script. It contains the following files:

 &emsp; **images_manifest_species.csv** - Raw feature data for each image for training models.  

 &emsp; **manifest_clean.csv** - Clean feature data for each image from training models.


 &emsp; **Sample_manifest** - Feature data for sample data to compare to inferences in sample testing script.

 &emsp; **glossary.csv** - Glossary of text for a 1 or 0 for each feature as a lookup table for verbalization.  

 &emsp; **Mosquito_Images (folder)** - Folder of mosquito images separated by species and within species by a unique mosquito ID for training.  

 &emsp; **Sample_Images (folder)** - Same as mosquito images folder but not used in training, used for inference examples in sample testing file.    

**Sample_Testing.ipynb** - Script to choose one of the trained models and run a sample inference on the sample images data that was not trained on to show an example output and explore different models.

**model_convnext_tiny.pth, model_efficientnet_b2.pth, model_mobilenet_v3.pth, model_resnet50.pth, model_vit_b_16.pth** - Files for the trained data of each model used in the sample testing file to switch between models and run inference on new data using them.

**Train&Comparison.pdf, Sample_Test.pdf** - Pdf file of the run notebooks for visualization of what the fully run file looks like. The training and comparison file pdf has slightly different code, but only in the first few cells, as it was adapted to be run in Google Collab for the pdf creation.
