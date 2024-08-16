# 🔒 Adversarial Attacks & Robustness

<p align="center">
  <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white" alt="PyTorch">
  <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54" alt="Python">
  <img src="https://img.shields.io/badge/Jupyter-F37626.svg?&style=for-the-badge&logo=Jupyter&logoColor=white" alt="Jupyter Notebook">
</p>
<p align="center">

Welcome to the **Adversarial Attacks & Robustness** repository! This project focuses on training a CNN using the CIFAR-10 dataset and evaluating its robustness against a spectrum of adversarial attacks. It covers both basic attacks like targeted and untargeted FGSM, as well as more sophisticated threats such as PGD attacks.

---

## 📂 Project Overview

This repository contains a Jupyter notebook that:
- Trains a CNN defined in the `resnet.py` file.
- Implements targeted and untargeted Fast Gradient Sign Method (FGSM) attacks.
- Implements the $l_{∞}$-Projected Gradient Descent (PGD) attack.
- Evaluates the model's performance using adversarial data generated by these attacks.

## 🛡️ Attacks

### 🎯 Targeted FGSM Attack
This attack aims to misclassify input images by perturbing them in a direction that maximizes the loss of the target class. By calculating the gradient of the loss function with respect to the input, small perturbations are added to the image pixels to shift the classification decision toward the desired target class.

### 🚫 Untargeted FGSM Attack
Similar to the targeted attack, the untargeted FGSM attack also perturbs input images. However, in this case, the objective is to maximize the loss of the true class, leading to misclassification into any incorrect class. The gradient of the loss function is computed with respect to the input, and perturbations are added to maximize the loss and cause misclassification.

### 🔄 $l_{∞}$-PGD Attack
The $l_{∞}$-PGD attack is a more powerful and iterative attack method. It performs multiple iterations of perturbations, each time adjusting the input image within a small $l_{∞}$-norm bound. This iterative process progressively maximizes the loss and produces adversarial examples that are challenging for the model to classify correctly.

## 📊 Insights
By implementing these attacks and evaluating the model's performance on the adversarial data, we gain insights into the model's robustness and its vulnerability to different types of attacks.

For more detailed information and code implementation, please refer to the notebook files in this repository.

---

Feel free to explore and contribute to this project. Let's make our models more robust together! 🚀

---

**Note:** Ensure you have the necessary dependencies installed to run the notebook and the `resnet.py` file.

---

Happy coding! 💻
