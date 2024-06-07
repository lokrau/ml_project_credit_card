# Machine Learning Projekt - Lorenz Krause (1840200)

## Daten
Die entscheidung viel darauf die Datenbeschaffung und die Verarbeitung in zwei Notebooks zu separieren, um zu vermeiden, dass die Daten bei mehrfacher Ausführung des Notebooks erneut heruntergeladen werden müssen.

### Datenbeschaffung
Die im Rahmen dieses Projekts verwendeten Daten werden von Kaggle heruntergeladen. Dazu wird ein Kaggle Account mit einem API Roken benötigt. Dieser Token kann wie [hier](https://www.kaggle.com/docs/api) zu sehen erstellt werden. Der Download der Daten erfolgt über das Notebook `data_download.ipynb`.

### Datenverarbeitung
Die Daten werden anschließend im Notebook `data_preperation` weiterverarbeitet, um sie für das Training der Modelle vorzubereiten. Dabei erfolgt eine Unterteilung in Trainings-, Test- und Validierungsdaten.

## Training
Das Training der Modelle erfolgt in drei unterschiedlichen Notebooks. Dabei wird zwei mal das selbe neuronale Netzwerk mit zwei unterschiedlichen Tunern optimiert und ein weiteres Modell mit einem Random Forest trainiert. Dabei wird für beide neuronale Netzwerke die Batch Size so optimiert, dass der Validierungsverlust möglichst gering ausfällt. Die Notebooks sind wie folgt benannt:
- `train_keras_tuning.ipynb`: Neuronales Netzwerk mit Keras Tuner optimiert
- `train_wandb_tuning.ipynb`: Neuronales Netzwerk mit Weights and Biases optimiert
- `train_random_forest.ipynb`: Random Forest Modell


Das Ziel ist in `train_wandb_tuning.ipynb` aufzuzeigen, wie der komplette Prozess samt des Hyperparameter Tunings mit Weights and Biases durchgeführt und aufgezeichnet werden kann. In `train_keras_tuning.ipynb` wird das gleiche Modell mit dem Keras Tuner optimiert, um die Unterschiede zu verdeutlichen und das Vorgehen mit einem anderen Tuner zu zeigen. In `train_random_forest.ipynb` wird ein Random Forest Modell trainiert, um zu untersuchen, ob es in diesem Fall wirklich einen Vorteil bringt, ein neuronales Netzwerk zu verwenden.
