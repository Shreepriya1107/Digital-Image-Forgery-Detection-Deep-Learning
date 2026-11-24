# Digital Image Forgery Detection Using Deep Learning

## Abstract

Digital image forgery has become a significant concern with the increasing use of digital images and image editing technologies. Manipulated images can spread misleading information, create false evidence, and compromise the authenticity of digital content. Therefore, identifying whether an image is authentic or forged has become an important application of deep learning and computer vision.

This project, **Digital Image Forgery Detection Using Deep Learning**, develops an automated image classification system to distinguish between authentic and forged images using Convolutional Neural Networks (CNNs) and transfer learning techniques.

The project uses the CASIA 2.0 Image Tampering Detection Dataset and explores multiple deep learning experiments using PyTorch, including optimizer comparison, regularization, data augmentation, and pretrained CNN architectures.

The implemented models are evaluated using accuracy, precision, recall, F1-score, and ROC-AUC. An interactive Gradio-based interface is also developed to allow users to upload images, select a trained model, and obtain predictions.

## Objectives

- Develop a deep learning-based system for digital image forgery detection.
- Classify digital images into Authentic and Forged categories.
- Implement CNN models using PyTorch.
- Compare Adam and SGD optimization techniques.
- Implement Dropout and L2 Weight Decay for regularization.
- Apply image data augmentation using Torchvision.
- Implement transfer learning using ResNet18 and MobileNetV2.
- Evaluate model performance using standard classification metrics.
- Develop an interactive Gradio application for image prediction.

## Dataset

**Dataset:** CASIA 2.0 Image Tampering Detection Dataset

The dataset contains two categories of images:

| Category | Number of Images |
|---|---:|
| Authentic | 7,501 |
| Forged | 5,133 |
| Total | 12,634 |

The dataset is used to train and evaluate the deep learning models for binary image classification.

Dataset source: [CASIA 2.0 Image Tampering Detection Dataset – Kaggle](https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset)

*Note: Dataset counts should be verified against the actual files used in the experiments.*

## Technologies Used

- Python
- PyTorch
- Torchvision
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab
- Gradio
- Kaggle

## Laboratory Concepts Implemented

The project incorporates the following five laboratory concepts:

1. **PyTorch Fundamentals:** Understanding tensors and automatic differentiation using Autograd.
2. **Optimizers:** Implementing and comparing Adam and SGD optimization techniques.
3. **Regularization:** Applying Dropout and L2 Weight Decay to reduce overfitting.
4. **CNN and Data Augmentation:** Implementing a custom CNN and applying image transformations using Torchvision.
5. **Transfer Learning:** Using pretrained ResNet18 and MobileNetV2 architectures for image classification.

## Models Implemented

The following model configurations are experimentally evaluated:

- Custom CNN (Adam)
- Custom CNN (SGD)
- Regularized CNN (Dropout + L2 Weight Decay)
- CNN with Data Augmentation
- ResNet18
- MobileNetV2

## Experimental Results

The models are compared using accuracy, precision, recall, F1-score, and ROC-AUC.

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|---|---:|---:|---:|---:|---:|
| Custom CNN (Adam) | 59.39% | 0.0000 | 0.0000 | 0.0000 | 0.5006 |
| Custom CNN (SGD) | 59.39% | 0.0000 | 0.0000 | 0.0000 | 0.5000 |
| Regularized CNN | 59.39% | 0.0000 | 0.0000 | 0.0000 | 0.4994 |
| Augmented CNN | 63.55% | 0.5884 | 0.3416 | 0.4322 | 0.6520 |
| ResNet18 | 75.63% | 0.6504 | 0.8649 | 0.7425 | 0.8017 |
| MobileNetV2 | 74.68% | 0.6690 | 0.7455 | 0.7052 | 0.8178 |

### Key Observations

- ResNet18 achieved the highest accuracy of 75.63%.
- ResNet18 achieved the highest F1-score of 0.7425.
- MobileNetV2 achieved the highest ROC-AUC of 0.8178.
- Data augmentation improved performance compared with the initial custom CNN experiments.
- The initial custom CNN configurations produced zero precision, recall, and F1-score for the evaluated positive class, indicating that their classification behaviour requires further investigation.

## Evaluation Metrics

The following metrics are used for model evaluation:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve and ROC-AUC

Training and validation accuracy and loss graphs, confusion matrices, ROC curves, and comparative visualizations are generated to analyze model performance.

## Web Application

The project includes an interactive **Gradio-based Image Forgery Detection System**.

Users can:

- Upload an image.
- Select a trained deep learning model.
- Submit the image for classification.
- View the model's prediction.

The application performs image-level classification into Authentic or Forged categories.

## Conclusion

This project demonstrates the application of deep learning and transfer learning techniques for digital image forgery classification. The experimental comparison indicates that pretrained CNN architectures, particularly ResNet18 and MobileNetV2, achieved better classification performance than the initial custom CNN configurations.

Among the evaluated models, ResNet18 achieved the highest accuracy, while MobileNetV2 achieved the highest ROC-AUC. These results highlight the potential of transfer learning for image forgery classification.

The integration of a Gradio interface provides an interactive way to test images using the trained models. Further experimentation and optimization are needed to improve classification performance and generalization.

## Future Scope

- Improve model performance through hyperparameter tuning.
- Experiment with additional training epochs and evaluate convergence.
- Implement pixel-level forgery localization using suitable annotations and segmentation techniques.
- Explore advanced deep learning architectures.
- Evaluate performance on additional image forgery datasets.
- Enhance the web interface with prediction confidence and visual explanations.

## How to Run the Project

1. Open the project notebook in Google Colab.
2. Configure Kaggle API authentication.
3. Download and extract the CASIA 2.0 dataset.
4. Execute the preprocessing and training cells.
5. Evaluate the trained models.
6. Launch the Gradio application for image prediction.

## References

1. [CASIA 2.0 Image Tampering Detection Dataset – Kaggle](https://www.kaggle.com/datasets/divg07/casia-20-image-tampering-detection-dataset)
2. [PyTorch Documentation](https://pytorch.org/docs/stable/index.html)
3. [Torchvision Documentation](https://pytorch.org/vision/stable/index.html)
4. [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)
5. [MobileNetV2: Inverted Residuals and Linear Bottlenecks](https://arxiv.org/abs/1801.04381)

## Author

**Shreepriya Kasulabada**

- Hall Ticket Number: 2403A51099
- Batch: 04

**Faculty Guide:** Dr. Anurodh Kumar  
Associate Professor  
Department of Computer Science & Artificial Intelligence

**Institution:** SR University
