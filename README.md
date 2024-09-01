
# Real-Time Eye Tracker

A realtime eye-tracking device utilizing EOG sensors combined with 3 (horizontal, vertical, blink eye movement classifiers) randomforest classification models. Data acquisition was performed via microcontroller and processed in real-time using a Python script running on a desktop.

- HorizontalDataset: The dataset used to train a classifier on horizontal eye movement. Label=0 means leftward eye movement, label=1 means no horizontal movement and label=2 means rightward eye movement.

- VerticalDataset: The dataset used to train a classifier on vertical eye movement. Label=0 means downward eye movement, label=1 means no vertical eye movement and label=2 means upward eye movement.

- blinkDataset: The dataset used to train a classifier on eye blinking. Label=0 means no blink and label=1 means there is a blink.

- datasetCollector.py: This python script was used to collect data from the eog sensors to an excel sheet via a microcontroller.

- labelDataPoint.ipynb: This python notebook labels the data collected which is used to train the different ml models.

- mlTrain.ipynb: This python notebook uses the dataset created by **labelDataPoint.ipynb** to train the 3 randomforest models.

- realTimeInference.py: Efficiently makes real-time inferences on eye movement and prints it on the terminal.

- realTimePrediction.py: The real-time predictions are processed to ensure higher accuracy of eye movement prediction and this is considered as the final prediction to be printed omn the terminal.

