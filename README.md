# DCGAN, CGAN on MNIST
In this project, I build the DCGAN, CGAN networks and train them on MNIST dataset to generate digit images.

Multiple architecture depths, hyperparameters including batchsize, learning rate are tried to find the most well-perform setting.

Several improvement techniques for GANs, which are Virtual Batch Normalization, One-sided Label Smoothing, Balancing G & D to improve the quality of generated images and overcome the Mode Collapse issues. 

A LeNet digit classifier trained on MNIST, which has 0.990 test accuracy, is used to calculated TARR and Inception Score for CGAN. The classifier is trained with generated images to evaluate their quality, and improve the performance of the classifier.

The sysnthetic images from CGAN obtain a realistic asymptotic quality when TARR and IS calculated are close to those calculated in real data.

### DCGAN
All experiments can be conducted in the notebook `DCGAN.ipynb` 

### CGAN
All experiments can be conducted in the notebook `CGAN.ipynb`

### Retrain the classifier
Initialize the classifier by the synthetic data, then finetune it on real data: `Retrain1.ipynb`

Initialize the classfier by the real data, then finetune it on synthetic data: `Retrain2.ipynb`

Choose the confident sysnthetic data to train the classifier: `Retrain3.ipynb`