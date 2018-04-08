# Skin-Lesion-Analysis-for-Melanoma-Detection
HackOverFlow Project by Parth Iramani: Detection of Skin disease using Computer Vision

Skin cancer is a major health problem in India, especially in rural regions which lack educated and experienced dermatologist. Melanoma is one the deadliest form of skin cancer, which causes a tumour in the melanin-forming cells. Melanoma Cancer is less prevalent in India than it is in the western countries, but the rate at which people are getting affected is increasing. This project aims at detecting the cancer and classifying it whether it is a malignant or benign. We take Images of the cancer infected skin and classifying those images into malignant and benign. The images were taken from the International Skin Imaging Collaboration(ISIC) archive.

We have used Convolutional Neural Networks, using keras and tensorflow in python, for training a model for detection of malignant cancer. This model is compared with classical machine learning algorith models like SVM, Random Forest, GBM etc. Comparing between these models, we come to the conclusion that CNNs give us the best model in this case.

We have done some image preprocessing to make the data better suited to use in the model. The images are resized and segmented using Image Thresholding Techniques.
Using Keras, we implemented a 6-layered CNN, and calculated the accuracy of the model.
The accuracy was 80.25% on the Testing data.

Using sklearn, we implemented a Decision Tree Model, a Random Forest Model, a GBM model, and a SVM model, and calculated their accuracies.
The accuracy for the Decision Tree model on the Testing Data was 65.5% using 'gini' as a parameter, and 69.5%, using entropy as a parameter.
The accuracy for the Random Forest model on the Testing Data was 78.83%
The accuracy for the GBM model on the Testing Data was 76.167%
The accuracy for the SVM model on the Testing Data was 80.5% which is surprising, as it is better than the acuuracy of the CNN model, but the catch is that the SVM model predicted all the images to be benign, hence being completely useless, since it could not handle the class imbalance.

Hence, we conclude that the CNN model worked best for detection of Melanoma in Skin Lesions.

Scope for Improvements:
1) Using higher resolution for the images. We resized the images to (64, 64, 3). Using a higher resolution (like (512, 512, 3) would improve the accuracy of the model
2) Using Data Augmentation, we can increase the noise in the data, which will help in avoiding overfitting. Creating new data by translation, rotation and fliping of the images would significantly improve the model.
3)Using Transfer Learning, we can initialize the weights to values that proved to be very efficient in different models for image classification. This will significantly improve the model.
4) Lastly, add more layers ;-P
