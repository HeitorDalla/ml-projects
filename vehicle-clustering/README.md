# 🚗 Projeto de Agrupamento de Veículos com K-Means

Este projeto tem como objetivo agrupar veículos com base em características como **peso**, **tamanho do motor** e **potência** do motor, utilizando técnicas de aprendizado de máquina não supervisionado (clustering).

---

## ⚙️ Tecnologias Utilizadas

- **Python** – Linguagem de programação
- **Pandas** – Manipulação e análise de dados
- **NumPy** – Geração de dados e operações numéricas
- **Matplotlib** – Visualização de dados e clusters
- **Scikit-learn** – Algoritmo de K-Means
- **Pickle** – Serialização do modelo final

---

## 📁 Geração dos Dados

- Os dados utilizados neste projeto são **sintéticos**, gerados aleatoriamente com:
  - **Peso (Weight)**: entre 1000 e 3000 kg
  - **Tamanho do motor (EngineSize)**: entre 1.0 e 4.0 litros
  - **Potência (Horsepower)**: entre 50 e 300 hp

---

## 🎯 Objetivo

Aplicar o algoritmo **K-Means** para agrupar os veículos com base em suas características técnicas, sem utilizar rótulos (aprendizado não supervisionado).

---

## 🚀 Como Executar

### 1. Clonar o Repositório

```bash
git clone https://github.com/HeitorDalla/ml_vehicle_clustering.git
```

### 2. Instalar Dependências

```bash
pip install pandas numpy matplotlib scikit-learn
```

### 3. Executar o Script

```bash
python index.py
```

> Será exibido um gráfico com os clusters formados com base em **peso** e **potência**.

---

## 🔎 Lógica do Projeto

1. **Geração dos Dados**:
   - Dataset com 300 registros simulando veículos.

2. **Aplicação do Algoritmo**:
   - KMeans com `n_clusters=3`.

3. **Visualização**:
   - Os veículos são plotados em um gráfico 2D com cores diferentes representando os clusters.

4. **Persistência do Modelo**:
   - O modelo treinado é salvo em `final_model.pkl` com `pickle`.

---

## 📈 Exemplo de Saída

Um gráfico exibindo os grupos formados de veículos por semelhança entre **peso** e **potência**.

---

## 🧠 Possíveis Melhorias Futuras

- Aplicar redução de dimensionalidade (PCA) para análise mais completa.
- Determinar o número ótimo de clusters com o método do cotovelo (Elbow Method).
- Adicionar novos atributos como consumo, torque, tipo de combustível etc.
- Avaliar a coesão dos clusters com métricas como Silhouette Score.

---

## 👨‍💻 Autor

- **Heitor Giussani Dalla Villa**  
- 📧 [heitorvillavilla@gmail.com](mailto:heitorvillavilla@gmail.com)  
- 🔗 [LinkedIn](https://www.linkedin.com/in/heitordallavilla)

---

## 📝 Observações Finais

> Este projeto é uma demonstração prática de clustering usando dados sintéticos.  
> O foco é compreender como o algoritmo K-Means pode separar amostras em grupos com base em similaridade.
