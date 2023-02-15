# Modifying binary cross entropy loss function to handle class imabalance

In this assignment from Coursera, I have used a pretrained model: DenseNet to detect 14 different types of conditions of chest: Cardiomegaly, Emphysema, Effusion, Hernia, Infiltration, Mass, Nodule, Atelectasis, Pneumothorax, Pleural_Thickening, Pneumonia, Fibrosis, Edema, and Consolidation.

Since datasets are heavily imbalanced (cell 10 of ChestXRay_Diagnosis.pynb), I have built my own custom loss function. At first, I have calculated the positive and negative frequency for each class. Consequently, I have modified the binary cross entropy loss function by penalizing the mistakes heavier of cases that occur rarely. On the other hand, cases that occur in abundance are penalized with less weight. With this key idea, the custom loss function addresses class imbalance.

To asses the model performance, ROC Curve is used. The x axis of the graph demonstrates the false positive rate (1 - Specificity) and the y-axis relates to the true positive rate (Sensitivity). I have also used GradCam to find out which part of the images the model relies on when performing classifications.
