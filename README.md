# Multi-head-Mood-Classification-
This project predicts **facial expressions**, **valence**, and **arousal** from face images using **CNNs**. We experimented with ResNet, EfficientNet, SE-Net, and a custom CNN to compare performance.

The dataset contains **224x224 RGB face images**, **68 facial landmarks**, **8 expression labels** (Neutral, Happy, Sad, Surprise, Fear, Disgust, Anger, Contempt), and **valence/arousal values** in [-1, +1]. Uncertain or no-face images have valence/arousal = -2. The data is divided into train, validation, and test sets.

Models were trained using **dropout, gradient clipping, weight decay, EMA**, and **early stopping** for stability. 

For evaluation, we used **accuracy, F1-score, Cohen’s Kappa, Krippendorff’s Alpha, ROC-AUC, PR-AUC** for expressions, and **RMSE, correlation, CCC, SAGR** for valence and arousal.  

Results show that **EfficientNet outperformed ResNet and the base CNN** in both classification and regression tasks. Training and validation curves, as well as examples of correct and incorrect predictions, are included in the notebook.

