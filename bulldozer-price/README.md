# 🚜 Previsão do Preço de Venda de Bulldozers

Este projeto tem como objetivo principal **construir e avaliar um modelo de Machine Learning** capaz de prever o **preço de venda de escavadeiras**, com base em suas características e dados históricos de vendas.  
O projeto segue um **pipeline completo de Machine Learning**, desde a **análise exploratória dos dados (EDA)** e **pré-processamento**, até a **otimização de hiperparâmetros** e **avaliação final**.

---

## 🎯 Objetivo
Desenvolver um **modelo de regressão robusto** para prever o **SalePrice** (preço de venda) das escavadeiras.  
A métrica de avaliação principal é o **RMSLE** (Root Mean Squared Logarithmic Error).

---

## 🚀 Tecnologias Utilizadas

- **Linguagem:** Python
- **Bibliotecas:**
  - `pandas` e `numpy` → Manipulação e análise de dados
  - `matplotlib` → Visualização de dados e gráficos
  - `scikit-learn` → Construção, avaliação e otimização dos modelos

---

## 📁 Estrutura do Projeto

```
📂 ml_bulldozer_price
├── 📁 data                     # Contém os datasets e arquivos de saída
│   ├── Data Dictionary.xlsx
│   ├── Test.csv
│   ├── TrainAndValid.csv
│   ├── test_predictions.csv    # Saída: Previsões do modelo
│   └── train_tmp.csv           # Saída: Dados de treino pré-processados
├── bulldozer_price.ipynb       # Notebook Jupyter com o pipeline de ML
└── README.md                   # Documentação do projeto
```

---

## 📁 Dataset

O projeto utiliza **três datasets** da competição do Kaggle:

- `TrainAndValid.csv` → Dados de **treinamento e validação**
- `Test.csv` → Dados de **teste** para submissão
- `Data Dictionary.xlsx` → Dicionário com a descrição dos atributos

Os datasets contêm **50+ atributos**, incluindo:  
`SalesID`, `SalePrice`, `MachineID`, `ModelID`, `saledate`, `YearMade`, entre outros.

---

## ⚙️ Pipeline de Machine Learning

O **notebook bulldozer_price.ipynb** executa as seguintes etapas:

### **1. Análise Exploratória e Pré-processamento**
- Carregamento dos dados e inspeção inicial
- Visualização da relação entre `saledate` e `SalePrice`
- Criação de novas features (`saleYear`, `saleMonth`, `saleDay`, `saleDayOfWeek`, `saleDayOfYear`)
- Conversão de colunas `object` para `category` (melhora performance e otimiza memória)
- Preenchimento de valores ausentes:
    - Numéricos → **mediana**
    - Categóricos → **0**
- Exportação de um **novo CSV** pré-processado (`train_tmp.csv`)

### **2. Modelagem e Treinamento**
- Divisão dos dados → **Treino** vs **Validação** (ano de 2012 usado como validação)
- Criação do **modelo base** com `RandomForestRegressor`

### **3. Otimização de Hiperparâmetros**
- Uso de **RandomizedSearchCV** para encontrar os melhores hiperparâmetros

### **4. Avaliação Final**
- Treinamento do modelo **otimizado** com todos os dados disponíveis
- Avaliação com a função `show_scores()` calculando:
    - **MAE** (Mean Absolute Error)
    - **RMSLE** (Root Mean Squared Logarithmic Error)
    - **R²** (Coeficiente de Determinação)

### **5. Previsão com Dados de Teste**
- Pré-processamento do arquivo `Test.csv` seguindo as mesmas etapas
- Geração das previsões → Arquivo `test_predictions.csv`

---

## 🛠️ Como Executar o Projeto

### **1. Clone o repositório**
```bash
git clone https://github.com/HeitorDalla/ml_bulldozer_price
cd ml_bulldozer_price
```

### **2. Crie e ative o ambiente virtual**
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### **3. Instale as dependências**
```bash
pip install pandas numpy matplotlib scikit-learn openpyxl
```

### **4. Verifique os datasets**
Certifique-se de que os arquivos `Data Dictionary.xlsx`, `Test.csv` e `TrainAndValid.csv` estão na pasta `/data`.

### **5. Execute o notebook**
Abra o **notebook** e rode todas as células:
```bash
jupyter notebook bulldozer_price.ipynb
```

---

## 🤝 Contribuições

Contribuições são **bem-vindas**!  
Se encontrar problemas, bugs ou tiver sugestões de melhorias, **abra uma issue** ou envie um **pull request**.

---

📌 **Autor:** Heitor Giussani Dalla Villa  
📧 **Contato:** heitorvillavilla@email.com