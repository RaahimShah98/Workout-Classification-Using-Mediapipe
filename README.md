Workout_Classification (1).ipynb:

### 1. **Pose Feature Extraction:**
   - The code calculates various body angles and distances using key body points such as shoulders, knees, hips, ankles, and wrists. These features include:
     - Shoulder-to-knee distances (left and right)
     - Hip-to-ankle distances (left and right)
     - Ankle dorsiflexion angles (left and right)
     - Elbow flexion angles (left and right)
     - Additional angles such as shoulder flexion, body tilt, and wrist-shoulder distances
   - These features are crucial for distinguishing between different workout activities based on body posture and movement.

### 2. **LSTM Model Architecture:**
   - The model leverages an LSTM (Long Short-Term Memory) layer with bidirectional configuration to capture sequential data more effectively.
   - After the LSTM layer, `LayerNormalization` and `Dropout` layers are added to prevent overfitting and improve the generalization ability of the model.
   - A `Dense` layer with `softmax` activation is used at the end to classify the workout into multiple categories.

### 3. **Model Checkpointing and Early Stopping:**
   - The notebook utilizes two techniques to improve model training:
     - **ModelCheckpoint**: Saves the best model during training by monitoring the validation loss. This ensures that the model doesn't overfit and the best version is retained.
     - **EarlyStopping**: Halts the training process if the validation loss doesn't improve for 10 consecutive epochs, preventing overfitting and saving computational resources.

### 4. **Model Training:**
   - The model is trained on the dataset using a 100-epoch limit with a batch size of 32.
   - The validation data is used to assess the model performance, and training progress is monitored with checkpointing and early stopping mechanisms.


In order to check the model with live cam feed Open "main.ipynb"

Download the model from your google drive and load the model using load_model function
**NOTE**: In order to run the code in jupter-notebook first make sure you have installed all the necessary Dependencies. All required Dependencies used in the **main.ipynb** are written on the top.
