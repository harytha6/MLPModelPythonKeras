# MLPModelPythonKeras  

### Description
A Keras mlp model developed to classify humans in a car seat with the help of ultrasonic sensor data.  

### Components
The folder Documentation contains the report of this work, along with some images.  
The folder Model Training has a couple of Python notebooks (.ipynb files). The file names starting with "backup_...." are only intended as a backup to store all of the combinations that have been tried in this work. Only the files "ACF-PSD.ipynb" and "ANN-Keras-PSD" are important. 



|File Name   | Description  |
|---|---|
|"ACF-PSD.ipynb"    | Convert ADC Data stored in a Folder to PSD format to be saved locally in another folder   | 
|"ANN-Keras-PSD"	  | Train the model with PSD files generated earlier with a MLP model |   
| MLP_21.07.2023.keras  | Name of the file that stores the MLP calibrated Model's configuration  |  
|  ModelTraining/aa_measurements | contains all of the measurements   |
   
   

#### Measurement Variations and their corresponding Labels

| Label suffixed to File Name | Description of experimental setup |
|---|---|
|leanedleast | seat more upright |
|leanedmiddle | normal default position with medium level of inclination |
|lhupfdown  | baby's left hand raised up a little and feet in default position (pressed down to the seat) |
|lfup | left foot raised up |
|rfup | right foot raised up |

***Note :
Some individual measurement files are zipped due to the size being > 50 MB. These need to be unzipped before they could be used in the Python Notebooks.

#### How to Load Saved Model

```python
# Keras package needs to be imported to run the below line of code
reconstructed_model = keras.models.load_model("MLP_21.07.2023.keras")
```
