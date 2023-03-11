# DoubleAU-Net
This file will give a short explanation about how to run our notebook – how to train from scratch, load a trained model, choose between different datasets, change hyperparameters and more.
A.	Datasets paths:
Data path – should be the folder name that contains the dataset in a .zip format.
config['data_path'] = '/content/gdrive/MyDrive/Datasets/’
We uploaded to our shared drive both datasets:
1)	In: Datasets/original/ – both of the original datasets.
2)	In: Datasets/splitted augmented data/ – our data after doing augmentation and splitting it into train ,validation and test sets (80%/10%/10%). 

We recommend using the augmented data to save time.
B.	Choose datasets:
In order to choose between the datasets you want to work with you should update in the config:
#config['dataset'] = 'bowl'
config['dataset']= 'CVC'
1)	When working with ‘bowl’ dataset, the relevant code cells for (D) creating new data or (E) Load data are 1,2,4.
2)	When working with ‘CVC’ dataset, the relevant code cells for (D) creating new data or (E) Load data are 1,2,3.
C.	Interpolation:
In case you want to use our interpolation technique you choose it in the config code:
config ['use_interpolation'] = True

D.	Creating new data (optional):
1)	If you want to use the original data and create your own split augmented data you should update in the config code this line as True:
config['first_time_data_arrangement'] = True

a.	Run section 1,2,3 to create ‘CVC’ split augmented data .zip file to your Google Drive.
b.	Run section 1,2,4 to create ‘bowl’ split augmented data .zip file to your Google Drive.
2)	After creating new data, Restart run time, and use your new data as (E) Load data describes.

E.	Load data (must):
In case your augmented data is ready (by using our augmented data/your augmented data).
1)	If you want to use ready split augmented data, set as False config['first_time_data_arrangement'] = False
a.	Run code cells 1,2,3 to load ‘CVC’ split augmented data .zip file to your Google Drive.
b.	Run code cells 1,2,4 to load ‘bowl’ split augmented data .zip file to your Google Drive.
2)	Proceed for train or test sections.

F.	Train:
1)	Load Data 
2)	Run code cells 5-7.
3)	Output path – should include the output folder path with the “/output/” ending.
config['output_path'] = '/content/gdrive/MyDrive/output/'
This is where we save the model, metrics and more.

G.	Test:
1)	Load Data.
2)	Update model path in code cell 8.
3)	Run code cells 8-10

H.	Load model and test:
1)	Load data.
2)	Run code cells 5.
3)	Change in code cell 8 folder_in_output to the wanted folder in output path to load from
4)	Run code cells 8,9,10. 
5)	You can choose between your trained model, or use our saved models which are the best we achieved.
Our models can be found in:
Best results/bowl/
Best results/CVC/

		
NOTE: The model’s name in our code is called DoubleUNet because we first implemented the DoubleUNet and on top of the base notebook we added our changes. We didn’t change the variable’s name when we implemented our DoubleAU-Net. To be clear, the model in the notebook is our DoubleAU-Net.
