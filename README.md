# Explorando Técnicas de Otimização e Agendamento de Taxa de Aprendizado no Dataset MNIST

## Sobre o Projeto

Este projeto explora diferentes técnicas de otimização (SGD, Momentum, Adam) e agendamento de taxa de aprendizado (StepLR, ExponentialLR, CyclicLR) aplicadas a uma Rede Neural Convolucional (CNN) treinada no dataset MNIST, um conjunto de dados clássico para classificação de dígitos escritos à mão.

---

## Requisitos

Antes de executar o projeto, certifique-se de ter os seguintes itens instalados:

1. **Python 3.7 ou superior**
2. **Bibliotecas Python:**
   - `torch`
   - `torchvision`
   - `matplotlib`
   - `numpy`

Instale as bibliotecas necessárias com o comando:
```bash
pip install torch torchvision matplotlib numpy
```

## Estrutura Geral do Projeto
### Preprocessamento do Dataset MNIST
- Carrega o dataset MNIST com torchvision.datasets.MNIST.
- Aplica transformações para converter imagens em tensores e normalizá-las.
- Cria DataLoaders para train e test, definindo batch_size e shuffle.

### Definição do Modelo CNN

- Modelo SimpleCNN, composto por camadas de convolução, pooling e camadas totalmente conectadas para classificação.
- Utiliza camada de dropout para regularização e função de ativação ReLU.

### Classe de Treinamento (StepByStep)

- Encapsula todo o processo de forward, backward e optimizer.step().
Permite setar:
- Scheduler para ajuste dinâmico do learning rate.
- Loaders de treino e validação.
-Armazena métricas de perda (loss) e acurácia para análise posterior.

### Treinamento e Avaliação com Otimizadores (SGD + Momentum)

- Define otimizador optim.SGD com momentum.
Configura a classe StepByStep passando modelo, função de perda (CrossEntropyLoss), otimizador e dispositivo (CPU/GPU).
- Executa o treinamento por um número definido de épocas e registra a perda e acurácia.

### Aplicação de Schedulers de Learning Rate

- Testa o otimizador Adam com um scheduler (StepLR), que reduz a taxa de aprendizado em determinados steps.
- Ajusta e observa o comportamento do treinamento (perda e acurácia) ao longo das épocas.

### Visualização de Resultados

- São plotados gráficos de perda e acurácia para comparar diferentes estratégias:
- SGD x Adam
- StepLR x ExponentialLR x CyclicLR
- Permite verificar como cada otimização e scheduler afeta a curva de aprendizado e a performance no conjunto de validação.

### Aplicação de Diferentes Learning Rate Schedulers

- Compara StepLR, ExponentialLR e CyclicLR, exibindo a evolução de loss e accuracy durante o treinamento.
- Demonstra as vantagens e desvantagens de cada agendamento de taxa de aprendizado.