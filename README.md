# Project Description
The Machine Learning division is responsible for developing classification models to support the main application. This project includes two primary models:

1. **Skin Type Classification Model** (`model_skintype.h5`) - Identifies skin types from facial images.
2. **Skin Condition Classification Model** (`model_skinconditions.h5`) - Detects skin conditions such as acne, spots, or other issues from facial images.


## Project Structure

- `Face_condition_classifier.ipynb`: Notebook for training and testing the skin condition model.
- `Face_type_classifier.ipynb`: Notebook for training and testing the skin type model.
- `model_skintype.h5`: Pretrained model for skin type classification.
- `model_skinconditions.h5`: Pretrained model for skin condition classification.

# How to Use

### 1. Training the Model (Optional)
If you want to retrain the models, follow these steps:
1. Download the ZIP or clone this repository:  
   `git clone https://github.com/SkinPal/ML-Model-Development.git`
2. Extract the ZIP file (if downloaded) to your desired directory.
3. Upload the dataset folder to your Google Drive.
4. Open the `.ipynb` file using Jupyter Notebook or Google Colab.
5. Follow the notebook cells to:
   - Load the dataset (ensure it matches the directory of the uploaded dataset).
   - Perform data preprocessing.
   - Train the model.
6. Save the model in `.h5` format:

   ```python
   import tensorflow as tf

   # Save the skin type model
   model.save("model_skintype.h5")

   # Save the skin condition model
   model.save("model_skinconditions.h5")

   ```

### 2. Using the Model
To load the pretrained models, use the following code:

```python
import tensorflow as tf

# Load the skin type model
model_skintype = tf.keras.models.load_model("model_skintype.h5")

# Load the skin condition model
model_skinconditions = tf.keras.models.load_model("model_skinconditions.h5")
```



## Team Member - ML

| Bangkit ID | Name | Learning Path | University |LinkedIn |
| ---      | ---       | ---       | ---       | ---       |
| M312B4KY1803 | Humam Alwi Ahmad | Machine Learning| Universitas Sebelas Maret | [![text](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/humam-alwi-ahmad-46a440311) |
| M312B4KY1487 | Ferdy Rizkiawan | Machine Learning|	Universitas Sebelas Maret  | [![text](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ferdyrizkiawan) |
| M312B4KX1981 | Inge Najwa Aqiilah | Machine Learning| Universitas Sebelas Maret| [![text](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/inge-najwa-aqiilah-226667310) |




