# 🏢 Projeto de Previsão de Eficiência Energética de Edifícios

Este projeto visa construir um modelo de regressão capaz de prever a **classificação de eficiência energética** de edifícios com base em características como **área da parede**, **área do telhado**, **altura total** e **área de envidraçamento**.

---

## ⚙️ Tecnologias Utilizadas

- **Python** – Linguagem de programação
- **Pandas** – Manipulação e análise de dados
- **NumPy** – Geração de dados e cálculos numéricos
- **Matplotlib / Seaborn** – Visualizações e análises gráficas
- **Scikit-learn** – Algoritmos de regressão, avaliação e particionamento dos dados
- **Pickle** – Serialização do modelo final

---

## 📁 Dados Utilizados

- **Fonte**: Dados sintéticos gerados com NumPy
- **Tamanho**: 500 amostras
- **Variáveis**:
  - `WallArea` – Área das paredes
  - `RoofArea` – Área do telhado
  - `OverallHeight` – Altura total do edifício
  - `GlazingArea` – Proporção de área de envidraçamento
  - `EnergyEfficiency` – Eficiência energética (variável alvo)

---

## 🎯 Objetivo

Criar um modelo de **regressão supervisionada** para prever o valor da eficiência energética com base em atributos arquitetônicos dos edifícios.

---

## 🚀 Como Executar

### 1. Clonar o Repositório

```bash
git clone https://github.com/HeitorDalla/ml_energy_efficiency.git
```

### 2. Instalar Dependências

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### 3. Executar o Script

```bash
python index.py
```

> Serão exibidas visualizações gráficas e a métrica de erro médio quadrático (MSE).

---

## 🔎 Lógica do Projeto

1. **Geração de Dados**:
   - Dados sintéticos representando características de edifícios e sua eficiência.

2. **Visualização Inicial**:
   - Utiliza `seaborn.pairplot()` para explorar relações entre variáveis.

3. **Separação dos Dados**:
   - Conjunto de treino (80%) e teste (20%) com `train_test_split`.

4. **Treinamento do Modelo**:
   - Modelo de regressão do tipo **Random Forest** com parâmetros padrão.

5. **Avaliação do Modelo**:
   - Métrica usada: **Erro Quadrático Médio (MSE)**
   - Gráfico comparativo entre valores reais e previstos.

6. **Salvamento do Modelo**:
   - O modelo treinado é salvo como `final_model.pkl` com `pickle`.

---

## 📊 Exemplo de Saída

```bash
Mean Squared Error: 12.14
```

Gráfico:

- Eixo X: Valores reais de eficiência
- Eixo Y: Valores previstos
- Linha tracejada: Linha ideal (previsão = realidade)

---

## 🧠 Possíveis Melhorias Futuras

- Ajuste de hiperparâmetros do modelo
- Testar outros algoritmos como XGBoost ou SVR
- Aplicar validação cruzada
- Coletar dados reais de projetos arquitetônicos

---

## 👨‍💻 Autor

- **Heitor Giussani Dalla Villa**  
- 📧 [heitorvillavilla@gmail.com](mailto:heitorvillavilla@gmail.com)  
- 🔗 [LinkedIn](https://www.linkedin.com/in/heitordallavilla)

---

## 📝 Observações Finais

> Este projeto tem finalidade educacional para demonstrar o uso de regressão com dados arquitetônicos sintéticos.  
> Pode ser adaptado facilmente para uso com dados reais em contextos profissionais de engenharia e arquitetura.
