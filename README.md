# **Transfer Learning Project**

## **Sobre o Projeto**
Este repositório contém um projeto de **Transfer Learning** que compara duas arquiteturas pré-treinadas, **ResNet18** e **VGG16**, aplicadas ao dataset **Intel Image Classification**. O objetivo principal é avaliar o desempenho de cada modelo, observando como se adaptam à tarefa de classificação de cenários e paisagens.

---

## **Contexto e Objetivo**
O projeto demonstra a utilização de **Transfer Learning** a partir de modelos pré-treinados no ImageNet (**ResNet18** e **VGG16**) para classificar imagens do dataset Intel Image Classification. O foco é comparar as **acurácias** obtidas e analisar **quais arquiteturas** melhor se adequam às características do conjunto de dados, levando em conta fatores como tempo de treino e recursos computacionais.

---

## **Descrição do Dataset**
O **Intel Image Classification** consiste em imagens de paisagens e cenários urbanos, divididas em **6 classes**:
- `buildings`
- `forest`
- `glacier`
- `mountain`
- `sea`
- `street`

A organização original do dataset traz pastas para:
- `seg_train`: conjunto de imagens para treino  
- `seg_test`: conjunto de imagens para teste  

> Foi criado um diretório adicional **`seg_val`**, separando aproximadamente **10%** dos dados de `seg_train` para validação. Assim, trabalhamos com três subconjuntos: **treino**, **validação** e **teste**.

---

## **Estrutura do Projeto**
1. **Download do Dataset via Kaggle**  
2. **Importação de bibliotecas** (PyTorch, Torchvision, etc.)  
3. **Organização do dataset** (treino/validação/teste)  
4. **Definição de transformações** (Resize, Flip, Normalize)  
5. **Criação de Datasets e DataLoaders**  
6. **Visualização** de imagens de treino  
7. **Configuração dos modelos** (ResNet18 e VGG16) para Transfer Learning  
8. **Função de treinamento e validação** (`train_model`)  
9. **Avaliação** no conjunto de teste (`evaluate_model`)  
10. **Comparação final** de acurácia e curvas de aprendizado  

---

## **Resultados**
- **Acurácia**: Ao final do treinamento, o projeto exibe a acurácia de teste de cada modelo (ResNet18 e VGG16), permitindo uma comparação direta no console/terminal.  
- **Curvas de Aprendizado**: Há um gráfico que compara a evolução da acurácia de **treino** e **validação** para ResNet18 vs. VGG16.

Em geral, cada arquitetura apresenta vantagens e desvantagens:  
- **ResNet18**: Rede mais leve, com menos parâmetros, resultando em um **menor tempo de treinamento** e ainda bom desempenho.  
- **VGG16**: Rede mais antiga, mas com um número maior de parâmetros, podendo **exigir mais recursos computacionais**, porém frequentemente alcança **excelente desempenho** em classificação de imagens.

---

### **Possíveis Melhorias**
- **Fine-Tuning**: Descongelar mais camadas (ou todas) para refinar os pesos além da última camada (`fc` ou `classifier`).  
- **Data Augmentation Avançado**: Utilizar `RandomRotation`, `ColorJitter`, `RandomResizedCrop`, etc.  
- **Scheduler**: Empregar redução de taxa de aprendizado (*StepLR*, *ReduceLROnPlateau*, etc.).   
- **Outras Arquiteturas**: Comparar com DenseNet, MobileNet, EfficientNet, Vision Transformers, etc.

---

## **Referências**
- **He, K., Zhang, X., Ren, S., & Sun, J. (2015).** *Deep Residual Learning for Image Recognition.* CVPR.  
- **Simonyan, K., & Zisserman, A. (2014).** *Very Deep Convolutional Networks for Large-Scale Image Recognition.* arXiv preprint arXiv:1409.1556.  
- **Godoy, D. V. (2021).** *Deep Learning with PyTorch Step by Step.* (Capítulo 7 aborda Transfer Learning)  
- **Kaggle:** [Intel Image Classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)  

---
### **Artigo no Medium**

Para uma explicação mais detalhada do projeto, incluindo contexto, metodologia e análise aprofundada dos resultados, confira o artigo publicado no Medium.

🔗 Acesse o artigo completo clicando **[aqui](https://n4thansouza.medium.com/transfer-learning-an%C3%A1lise-de-desempenho-resnet18-x-vgg16-b774881089e8)**.
