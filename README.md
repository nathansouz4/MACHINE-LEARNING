# **PPGEEC2318 - Machine Learning Course Repository**

### **Student: Nathan Souza de Oliveira**

This repository is part of my coursework for the **Machine Learning** course in my post-graduation program in **Computer Engineering**, with an emphasis on **Intelligence Process of Information**, at **UFRN (Federal University of Rio Grande do Norte).**

Here, you will find various tasks and assignments related to the course, each organized within its respective branch.

---

## **Repository Organization**

The repository is structured with separate branches for each task and assignment from the Machine Learning course. This organization helps maintain a **clean and structured repository**, where each branch is dedicated to a specific piece of coursework.

### **Current Branches**
- `main`: This branch includes the general course information and links to other specific task branches.
- `task_1`: [Task 1 - Video Summaries of *Designing Machine Learning Systems*](https://github.com/nathansouz4/MACHINE-LEARNING/tree/task_1)
- `task_2`: [Task 2 - Technical Notes on Hooks in PyTorch](https://n4thansouza.medium.com/explorando-cnns-com-hooks-no-pytorch-a6dda8ed8bb1)
- `task_3`: [Task 3 - Technical Notes on Learning Rate Schedulers and Optimizers](#)
- `final_project`: [Final Project - Transfer Learning: ResNet18 vs. VGG16](https://github.com/nathansouz4/MACHINE-LEARNING/tree/final_project?tab=readme-ov-file)

---

## **Task 1: Video Summaries**

In the `task_1` branch, you will find a series of **five video summaries**. Each video is a **concise 5-minute explanation** covering the key points of the first five chapters of the book "**Designing Machine Learning Systems**" by **Chip Huyen**.

Additionally, this branch includes markdown files that provide a **written summary** of the key concepts and lessons learned from each chapter.

### [Go to Task 1](https://github.com/nathansouz4/MACHINE-LEARNING/tree/task_1)

---

## **Task 2: Technical Notes on Hooks in PyTorch**

In the `task_2` branch, you will find **technical notes and examples** about **PyTorch Hooks**. This task explores the usage of **forward and backward hooks** on CNN layers to **capture and analyze intermediate features or gradients**. These hooks facilitate:
- **Debugging and understanding internal representations** of the network;
- **Visualizing activation maps** or **gradient flows**;
- **Enhancing explainability** of CNN-based architectures.

You can also find a **Medium article** elaborating on these concepts:

### [Go to Task 2](https://n4thansouza.medium.com/explorando-cnns-com-hooks-no-pytorch-a6dda8ed8bb1)

---

## **Task 3: Technical Notes on Learning Rate Schedulers and Optimizers**

In the `task_3` branch (to be finalized), you will find an **in-depth exploration** of:
- **Optimizers** (e.g., **SGD, Adam, Momentum, Nesterov**);
- **Learning rate schedulers** (e.g., **StepLR, ExponentialLR, CyclicLR**).

This task covers:
- How **exponentially weighted moving averages (EWMA)** are applied to gradients (e.g., Adam);
- Comparisons between **adaptive optimizers** and **classic SGD** with momentum/Nesterov momentum;
- Practical examples demonstrating how different schedulers adjust the **learning rate** to **improve convergence** and **avoid overfitting**;
- Integration of these strategies into a CNN **training pipeline**, including **visualizations of loss curves and gradient behaviors**.

A **Medium article** detailing these notes and experiments is forthcoming:

### [Go to Task 3](#)

---

## **Final Project: Transfer Learning - ResNet18 vs. VGG16**

The **final project** of the Machine Learning course explores **Transfer Learning**, comparing the performance of **ResNet18** and **VGG16** in classifying images from the **Intel Image Classification** dataset.

### **Project Overview**
- **Objective**: Evaluate the effectiveness of **Transfer Learning** by fine-tuning **pre-trained models** (ResNet18 & VGG16) for **image classification**.
- **Dataset**: Intel Image Classification (**6 categories**: buildings, forest, glacier, mountain, sea, street).
- **Methodology**:
  - Models were initialized with **pre-trained weights** from ImageNet.
  - The **final layers were replaced** and fine-tuned for **6-class classification**.
  - The dataset was split into **training (80%), validation (10%), and testing (10%)**.
  - Models were trained for **5 epochs** with **data augmentation** and **learning rate scheduling**.
  - Performance was measured using **accuracy, precision, recall, F1-score, and confusion matrices**.

### **Key Takeaways**
- **ResNet18**: Lighter and faster, with competitive accuracy.
- **VGG16**: Requires **more computational resources**, but often achieves **high classification performance**.
- **Confusion Matrices & F1-Scores**: Provided detailed insights into **class-wise performance**.

### **Links**
- 🔗 **GitHub Repository (Final Project Branch):**  
  [Final Project - Transfer Learning: ResNet18 vs. VGG16](https://github.com/nathansouz4/MACHINE-LEARNING/tree/final_project?tab=readme-ov-file)  
- 📝 **Detailed Medium Article:**  
  [Transfer Learning: Performance Analysis - ResNet18 vs. VGG16](https://n4thansouza.medium.com/transfer-learning-an%C3%A1lise-de-desempenho-resnet18-x-vgg16-b774881089e8)  

---

## **About This Course**

The **Machine Learning** course is an integral part of the **Computer Engineering** program, tailored to **deepen the understanding of intelligent information processing systems**. Through **hands-on tasks** and **comprehensive assignments**, students gain both **practical and theoretical** knowledge crucial for advancing in the field of **Machine Learning and Information Processing**.
