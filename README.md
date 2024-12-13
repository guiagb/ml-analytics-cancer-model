# Modelo de Previsão de Diagnóstico de Câncer

## Visão Geral
Este projeto implementa um pipeline de aprendizado de máquina para prever diagnósticos de câncer de mama com base nas características de tumores. O objetivo é classificar se um tumor é benigno ou maligno, utilizando diversos algoritmos de aprendizado de máquina e técnicas de pré-processamento. O conjunto de dados é pré-processado, balanceado e avaliado para construir um modelo eficaz para diagnósticos.

## Funcionalidades
- Pré-processamento dos dados, incluindo tratamento de valores ausentes, escalonamento de atributos e remoção de outliers.
- Implementação do SMOTE (Synthetic Minority Oversampling Technique) para balancear o conjunto de dados.
- Comparação de diversos algoritmos de aprendizado de máquina, incluindo:
  - K-Nearest Neighbors (KNN)
  - Árvores de Decisão (CART)
  - Naive Bayes (NB)
  - Support Vector Machines (SVM)
- Extração de importância dos atributos utilizando Random Forests.
- Ajuste de hiperparâmetros com GridSearchCV.
- Métricas de avaliação, incluindo acurácia, F1-score e ROC-AUC.
- Visualização do desempenho dos modelos por meio de boxplots e curvas ROC.

## Conjunto de Dados
O conjunto de dados utilizado neste projeto contém informações sobre diagnósticos de câncer de mama, incluindo:
- Características dos tumores (ex.: raio, textura, perímetro, área, suavidade, compacidade, etc.).
- Rótulos de diagnóstico: `M` (Maligno) e `B` (Benigno).

**Fonte**: [Link do Dataset](https://raw.githubusercontent.com/guiagb/ml-analytics-cancer-model/develop/cancer.csv)

## Estrutura do Projeto
```
.
├── cancer-model.ipynb     # Notebook principal contendo o código do projeto
├── README.md              # Documentação do projeto
├── requirements.txt       # Dependências Python
```

## Configuração do Ambiente

1. Clone este repositório:
   ```bash
   git clone https://github.com/yourusername/cancer-diagnosis-model.git
   ```
2. Navegue até o diretório do projeto:
   ```bash
   cd cancer-diagnosis-model
   ```
3. Crie um ambiente virtual e ative-o:
   ```bash
   python -m venv venv
   source venv/bin/activate   # No Windows: venv\Scripts\activate
   ```
4. Instale as dependências necessárias:
   ```bash
   pip install -r requirements.txt
   ```

## Uso

1. Abra o Jupyter Notebook:
   ```bash
   jupyter notebook cancer-model.ipynb
   ```
2. Execute as células passo a passo para:
   - Pré-processar o conjunto de dados
   - Treinar os modelos de aprendizado de máquina
   - Avaliar e comparar os resultados

## Resultados
O projeto compara o desempenho de vários modelos de aprendizado de máquina no conjunto de dados. Destaques incluem:
- **Melhor modelo**: SVM e KNN com pré-processamento padronizado.
- **Acurácia**: >95% nos conjuntos de treinamento e teste.
- **AUC-ROC**: Alta separação entre classes, indicando excelente poder preditivo.

## Melhorias Futuras
- Adicionar mais dados para melhorar a generalização do modelo.
- Testar modelos mais avançados, como XGBoost ou LightGBM.
- Validar o modelo em conjuntos de dados externos.
- Implementar o modelo como uma aplicação web para uso no mundo real.

## Licença
Este projeto está licenciado sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

## Agradecimentos
- Agradecimentos ao fornecedor do conjunto de dados por possibilitar este projeto.
- Inspirado pela necessidade de melhorar o diagnóstico precoce e o tratamento do câncer de mama.

